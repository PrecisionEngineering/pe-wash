<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';

defineProps({
    bizs: Object
})
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">
                Businesses
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white dark:bg-gray-800 overflow-hidden shadow-xl sm:rounded-lg">
                    <template v-for="biz in bizs.data" :key="biz.id">
                        <pre>{{ biz }}</pre>
                    </template>

                    <div>{{ bizs.links }}</div>
                </div>
            </div>
        </div>
    </AppLayout>
</template>

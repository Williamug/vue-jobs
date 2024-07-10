<script setup>
import JobListing from '@/components/JobListing.vue';
import jobData from '@/jobs.json';
import { ref } from 'vue';

const jobs = ref(jobData);
console.log(jobs.value);
</script>

<template>
    <section class="px-4 py-10 bg-blue-50">
        <div class="m-auto container-xl lg:container">
            <h2 class="mb-6 text-3xl font-bold text-center text-green-500">
                Browse Jobs
            </h2>

            <div class="grid grid-cols-1 gap-6 md:grid-cols-3">
                <JobListing v-for="job in jobs" :key="job.id" :job="job" />
            </div>
        </div>
    </section>
</template>
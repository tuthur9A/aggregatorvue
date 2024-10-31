<script setup lang="ts">
import axios from 'axios'
import JobCard from './JobCard.vue'
import type { IJob } from '@/Model/job.model'
import { onMounted } from 'vue'

async function getJobs() {
  const jobs = await axios.get<IJob[]>('http://localhost:3001/jobs')
  jobsTest.push(...(jobs.data || []))
}

onMounted(async () => {
  await getJobs()
})
defineProps<{
  msg: string
}>()
const jobsTest: IJob[] = [
  {
    id: '1',
    name: 'test',
    url: 'https://portfolio.arthurcargnelli.fr',
  },
  {
    id: '2',
    name: 'test',
    url: 'https://portfolio.arthurcargnelli.fr',
  },
]
</script>

<template>
  <div v-for="item in jobsTest" v-bind:key="item.id" class="container">
    <JobCard :job="item" />
  </div>
</template>

<style scoped></style>

<script setup lang="ts">
import type { IJob } from '@/Model/job.model'

defineProps<{
  job: IJob
}>()
</script>

<template>
  <div class="jobs">
    <a :href="job.url">
      <div class="job-card">
        <h3>{{ job.name }}</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore
          nostrum distinctio excepturi beatae optio possimus eos commodi
          repudiandae itaque modi ipsa, placeat quis sint fugit tempore quia
          quasi autem architecto.
        </p>
      </div>
    </a>
  </div>
</template>

<style scoped>
.job-card {
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  border-radius: 5px; /* 5px rounded corners */
  padding: 2px 16px;
}

/* On mouse-over, add a deeper shadow */
.job-card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

/* Add some padding inside the card container */
.jobs {
  padding: 2px 16px;
}

/* Add rounded corners to the top left and the top right corner of the image */
/* img {
  border-radius: 5px 5px 0 0;
} */
</style>

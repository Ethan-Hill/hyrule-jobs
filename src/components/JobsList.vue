<template>
  <div class="job-list">
    <ul>
      <li v-for="job in Jobs" :key="job.id">
        <h2>{{ job.title }} in {{ job.location }}</h2>
        <div class="salary">
          <p>{{ job.salary }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup="props" lang="ts">
import type Job from "@/types/Job";
import { defineProps } from "vue";

defineProps<{
  Jobs: Job[];
}>();
</script>

<style lang="scss">
li {
  list-style: none;
}
</style>

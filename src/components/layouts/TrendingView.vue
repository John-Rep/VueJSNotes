<script lang="ts" setup>
import type { Trend } from "@/models/trend"
const props = defineProps<{
    trend: Trend
}>()
</script>
<template>
    <div class="trend">
                  <figure>
                    <img
                      class="avatar"
                      :src="props.trend.image"
                      alt="avatar"
                    />
                  </figure>
                  <div class="trend-details">
                    <h6>{{ trend.name }}</h6>
                    <p>{{ trend.title }}</p>
                  </div>
                </div>
</template>
<style></style>
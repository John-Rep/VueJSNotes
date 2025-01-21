<script lang="ts" setup>
import type { Announcement } from "@/models/announcement"
const props = defineProps<{
    announcement: Announcement
}>()
</script>
<template>
    <div class="anounce">
                  <h5>{{ announcement.title }}</h5>
                  <p>
                    {{ announcement.content }}
                  </p>
                </div>
</template>
<style></style>
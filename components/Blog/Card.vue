<script lang="ts" setup>
defineProps<{
  title: string;
  excerpt?: string;
  image?: string;
  slug?: string;
}>();
</script>

<template>
            <div class="col-span-1 shadow-lg">
                <!-- Blog Image -->
                <div v-if="image" class="w-full h-[180px] relative">
                    <img
                     :src="image" 
                     alt="Blog Thmbnail" 
                     class="w-full h-full absolute object-cover"
                    />
                </div>
                <!-- Blog Contents -->
                <div class="p-5">
                    <h3 class="text-xl font-semibold mb-3">
                        {{ title }}
                    </h3>
                    <p class="text-sm mb-3">
                        {{ excerpt }}
                    </p>
                    <NuxtLink :to=" `/${slug} `">Read More</NuxtLink>
                </div>
            </div>
</template>
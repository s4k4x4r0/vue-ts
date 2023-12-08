<script setup lang="ts">
import { GoogleMap, Marker, CustomControl } from 'vue3-google-map'
import { Edit } from '@element-plus/icons-vue'
const apiKey = import.meta.env.VITE_GOOGLE_MAPS_API_KEY
</script>

<template>
  <GoogleMap
    :api-key="apiKey"
    :center="{ lat: 35.6585805, lng: 139.742858 }"
    style="width: 100%; height: 500px"
    :zoom="15"
    :disable-default-ui="true"
    :clickable-icons="false"
    :fullscreenControl="false"
  >
    <CustomControl position="BOTTOM_RIGHT">
      <el-button type="warning" :icon="Edit"></el-button>
    </CustomControl>
    <CustomControl position="BOTTOM_RIGHT">
      <el-button type="info" :icon="Edit"></el-button>
    </CustomControl>
    <CustomControl position="BOTTOM_RIGHT">
      <el-button type="info" :icon="Edit"></el-button>
    </CustomControl>
    <Marker :options="{ position: { lat: 35.6585805, lng: 139.742858 } }" />
  </GoogleMap>
</template>

<style></style>

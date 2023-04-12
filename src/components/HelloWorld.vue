<template>
  <div>
    <el-upload
      :before-upload="upload"
    >
    <el-button>上传</el-button>
    </el-upload>
  </div>
</template>

<script lang="ts" setup>
import { onMounted } from 'vue';

function upload(file: any) {
  console.log(file)
  const blob = new Blob([JSON.stringify(file)], {type: 'text/plain;charset=utf-8'})
  console.log(blob)
  return
}
</script>
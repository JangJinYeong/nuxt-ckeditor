<template>
  <div>
    <h1>CKEditor 4 in Nuxt.js</h1>
    <div v-if="isClient">
      <ckeditor v-model="editorData"></ckeditor>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      editorData: '<p>Content of the editor.</p>',
      isClient: false,
    }
  },
  mounted() {
    // 컴포넌트가 클라이언트 사이드에서만 로드되도록 설정
    this.isClient = true
  },
}
</script>

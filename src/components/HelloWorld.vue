<template>
  <div class="main-container">
    <div style="width: 100%">
      <MarkdownPreview :markdown-content="text"/>
    </div>
    <div style="width: 100%;">
<!--      <MdComment />-->
    </div>
  </div>
</template>

<script lang="ts">
import MarkdownPreview from "./MarkdownPreview.vue";
import MdComment from "./MarkdownComment.vue";
export default {
  components: {MdComment, MarkdownPreview},
  data() {
    return {
      text: `
## title1
> hello
## title2
> hello
## title3
> hello
## title4
> hello
## title5
> hello
## title6
> hello
      `
    }
  }
}
</script>
<style scoped>
.main-container {
  width: 100%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
}
</style>
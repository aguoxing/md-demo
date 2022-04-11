<template>
  <div class="md-editor-preview">
    <MdEditor
        editorId="preview-editor"
        v-model="markdownContent"
        :previewOnly="true"
        :previewTheme="'vuepress'"
    />
    <MdCatalog editorId="preview-editor" :scrollElement="scrollElement" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import MdEditor from 'md-editor-v3'
import 'md-editor-v3/lib/style.css'

const MdCatalog = MdEditor.Catalog

export default defineComponent({
  name: 'MarkdownPreview',
  components: {
    MdEditor,
    MdCatalog
  },
  props: {
    markdownContent: {
      type: String,
      default: 'no data',
      required: true
    }
  },
  data() {
    return {
      scrollElement: document.scrollingElement
    }
  }
})
</script>
<style scoped>
.md-editor-preview {
  display: flex;
  flex-direction: row;
}
</style>

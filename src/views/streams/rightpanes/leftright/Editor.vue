<template>
  <section class="shadow p-3 mb-5 bg-body-tertiary rounded">
    <div v-if="editor" class="tiptap-header">
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleBold().run()"
        :disabled="!editor.can().chain().focus().toggleBold().run()"
        :class="{ 'is-active': editor.isActive('bold') }"
      >
        <EditorIcon
          link="https://img.icons8.com/windows/32/null/bold.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleItalic().run()"
        :disabled="!editor.can().chain().focus().toggleItalic().run()"
        :class="{ 'is-active': editor.isActive('italic') }"
      >
        <EditorIcon
          link="https://img.icons8.com/fluency-systems-filled/48/null/italic.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleStrike().run()"
        :disabled="!editor.can().chain().focus().toggleStrike().run()"
        :class="{ 'is-active': editor.isActive('strike') }"
      >
        <EditorIcon
          link="https://img.icons8.com/fluency-systems-filled/48/null/strikethrough.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleCode().run()"
        :disabled="!editor.can().chain().focus().toggleCode().run()"
        :class="{ 'is-active': editor.isActive('code') }"
      >
        code
      </button>

      <button
        class="tip-btn"
        @click="editor.chain().focus().setParagraph().run()"
        :class="{ 'is-active': editor.isActive('paragraph') }"
      >
        <EditorIcon
          link="https://img.icons8.com/ios-filled/50/null/paragraph.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleHeading({ level: 1 }).run()"
        :class="{ 'is-active': editor.isActive('heading', { level: 1 }) }"
      >
        h1
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleHeading({ level: 2 }).run()"
        :class="{ 'is-active': editor.isActive('heading', { level: 2 }) }"
      >
        h2
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleHeading({ level: 3 }).run()"
        :class="{ 'is-active': editor.isActive('heading', { level: 3 }) }"
      >
        h3
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleHeading({ level: 4 }).run()"
        :class="{ 'is-active': editor.isActive('heading', { level: 4 }) }"
      >
        h4
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleHeading({ level: 5 }).run()"
        :class="{ 'is-active': editor.isActive('heading', { level: 5 }) }"
      >
        h5
      </button>
      
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleHeading({ level: 6 }).run()"
        :class="{ 'is-active': editor.isActive('heading', { level: 6 }) }"
      >
        h6
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleBulletList().run()"
        :class="{ 'is-active': editor.isActive('bulletList') }"
      >
        <EditorIcon
          link="https://img.icons8.com/ios-glyphs/30/null/overview-pages-3--v2.png"
        ></EditorIcon>
      </button>
      <button
        @click="editor.chain().focus().toggleOrderedList().run()"
        :class="{ 'is-active': editor.isActive('orderedList') }"
        class="tip-btn"
      >
        <EditorIcon
          link="https://img.icons8.com/fluency-systems-regular/48/null/numbered-list.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().toggleCodeBlock().run()"
        :class="{ 'is-active': editor.isActive('codeBlock') }"
      >
        <EditorIcon
          link="https://img.icons8.com/ios/50/null/code--v1.png"
        ></EditorIcon>
      </button>

      <button
        class="tip-btn"
        @click="editor.chain().focus().setHorizontalRule().run()"
      >
        <EditorIcon
          link="https://img.icons8.com/ios-filled/50/null/horizontal-line.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().setHardBreak().run()"
      >
        <EditorIcon
          link="https://img.icons8.com/ios-filled/50/null/space-after-paragraph.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().undo().run()"
        :disabled="!editor.can().chain().focus().undo().run()"
      >
        <EditorIcon
          link="https://img.icons8.com/metro/26/null/undo.png"
        ></EditorIcon>
      </button>
      <button
        class="tip-btn"
        @click="editor.chain().focus().redo().run()"
        :disabled="!editor.can().chain().focus().redo().run()"
      >
        <EditorIcon
          link="https://img.icons8.com/metro/26/null/redo.png"
        ></EditorIcon>
      </button>
    </div>
    <editor-content :editor="editor" />
  </section>
</template>

<script lang="js">
import StarterKit from "@tiptap/starter-kit";
import { Editor, EditorContent } from "@tiptap/vue-3";
import EditorIcon from "./EditorIcon.vue";
export default {
  components: {
    EditorContent,EditorIcon
  },

  data() {
    return {
      editor: null,
    };
  },

  mounted() {
    this.editor = new Editor({
      extensions: [StarterKit],
    });
  },

  beforeUnmount() {
    this.editor.destroy();
  },
};
</script>

<style lang="scss">
/* Basic editor styles */
.tiptap-header {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-evenly;
  gap: 0.5em;
  margin-top: 10px;
  border-bottom: 2px solid #a0a0a0;
  padding: 20px 5px;
}
.tip-btn {
  border: 0;
}
.ProseMirror {
  outline: none;
  min-height: 200px;
  padding: 10px 15px;
}
.ProseMirror {
  > * + * {
    margin-top: 0.75em;
  }

  ul,
  ol {
    padding: 0 1rem;
  }

  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    line-height: 1.1;
  }

  code {
    background-color: rgba(#616161, 0.1);
    color: #616161;
  }

  pre {
    background: #0d0d0d;
    color: #fff;
    font-family: "JetBrainsMono", monospace;
    padding: 0.75rem 1rem;
    border-radius: 0.5rem;

    code {
      color: inherit;
      padding: 0;
      background: none;
      font-size: 0.8rem;
    }
  }

  img {
    max-width: 100%;
    height: auto;
  }

  blockquote {
    padding-left: 1rem;
    border-left: 2px solid rgba(#0d0d0d, 0.1);
  }

  hr {
    border: none;
    border-top: 2px solid rgba(#0d0d0d, 0.1);
    margin: 2rem 0;
  }
}
</style>

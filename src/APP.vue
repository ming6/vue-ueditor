<template>
  <div id="app">
    <VueUEditor @ready="editorReady" v-model="content" style="width: 800px"></VueUEditor>
    {{content}}
  </div>
</template>

<script>
  import VueUEditor from './components/UEditor';
  export default {
    name: 'app',
    data () {
      return {
        content: 'Hello world!<br>你可以在这里初始化编辑器的初始内容。'
      };
    },
    components: { VueUEditor },
    methods: {
      editorReady (editorInstance) {
        this.content = 'Hello world!<br>变了';
//        editorInstance.setContent('Hello world!<br>你可以在这里初始化编辑器的初始内容。');
//        editorInstance.addListener('contentChange', () => {
//          console.log('编辑器内容发生了变化：', editorInstance.getContent());
//        });
      }
    }
  };
</script>

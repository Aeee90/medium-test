<template>
  <div id="editor" >

  </div>
</template>
<script>
    import MediumEditor from 'medium-editor';

    const editor = new MediumEditor('#editor', {});

    export default {
        name: "Editor"
    }
</script>

<style scoped>

</style>

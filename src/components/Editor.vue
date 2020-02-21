<template>
  <div>
    <link rel="stylesheet" href="../assets/demo.css">
    <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.css">
    <link rel="stylesheet" href="../assets/theme/default.css" id="medium-editor-theme">
    <div class="editable">
      <h2>Font Awesome</h2>
      <p>My father’s family name being <a href="https://en.wikipedia.org/wiki/Pip_(Great_Expectations)">Pirrip</a>, and my Christian name Philip, my infant tongue could make of both names nothing longer or more explicit than Pip. So, I called myself Pip, and came to be called Pip.</p>
      <p>I give Pirrip as my father’s family name, on the authority of his tombstone and my sister,—Mrs. Joe Gargery, who married the blacksmith. As I never saw my father or my mother, and never saw any likeness of either of them (for their days were long before the days of photographs), my first fancies regarding what they were like were unreasonably derived from their tombstones...</p>
    </div>

    <div>
      <button @click="getContent">Get Content</button>
    </div>
  </div>
</template>
<script>
    import MediumEditor from 'medium-editor';

    const editor = new MediumEditor('.editable', {
      activeButtonClass: 'medium-editor-button-active',
      toolbar: {
        buttons: ['bold', 'italic', 'underline', 'strikethrough', 'quote', 'anchor', 'image', 'justifyLeft', 'justifyCenter', 'justifyRight', 'justifyFull', 'superscript', 'subscript', 'orderedlist', 'unorderedlist', 'pre', 'removeFormat', 'outdent', 'indent', 'h2', 'h3', 'html'],
        static: true,
        sticky: true
      },
      buttonLabels: 'fontawesome',
      anchor: {
        targetCheckbox: true
      }
    });
    editor.setup();
    console.log(editor);

    export default {
        name: "Editor"
        , methods: {
        getContent() {
            console.log(editor.getContent());
            console.log(editor.serialize());
          }
      }
    }
</script>

<style scoped>
</style>

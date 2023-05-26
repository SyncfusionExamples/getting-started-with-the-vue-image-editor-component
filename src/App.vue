<template>
  <div style="height: 550px; width: 700px;">
    <ejs-imageeditor ref="editorObject" :created="openImage" ></ejs-imageeditor>
  </div>
  <div style="padding-top: 20px;">
    <ejs-button isPrimary="true" :onClick="saveImage">SAVE</ejs-button>
  </div>
 
</template>

<script>
import { ImageEditorComponent } from '@syncfusion/ej2-vue-image-editor';
import { ButtonComponent } from '@syncfusion/ej2-vue-buttons';

export default {
  name: 'App',
  components: {
    'ejs-imageeditor': ImageEditorComponent,
    'ejs-button': ButtonComponent
  },
  methods: {
    saveImage: function(){
      this.$refs.editorObject.export("PNG", "Syncfusion");
    },
    openImage: function(){
      this.$refs.editorObject.open('https://ej2.syncfusion.com/demos/src/image-editor/images/bridge.png');     
    }
  }
}
</script>

<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
@import "../node_modules/@syncfusion/ej2-lists/styles/material.css";
@import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
@import "../node_modules/@syncfusion/ej2-splitbuttons/styles/material.css";
@import "../node_modules/@syncfusion/ej2-navigations/styles/material.css";
@import "../node_modules/@syncfusion/ej2-inputs/styles/material.css";
@import "../node_modules/@syncfusion/ej2-image-editor/styles/material.css"; 
</style>

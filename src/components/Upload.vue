<template>
  <div class="upload">
    <FileUpload
      name="demo[]"
      url="./upload.php"
      :multiple="true"
      accept=".pdf"
      :maxFileSize="1000000"
      v-model="filesUploaded"
      ref="upload"
      @uploader="uploadFile"
    >
      <template #empty>
        <p class="instruction">Drag and drop files to here to upload.</p>
      </template>
    </FileUpload>
  </div>
</template>


<script>
import FileUpload from 'primevue/fileupload';

export default {
    components:{
        FileUpload
    },
    data(){
      return{
        filesUploaded: []
      }
    },
    mounted() {
      console.log(this.$refs['upload']);
    },
    watch:{
      filesUploaded(){
        console.log('Goas');
        if (this.filesUploaded.length > 0) {
          console.log(this.filesUploaded[0]);
        }
      }
    },
    methods:{
      uploadFile(event){
        console.log(event);
      }
    }
};
</script>

<style>
</style>
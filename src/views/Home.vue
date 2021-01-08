<template>
  <div class="home">
    <Upload/>

  </div>
</template>

<script>
import Upload from '../components/Upload';

export default {
  name: "Home",
  components: {
    Upload
  },
  methods:{
    onUpload() {
			this.$toast.add({severity: 'info', summary: 'Success', detail: 'File Uploaded', life: 3000});
		}
  }
};
</script>

<style>
.p-fileupload{
  width: 50%;
  margin: 0px auto;
}

.p-fileupload-empty{
  width: 100%;
}

</style>

<template>
  <form enctype="multipart/form-data">
    <div class="container">
      <label
        >Files
        <input
          type="file"
          id="files"
          ref="files"
          multiple
          v-on:change="handleFilesUpload()"
        />
      </label>
    </div>
    <div>
      <div v-for="(file, key) in files" :key="key" class="file-listing">
        {{ file.name }}
        <span class="remove-file" v-on:click="removeFile(key)">Remove</span>
      </div>
    </div>
    <br />
    <div>
      <button
        class="group relative justify-center py-2 px-2 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
        v-on:click="addFiles()"
      >
        Add Files
      </button>
    </div>
    <br />
    <div>
      <button
        class="group relative justify-center py-2 px-2 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
        v-on:click="submitFiles()"
      >
        Submit
      </button>
    </div>
  </form>
</template>
<script>
export default {
  data() {
    // Defines the data used by the component
    // setting a local piece of data
    return {
      files: [],
    };
  },

  methods: {
    addFiles() {
      // adds a file
      this.$refes.files.click();
    },

    handleFileUpload() {
      // Handles change on the file upload
      let uploadedFiles = this.$refes.files.files;

      //Adds the uploaded file to the files array

      for (var i = 0; i < uploadedFiles.length; i++) {
        this.files.push(uploadedFiles[i]);
      }
    },

    removeFile(key) {
      this.files.splice(key, 1);
    },

    submitFiles() {
      // Submits the file to the server

      const formData = new FormData();
      formData.append("repositoryName", "unknown"); //  // Add the form data we need to submit
      formData.append("commitName", "unknown");
      formData.append("fileData", this.$refs.fileInputRef.files.item(0));
      formData.append(
        "fileRelativePath",
        this.$refs.fileInputRef.files.item(0)
      );
      formData.append("commitName", "unknown");
      formData.append("productName", "unknown");
      formData.append("releaseName", "unknown");
      formData.append("repositoryUrl", this.$refs.fileInputRef.files.item(0));
      formData.append("branchName", "unknown");
      formData.append("ciUploadld", this.$refs.fileInputRef.files.item(0));
      fetch("http://localhost:8080/api/1.0/open/uploads/dependencies/files", {
        method: "POST",
        headers: {
          Authorization: "Bearer " + this.token,
          "Content-Type": "multipart/form-data",
        },

        body: formData,
      }).then((res) => {
        console.log("Request complete! response:", res);
      });
    },
  },
};

/* tried to use axios but did not work

      let formData = new FormData(); // Initialize the form data
      for (var i = 0; i < this.files.length; i++) {
        let file = this.files[i];
        formData.append("files[" + i + "]", file);
      }
      //formData.append("file", this.file); // Add the form data we need to submit

      const axios = require("axios").default;

      axios
        .post("/select-files", formData, {
          // make the request to the POST/ single-file URL
          headers: {
            "Content-Type": "multipart/form-data",
          },
        })
        .then(function() {
          console.log("Uploaded");
        })
        .catch(function() {
          console.log("Failure!");
        });
    },

    */
</script>

<style>

</style>

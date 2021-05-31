<template>
  <form enctype="multipart/form-data">
    <div class="container">
      <label
        >Files
        <input
          type="file"
          id="files"
          ref="files"
          v-on:change="filesRelativePath()"
        />
      </label>
    </div>
    <div>
      <div v-for="files in files" :key="files" class="file-listing">
        {{ files.ciUploadId }} - {{ files.repositoryName }} - {{ files.commitName }} -
        {{ files.productName }} - {{ files.releaseName }} - {{ files.repositoryUrl }}
        {{ files.branchName }}
        <span class="remove-file" v-on:click="removeFiles(files)">Remove</span>
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
      <router-link to="/api">
        <button
          class="group relative justify-center py-2 px-2 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          v-on:click="submitFiles()"
        >
          Submit
        </button></router-link
      >
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

    fileRelativePath() {
      // Handles change on the file upload
      let uploadedFiles = this.$refes.files.files;

      //Adds the uploaded file to the files array

      for (var i = 0; i < uploadedFiles.length; i++) {
        this.files.push(uploadedFiles[i]);
      }
    },

    removeFile(file) {
      this.files.splice(file);
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
      formData.append("productName", "unknown");
      formData.append("releaseName", "unknown");
      formData.append("repositoryUrl", this.$refs.fileInputRef.files.item(0));
      formData.append("branchName", "unknown");
      formData.append("ciUploadld", this.$refs.fileInputRef.files.item(0));
      fetch("http://localhost:8080", {
        method: "POST",
        headers: {
          Authorization:
            "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzUxMiJ9.eyJpYXQiOjE2MjIxMzU3MzcsImV4cCI6MTYyMjEzOTMzNywicm9sZXMiOlsiUk9MRV9VU0VSIiwiUk9MRV9DT01QQU5ZX0FETUlOIl0sInVzZXJuYW1lIjoiNWU3ZmUxYTY1OWMzNjIxODY3NGMwYjI5ZDBiYjk0YTkwOTM2NWU1OCJ9.f9XOR6ldi7t0BhIw5fzPnvFgwscanbcfcJEOtg2mII-524Q02o4DaMTuor4COKnhgWa2h0BYV914JCuNCRGsKiUoymHYcEuSicwFkxUqo6b9YqoUr5fM1-Oi5Tly-0PK2qJgnU0VzUoXXS6DDeMnbA4QLpjZiukF6YExy_02sNxZZ1B9ck6u4uYvyOAbfh0cPyJ3RlUJ0dje_YRhCiILYBNDuoSpOwoM7o57Vvg_Ly8KlV6YDmJtJDZXj5QpBrkADfY0wFu7TqI69lcP-0ORQRRr6YrRXY8j7Iu-kP5dxjR4UhHyIy0aXOBf3h1pgIKcV4x9rkt6UZnn9SfuNrYRmUmQP-JzutKze-rGrH_5WqKpwNVgA5D0-cjYCxzNsjczlvSieej3mu_V8NFqs9WvYwBYFMi3vhwr7FN3B7F2qQBT6IINY4bzIOP-wfjBZQLmKfTe55ENLhEaatNkO9a88dFa5ZxDqIkaJM1PxOUYL4HUGJW-n8tKx-MXeoqZiNhImX5MYlu55Jv_x5ZdFfzH1xU6qnhWIMctyvko7RpiL-4GALumkYkHpGFz94I3wbZD01hMFwPPo2-VRy14BXUrKzClWXgnXXi9dBxDpZguim6Ad9O74jXBYVl_nrgbxvoA37FETeG2AJs2jb1vi_L09yKjK7AUTmnqAokO2QGPhlQ",
          "Content-Type": "multipart/form-data",
        },

        body: formData,
      }).then((res) => {
        console.log("Request complete! response:", res);
      });
    },
  },
};

/* 
  
curl -X POST https://app.debricked.com/api/login_check --data-urlencode _username='conscientia.digitaltech@gmail.com' --data-urlencode _password='Daemon17338889'
}*/
</script>
<style>
#input[type="file"] {
  position: absolute;
  top: -500px;
}

#div.file-listing {
  width: 200px;
}

#span.remove-file {
  color: red;
  cursor: pointer;
  float: right;
}
</style>

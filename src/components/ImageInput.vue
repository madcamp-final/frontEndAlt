<style scoped>
.container img {
  max-width: 200px;
  max-height: 200px;
  display: block;
  margin: auto;
  margin-top: 20px;
  margin-bottom: 20px;
}
.title {
  font-weight: 700;
}
</style>

<template>
  <div class="container">
    <p class="title">Single Image Preview</p>
    <hr />
    <div class="large-12 medium-12 small-12 cell">
      <label
        >File Preview
        <input
          type="file"
          id="file"
          accept="image/*"
          @change="handleFileUpload($event)"
        />
      </label>
      <img v-bind:src="imagePreview" v-show="showPreview" />
      <button v-on:click="submitFile()">Submit</button>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      file: "",
      showPreview: false,
      imagePreview: "",
    };
  },

  methods: {
    /*
				Submits the file to the server
			*/
    submitFile() {
      /*
					Initialize the form data
				*/
      let formData = new FormData();

      /*
					Add the form data we need to submit
				*/
      formData.append("image", this.file);

      /*
					Make the request to the POST /single-file URL
				*/
      let objectList;
      // e.g. {class: 'backpack', x: 7, y: 33, w: 1043, h: 1361} - 이게 원소 하나
      axios
        .post("http://192.249.18.199:80/detect", formData, {
          headers: {
            "Content-Type": "multipart/form-data",
          },
        })
        .then(function (res) {
          var data = res["data"];
          return data["data"];
        })
        .catch(function () {
          console.log("FAILURE!!"); 
        }).then((datas) => {
          objectList = datas;
          console.log(objectList);
          if (datas.length == 0) {
            alert("감지된 상품이 없습니다!"); 
          }
          // var obj = objectList[1];
          // console.log(obj["class"])
        });
    },

    handleFileUpload(event) {
      this.file = event.target.files[0];
      let reader = new FileReader();

      reader.addEventListener(
        "load",
        function () {
          this.showPreview = true;
          this.imagePreview = reader.result;
        }.bind(this),
        false
      );

      if (this.file) {
        if (/\.(jpe?g|png|gif)$/i.test(this.file.name)) {
          reader.readAsDataURL(this.file);
        }
      }
    },
  },
};
</script>

<template>
  <div>
    <br/><br/><br/><br/><br/>
    <p class="title">Single</p>
    <input type=text id="email" @change="modifyId($event)" placeholder="아이디를 입력해주세요">
    <br/>
    <input type="password" id="passwd" @change="modifyPw($event)" placeholder="비밀번호를 입력주세요">
    <br/>
    <button @click="submit()">submit</button>
  </div>
</template>

<script>
import axios from "axios";
let id = "";
let pw = "";
let accessToken;
let refreshToken;
export default {
  data() {
    return {
    };
  },
  methods: {
      modifyId(event) {
          id = event.target.value;
      },
      modifyPw(event) {
          pw = event.target.value;
      },
      submit() {
          let data = {
              "email" : id,
              "password" : pw,
          }
          axios
          .post("http://54.180.160.3:8080/user/sign-in", data, {
              headers: {
                  "Content-Type": "application/json",
              },
          })
          .then((res) => res.data)
          .then((data) => data["data"])
          .then((form) => {
              accessToken = form["accessToken"];
              refreshToken = form["refreshToken"];
              if (accessToken != null && refreshToken != null){
                  console.log(accessToken);
                  console.log(refreshToken);
                  alert("캇!");
              }
          })
      },
  },
};
</script>

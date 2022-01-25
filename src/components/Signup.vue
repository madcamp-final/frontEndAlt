<template>
  <div>
    <br/><br/><br/><br/><br/>
    <p class="title">회원가입!</p>
    <input type=text id="email" @change="modifyId($event)" placeholder="아이디를 입력해주세요">
    <br/>
    <input type="password" id="passwd" @change="modifyPw($event)" placeholder="비밀번호를 입력해주세요">
    <br/>
    <input type="text" id="nickname" placeholder="닉네임을 입력해주세요" @change="modifyNn($event)">
    <br/>
    <button @click="submit()">submit</button>
  </div>
</template>

<script>
import axios from "axios";
let id = "";
let pw = "";
let nickname = "";
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
      modifyNn(event) {
          nickname = event.target.value;
      },
      submit() {
          let data = {
              "email" : id,
              "password" : pw,
              "user_name" : nickname,
          }
          axios
          .post("http://54.180.160.3:8080/user/sign-up", data, {
              headers: {
                  "Content-Type": "application/json",
              },
          })
          .then((res) => res.data)
          .then((data)=>{
              console.log(data);
              if (data["statusCode"] == 200){
                  console.log("..")
                  console.log(id)
                  console.log(pw)
                  alert("캇!")
              }
          })
      },
  },
};
</script>
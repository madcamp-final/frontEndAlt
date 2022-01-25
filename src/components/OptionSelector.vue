<template>
  <div class="keyword-selector">
    <div v-if="toggle1">
      <button id="내구성" @click="keywordHandler">내구성</button>
      <div v-if="toggleText1">
        <p>{{ sentence1 }}</p>
        <p>{{ sentence2 }}</p>
        <p>{{ sentence3 }}</p>
      </div>
    </div>
    <div v-if="toggle2">
      <button id="디자인" @click="keywordHandler">디자인</button>
      <div v-if="toggleText2">
        <p>{{ sentence1 }}</p>
        <p>{{ sentence2 }}</p>
        <p>{{ sentence3 }}</p>
      </div>
    </div>
    <div v-if="toggle3">
      <button id="상태" @click="keywordHandler">상태</button>
    </div>
    <div v-if="toggle4">
      <button id="alt1" @click="keywordHandler">{{ other1 }}</button>
      <input
        v-if="toggleText4"
        v-model="message4"
        placeholder="여기를 수정해보세요"
      />
    </div>
    <div v-if="toggle5">
      <button id="alt2" @click="keywordHandler">{{ other2 }}</button>
      <input
        v-if="toggleText5"
        v-model="message5"
        placeholder="여기를 수정해보세요"
      />
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  beforeMount() {
    this.other1 = "키워드 1";
    this.other2 = "키워드 2";
  },
  data() {
    return {
      toggle1: true,
      toggle2: true,
      toggle3: true,
      toggle4: true,
      toggle5: true,
      toggleText1: false,
      toggleText2: false,
      toggleText3: false,
      toggleText4: false,
      toggleText5: false,
      sentence1: "",
      sentence2: "",
      sentence3: "",
      other1: "",
      other2: "",
      message4: "",
      message5: "",
    };
  },
  methods: {
    keywordHandler(event) {
      const targetId = event.currentTarget.id;
      switch (targetId) {
        case "내구성":
          this.toggleText1 = !this.toggleText1;
          this.toggle2 = !this.toggle2;
          this.toggle3 = !this.toggle3;
          this.toggle4 = !this.toggle4;
          this.toggle5 = !this.toggle5;
          this.sentence1 = "내구성과 관련된";
          this.sentence2 = "어썸한 문장이 이곳으로";
          this.sentence3 = "들어오면 됩니다!";
          break;
        case "디자인":
          this.toggleText2 = !this.toggleText2;
          this.toggle1 = !this.toggle1;
          this.toggle3 = !this.toggle3;
          this.toggle4 = !this.toggle4;
          this.toggle5 = !this.toggle5;
          this.sentence1 = "디자인과 관련된";
          this.sentence2 = "어메이징한 문장이 이곳으로";
          this.sentence3 = "들어오면 됩니다!!";
          break;
        case "상태":
          console.log("상태를 선택했습니다");
          break;
        case "alt1":
          this.toggleText4 = !this.toggleText4;
          this.toggle1 = !this.toggle1;
          this.toggle2 = !this.toggle2;
          this.toggle3 = !this.toggle3;
          this.toggle5 = !this.toggle5;
          break;
        case "alt2":
          this.toggleText5 = !this.toggleText5;
          this.toggle1 = !this.toggle1;
          this.toggle2 = !this.toggle2;
          this.toggle3 = !this.toggle3;
          this.toggle4 = !this.toggle4;
          break;
      }
    },
  },
};
</script>

<style scoped>
p {
  margin: 1em 1em;
}
.state-selector {
  margin-top: 10px;
}
.keyword-selector {
  margin-top: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}
button {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;

  background: #4f95ff;
  color: #ffffff;

  margin: 0 1em;
  padding: 0.5rem 1rem;

  font-family: "Noto Sans KR", sans-serif;
  font-size: 1rem;
  font-weight: 400;
  text-align: center;
  text-decoration: none;

  border: none;
  border-radius: 4px;

  display: inline-block;
  width: auto;

  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);

  cursor: pointer;

  transition: 0.5s;
}

button:active,
button:hover,
button:focus {
  background: #267dff;
  outline: 0;
}
button:disabled {
  opacity: 0.5;
}
</style>

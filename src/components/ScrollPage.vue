<template>
  <div class="container">
    <nav class="local-nav">
      <div class="local-nav-links">
        <a href="#" class="product-name">AirSumin Pro</a>
        <a href="#">개요</a>
        <a href="#">제품사양</a>
        <a href="#">구입하기</a>
      </div>
    </nav>
    <section class="scroll-section" id="scroll-section-0">
      <h1>AirSumin Pro</h1>
      <div class="sticky-elem sticky-elem-canvas">
        <canvas id="video-canvas-0" width="1920" height="1080"></canvas>
      </div>
      <div class="sticky-elem main-message a">
        <p>
          뭔가 멋져 보이는<br />
          아무말
        </p>
      </div>
      <div class="sticky-elem main-message b">
        <p>주변 맛을 느끼게 해주는<br />주변 맛 허용 모드</p>
      </div>
      <div class="sticky-elem main-message c">
        <p>온종일 편안한<br />맞춤형 손잡이</p>
      </div>
      <div class="sticky-elem main-message d">
        <p>새롭게 입가를<br />찾아온 매혹</p>
      </div>
    </section>
    <section class="scroll-section" id="scroll-section-1">
      <p class="description">
        <strong>Lorem ipsum !</strong>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reiciendis
        adipisci beatae numquam sunt, exercitationem nihil recusandae vel harum
        iure quo suscipit blanditiis. Quos facere architecto nesciunt. Sed
        corrupti aliquid doloremque non illum eius harum similique temporibus
        maiores impedit, laborum praesentium nobis rerum quas nesciunt corporis
        veniam delectus, nisi necessitatibus assumenda. Earum, magni? Accusamus,
        doloremque. Debitis consequatur quos, similique assumenda error sunt.
        Nam aspernatur sit quibusdam facilis quis? Aut mollitia cum dolorem
        doloribus earum laborum enim vitae exercitationem officiis similique!
        Necessitatibus culpa nam ipsum aperiam? Mollitia ducimus quis maxime
        soluta tempore eius enim id culpa ut quia quisquam molestiae itaque
        repellendus consequuntur earum illo velit quam nemo eaque eveniet ipsa
        animi voluptates, dolorem laborum. Ratione molestias dolor pariatur ex,
        enim nobis perferendis, mollitia nulla natus voluptas architecto
        similique maiores nam, ullam corporis velit. Eveniet veniam quo iste
        itaque dignissimos quasi recusandae repellendus aut nam beatae, suscipit
        debitis voluptate numquam ullam laborum non assumenda rem laudantium hic
        sapiente sunt praesentium tempore repudiandae! Tempore, dolor non
        mollitia aspernatur sunt consectetur, excepturi voluptate quidem
        laboriosam repellat labore reiciendis libero dicta. Accusamus dolorum
        itaque consectetur enim delectus corporis quasi repellendus iste?
        Possimus reprehenderit ut vero, quaerat officia ipsa eius aperiam dolor
        rerum magni distinctio magnam.
      </p>
    </section>
    <section class="scroll-section" id="scroll-section-2">
      <div class="sticky-elem sticky-elem-canvas">
        <canvas id="video-canvas-1" width="1920" height="1080"></canvas>
      </div>
      <div class="sticky-elem main-message a">
        <p>
          <small>편안한 촉감</small>
          입과 하나 되다
        </p>
      </div>
      <div class="sticky-elem desc-message b">
        <p>
          편안한 목넘김을 완성하는 디테일한 여러 구성 요소들, 우리는 이를
          하나하나 새롭게 살피고 재구성하는 과정을 거쳐 새로운 수준의 머그,
          AirMug Pro를 만들었습니다. 입에 뭔가 댔다는 감각은 어느새 사라지고
          오롯이 당신과 음료만 남게 되죠.
        </p>
        <div class="pin"></div>
      </div>
      <div class="sticky-elem desc-message c">
        <p>디자인 앤 퀄리티 오브 스웨덴,<br />메이드 인 차이나</p>
        <div class="pin"></div>
      </div>
    </section>
    <section class="scroll-section" id="scroll-section-3">
      <p class="mid-message">
        <strong>Gorani Sumin</strong>
        <br />
        어디든지 언제든지 뛰어다니는
        <br />
        지치지 않는 체력.
      </p>
      <canvas class="image-blend-canvas" width="1920" height="1080"></canvas>
      <p class="canvas-caption">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eveniet at
        fuga quae perspiciatis veniam impedit et, ratione est optio porro.
        Incidunt aperiam nemo voluptas odit quisquam harum in mollitia. Incidunt
        minima iusto in corporis, dolores velit. Autem, sit dolorum inventore a
        rerum distinctio vero illo magni possimus temporibus dolores neque
        adipisci, repudiandae repellat. Ducimus accusamus similique quas earum
        laborum. Autem tempora repellendus asperiores illum ex! Velit ea
        corporis odit? Ea, incidunt delectus. Sapiente rerum neque error
        deleniti quis, et, quibusdam, est autem voluptate rem voluptas. Ratione
        soluta similique harum nihil vel. Quas inventore perferendis iusto
        explicabo animi eos ratione obcaecati.
      </p>
    </section>
    <footer class="footer">2022 &copy; nothing here</footer>
  </div>
</template>

<style scoped>
p {
  line-height: 1.6;
}

a {
  color: rgb(29, 29, 31);
  text-decoration: none;
}

.container {
  /* iPhone 가로 스크롤 방지 */
  overflow-x: hidden;
}
.local-nav {
  position: absolute;
  top: 45px;
  left: 0;
  z-index: 11;
  width: 100%;
  height: 52px;
  padding: 0 1rem;
  border-bottom: 1px solid #ddd;
}

.local-nav-stick .local-nav {
  position: fixed;
  top: 0;
  background: rgba(255, 255, 255, 0.1);
  -webkit-backdrop-filter: saturate(180%) blur(15px);
  -moz-backdrop-filter: saturate(180%) blur(15px);
  -o-backdrop-filter: saturate(180%) blur(15px);
  backdrop-filter: saturate(180%) blur(15px);
}
.local-nav-links {
  display: flex;
  align-items: center;
  max-width: 1000px;
  height: 100%;
  margin: 0 auto;
}

.local-nav-links .product-name {
  margin-right: auto;
  font-size: 1.4rem;
  font-weight: bold;
}

.local-nav-links a {
  font-size: 0.8rem;
}

.local-nav-links a:not(.product-name) {
  margin-left: 2em;
}

.scroll-section {
  position: relative;
  padding-top: 50vh;
}

#scroll-section-0 h1 {
  position: relative;
  top: -10vh;
  z-index: 5;
  font-size: 4rem;
  text-align: center;
}

.main-message {
  display: flex;
  align-items: center;
  justify-content: center;
  top: 35vh;
  margin: 5px 0;
  height: 3em;
  font-size: 2.5rem;
  opacity: 0;
}

.main-message p {
  font-weight: bold;
  text-align: center;
  line-height: 1.2;
}

.main-message small {
  display: block;
  margin-bottom: 0.5em;
  font-size: 1.2rem;
}

#scroll-section-2 .main-message {
  font-size: 3.5rem;
}

.description {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 1rem;
  font-size: 1.2rem;
  color: #888;
}

.description strong {
  float: left;
  margin-right: 0.2em;
  font-size: 3rem;
  color: rgb(29, 29, 31);
}

.desc-message {
  width: 50%;
  font-weight: bold;
  opacity: 0;
}
.pin {
  width: 1px;
  height: 100px;
  background: rgb(29, 29, 31);
}

#scroll-section-2 .b {
  top: 10%;
  left: 40%;
}
#scroll-section-2 .c {
  top: 15%;
  left: 45%;
}

.mid-message {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 1rem;
  font-size: 2rem;
  color: #888;
}

.mid-message strong {
  color: rgb(29, 29, 31);
}

.canvas-caption {
  max-width: 1000px;
  margin: -30rem auto 0;
  text-align: center;
  padding: 0 1rem;
  font-size: 1.2rem;
  color: #888;
}

.footer {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 4rem;
  color: white;
  background: rgb(78, 78, 78);
}
.sticky-elem {
  display: none;
  position: fixed;
  left: 0;
  width: 100%;
}

#show-scene-0 #scroll-section-0 .sticky-elem,
#show-scene-1 #scroll-section-1 .sticky-elem,
#show-scene-2 #scroll-section-2 .sticky-elem,
#show-scene-3 #scroll-section-3 .sticky-elem {
  display: block;
  will-change: transform, opacity;
}

.sticky-elem-canvas {
  top: 0;
  height: 100%;
}

.sticky-elem-canvas canvas {
  position: absolute;
  top: 50%;
  left: 50%;
}

#scroll-section-3 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.image-blend-canvas.sticky {
  position: fixed;
  top: 0;
}

.loading {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;
  background: white;
  opacity: 0;
  transition: 0.5s;
}

.before-load .container {
  display: none;
}
.before-load .loading {
  opacity: 1;
}

@keyframes loading-spin {
  100% {
    transform: rotate(360deg);
  }
}

@keyframes loading-circle-ani {
  0% {
    stroke-dashoffset: 157;
  }
  75% {
    stroke-dashoffset: -147;
  }
  100% {
    stroke-dashoffset: -157;
  }
}

.loading-circle {
  width: 54px;
  height: 54px;
  animation: loading-spin 3s infinite;
}

.loading-circle circle {
  stroke: black;
  stroke-width: 4;
  /* getTotalLength()로 stroke의 길이를 얻어 올 수 있음 */
  stroke-dasharray: 157;
  stroke-dashoffset: 0;
  fill: none;
  animation: loading-circle-ani 1s infinite;
}

/* .loading-circle:hover circle {
  stroke-dashoffset: -157;
} */

@media (min-width: 1024px) {
  #scroll-section-0 h1 {
    font-size: 9vw;
  }
  .main-message {
    font-size: 4vw;
  }
  .description {
    padding: 0;
    font-size: 2rem;
  }
  .description strong {
    font-size: 6rem;
  }
  #scroll-section-2 .main-message {
    font-size: 6vw;
  }
  .main-message small {
    font-size: 1.5vw;
  }
  .desc-message {
    width: 20%;
  }
  #scroll-section-2 .b {
    top: 20%;
    left: 53%;
  }
  #scroll-section-2 .c {
    left: 55%;
  }
  .mid-message {
    width: 1000px;
    padding: 0;
    font-size: 4vw;
  }
  .canvas-caption {
    margin-top: -8rem;
    padding: 0;
    font-size: 2rem;
  }

  .scroll-section {
    padding-top: 50vh;
  }
}
</style>

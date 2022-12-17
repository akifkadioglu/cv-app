<template>
  <div>
    <div class="text-wrapper">
      <div class="background"></div>
    </div>
    <div class="text-wrapper">
      <div class="text mb-3">
        <span style="font-size: 30px; color: white; text-transform: uppercase">
          Akif Kadioglu
        </span>
      </div>
      <div class="text">
        <span style="font-size: 15px; color: #e4bb68">console</span>
        <span style="font-size: 15px; color: white">.</span>
        <span style="font-size: 15px; color: #e06c75">log</span>
        <span style="font-size: 15px; color: #e4bb68">("</span>
        <span style="font-size: 21px; color: #61afef">{{
          $t("developer-type")
        }}</span>
        <span style="font-size: 22px; color: white">!</span>
        <span style="font-size: 15px; color: #e4bb68">")</span>
      </div>
    </div>

    <div class="wrapper">
      <div class="link_wrapper">
        <router-link :to="{ name: 'Home' }" class="button-name">
          {{ $t("intro") }}
        </router-link>
        <div class="icon">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 268.832 268.832">
            <path
              d="M265.17 125.577l-80-80c-4.88-4.88-12.796-4.88-17.677 0-4.882 4.882-4.882 12.796 0 17.678l58.66 58.66H12.5c-6.903 0-12.5 5.598-12.5 12.5 0 6.903 5.597 12.5 12.5 12.5h213.654l-58.66 58.662c-4.88 4.882-4.88 12.796 0 17.678 2.44 2.44 5.64 3.66 8.84 3.66s6.398-1.22 8.84-3.66l79.997-80c4.883-4.882 4.883-12.796 0-17.678z"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.background {
  background: #282c34;
  height: 250px;
  width: 600px;
}
@import url("https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@100;500&display=swap");
* {
  margin: 0;
  padding: 0;
}
.text-wrapper {
  position: fixed;
  left: 50%;
  top: 40%;
  transform: translate(-50%, -50%);
}
.text {
  font-family: JetBrains Mono, monospace;
}

@keyframes shine {
  0% {
    background-position-x: -500%;
  }
  100% {
    background-position-x: 500%;
  }
}
.wrapper {
  position: fixed;
  bottom: 100px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.link_wrapper {
  position: relative;
}
.button-name {
  color: rgb(255, 255, 255);
}
a {
  display: block;
  width: 250px;
  height: 50px;
  line-height: 50px;
  font-weight: bold;
  text-decoration: none;
  background: #333;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 1px;
  border: 3px solid #333;
  transition: all 0.35s;
}

.icon {
  width: 50px;
  height: 50px;
  border: 3px solid transparent;
  position: absolute;
  transform: rotate(45deg);
  right: 0;
  top: 0;
  z-index: -1;
  transition: all 0.35s;
}

.icon svg {
  width: 30px;
  position: absolute;
  top: calc(50% - 15px);
  left: calc(50% - 15px);
  transform: rotate(-45deg);
  fill: #e06c75;
  transition: all 0.35s;
}

a:hover {
  width: 200px;
  border: 3px solid #e06c75;
  background: transparent;
  color: #e06c75;
}

a:hover + .icon {
  border: 3px solid #e06c75;
  right: -25%;
}
</style>

<template>
  <div class="loginContainer">
    <img class="mainBackground" src="./../../assets/images/news-and-promos-bg.jpg"/>
    <!-- <img class="movingFigures" src="./../../assets/images/201805150822-201805090723-news-and-promos-avatars.png"> -->
    <img class="movingFigures" src="./../../assets/images/201805150822-201805141209-total-jackpot.png">    
    <LoginForm/>
  </div>
</template>

<script>

import LoginForm from "./LoginForm"

export default {
    name: 'loginContainer',
    components: {
      LoginForm
    }
    
}
</script>

<style lang="scss">

.loginContainer {
//     width: 100%;
//     height: 64%;
//     background-image: url('./../../assets/images/dust-bg.jpg');
//     background-position: center center;
//     background-size: 100% 100%;
//     background-repeat: no-repeat;
width: 100%;
    height: 100%;
}
.mainBackground {
  width: 100%;
  height: 100%;
}
// .movingFigures {
//     width: 82%;
//     height: 74%;
//     position: absolute;
//     top: 12%;
//     left: 9%;
//     // animation: flyingFigures 6s infinite;
// }

// .loginForm {
//     position: absolute;
//     top: 26%;
//     width: 38%;
//     left: 31%;
//     height: 39%;
//     background: rgba(1, 1, 1, 0.5);
// }

.movingFigures {
    width: 66%;
    height: 65%;
    position: absolute;
    top: 37%;
    left: 10%;
}



@keyframes flyingFigures {
  0% {
    transform: translateY(0%);
  }
  50% {
    transform: translateY(-5%);
  }
  100% {
    transform: translateY(0%);
  }
}
</style>
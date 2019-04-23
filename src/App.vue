<template>
  <div class="container">
    <Header/>
    <LoginContainer/>
    <GamePodsContainer/>
    <!-- <MovingFiguresSection/> -->
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header';
import LoginContainer from './components/LoginContainer/LoginContainer';
import GamePodsContainer from './components/GamePodsContainer';
// import MovingFiguresSection from './components/MovingFiguresSection';
import Footer from './components/Footer';
export default {
  components: {
    Header,
    LoginContainer,
    GamePodsContainer,
    // MovingFiguresSection,
    Footer
  }
}
</script>

<style lang="scss">

html {
    width: 100%;
    height: 100%;
}

body {
  width: 100%;
  height: 100%;
  overflow-y: scroll;
  margin: 0;
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  color: white;
}
.container {
    width: 100%;
    height: 100%;
}
// .slide-enter-active{
//   animation: slide-in 300ms ease-out forwards;
// }
// slide-leave-active {
//   animation: slide-out 300ms ease-out forwards;
// }

// @keyframes slide-in {
//   from{
//     transform: translateY(-30px);
//     opacity: 0;
//   }
//   to {
//     transform: translateY(0);
//     opacity: 1;
//   }
// }
// @keyframes slide-out {
//   from{
//     transform: translateY(0);
//     opacity: 1;
//   }
//   to {
//     transform: translateY(-30);
//     opacity: 0;
//   }
// }

@media screen and (max-width: 560px) {
  ul {
    display: flex;
    justify-content: center;
    .logo{
      width: 84%;
      a {
        width: 71%;
    }
    
    }
    .navigationLinks {
      width: 16%;
    }
    .navigationLink {
      display: none;
    }
    .navigationLink:last-child {
    width: 100%;
}
  }
  .movingFigures {
    display: none;
  }

  .loginForm {
    
    width: 90%;
    left: 5%;
    height: 70%;
    z-index: 1;
    input,
    button {
      height: 10%;
    }
    .readyToPlay {
      font-size: 1.5em;
    }
    
  }

  .input[type="checkbox"] {
      width: 6%;
      height: 33%;
    }

  .gamePodsSection {
    flex-wrap: wrap;
    .gamePod {
      width: 30%;
      height: 48%;
    }
  }

  .footer {
    height: 57%;
    top: 10%;
    .footerIcons {
          width: 85%;
          height: 13%;
          background-position: 50% 58%;
    }
  }

}
@media screen and (min-width: 601px) and (max-width: 1024px) {
  .logo {
    width: 30%;
  }
  .navigationLinks {
    font-size: 0.8em;
    width: 55%;
  }
  .navigationLink {
    width: 21%;
    margin-right: 7%;
  }
  .movingFigures {
    height: 50%;
    top: 49%;
    left: 3%;
  }
  .loginForm {
    width: 44%;
    left: 53%;
    height: 55%;
    z-index: 1;
    input, 
    button {
      height: 8%;
    }
  }
  .gamePodsSection {
    height: 13%;
  }
  .footer {
    top: 2%;
    height: 22%;
  }
  .footerIcons {
    width: 100%;
    height: 40%;
    background-position: 9% 54%;
  }
}

@media screen and (min-width: 768px) {
  .footerIcons {
    width: 100%;
    height: 29%;
    background-position: 13% 58%;
} 
}

@media screen and (width: 1024px) {
  .loginForm {
    z-index: 1;
  }
  .footerIcons {
    width: 94%;
    height: 42%;
    background-position: 15% 58%;
}
.footerText {
    height: 50%;
}
}

@media screen and (width: 1024px) and (orientation: portrait){
  .footerIcons {
      width: 92%;
      height: 24%;
      background-position: 19% 58%;
  }

}

@media screen and (width: 1366px) {
  .loginForm {
    height: 65%;
    width: 32%;
    left: 66%;
    z-index: 1;
    button, 
    input {
      height: 8%;
    }
      
  }
  .footerIcons {
    height: 50%;
  }
}

@media screen and (min-width: 500px) and(max-width: 1020px) and (orientation: landscape) {
  .loginForm {
    height: 87%;
  }
  .gamePodsSection {
    height: 22%;
  }

  .footer {
    top: 11%;
    height: 37%;
}
.footerIcons {
    width: 94%;
    height: 45%;
}
}

@media screen and (width: 568px) and (orientation: landscape) {
  body {
    font-size: 0.5em;
  }
  .loginForm {
    height: 75%;  
    z-index: 1;
    font-size: 0.8em;
    width: 29%;
    input, 
    button {
      height: 9%;
    }
  }
  .gamePodsSection {
    height: 22%;
  }

  .footer {
    top: 11%;
    height: 54%;
}
.footerIcons {
    width: 96%;
    height: 32%;
    background-position: 9% 50%;
}
}

</style>


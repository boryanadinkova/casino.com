<template>
  <div class="footer">
    <div class="footerIcons">
      <!-- <div class="footerIcon" v-for="(footerIcon, index) in footerIcons" :key="(footerIcon, index)" :class="`icon${index+1}`"></div> -->
    </div>
    <div class="footerText">
      <div class="footerRow">Casino.com is licensed and regulated to offer online casino gaming services under the jurisdiction of Gibraltar. © 2019 Casino.com is an internationally registered trademark. </div>
      <div class="footerRow">Casino.com is operated by ONISAC Ltd of Suite 732 Europort, Gibraltar under a license issued by the Gibraltar Licensing Authority, RGL No.053 and regulated by the Gibraltar Gambling Commissioner.</div> 
      <div class="footerRow">Only players above the age of 18 are permitted to play our games. www.gambleaware.co.uk </div>
    </div>
  </div>
</template>

<script>

export default {
    name: 'Footer',
    data(){
      return{
        footerIcons: 9
      }
    }
    
}
</script>

<style lang="scss">

.footer {
    position: relative;
    top: 10%;
    width: 100%;
    height: 20%;
    background: #E3E2E2;
    color: #B7B2AE;
    font-size: 0.8em;
    font-weight: 600;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;

    a {
      color: inherit; 
      text-decoration: inherit;
    }
}

.footerIcons {
  width: 90%;
  height: 40%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background: url('./../assets/images/footer-sprite-v4.png');
  background-position: -108% 50%;
  background-repeat: no-repeat;  
}

.icon1 {
  background: url('./../assets/images/footer-sprite-v4.png');
  display: inline-block;
  height: 20px;
  width: 20px;
  background-position: -20px 0px;
}

.icon2 {
  
}

.icon3 {
  
}

.icon4 {
  
}

.icon5 {
  
}

.icon6 {
  
}

.icon7 {
  
}

.icon8 {
  
}

.icon9 {
  
}
.footerText {
    width: 100%;
    height: 60%;
    display: flex;
    flex-direction: column;
    .footerRow{
      display: flex;
      justify-content: center;
      }
}
</style>
<template>
  <div class="gamePodsSection">
    <img class="gamePod" v-for="(pod, index) in pods" :key="(pod, index)" :class="`pod${index+1}`"/>
  </div>
</template>

<script>

export default {
    name: 'gamePodsSection',
    data() {
      return {
        pods: ['glr2.jpg','gpas-secagent-pop.jpg','gpas-squeen-pop.jpg','pop-bp-wlflgnmgw-blp.jpg','pop-dragonsluck-rdt.jpg']
      }
    }
    
}
</script>

<style lang="scss">

  .gamePodsSection {
    position: absolute;
    top: 89%;
    width: 100%;
    height: 21%;
    background: url('./../assets/images/dust-bg.jpg');
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .gamePod {
    width: 16%;
    height: 94%;
    border-radius: 0.4em;
  }

  .pod1 {
    background: url('./../assets/images/glr2.jpg');
    background-position: center center;
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }

  .pod2 {
    background: url('./../assets/images/gpas-secagent-pop.jpg');
    background-position: center center;
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }

  .pod3 {
    background: url('./../assets/images/gpas-squeen-pop.jpg');
    background-position: center center;
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }

  .pod4 {
    background: url('./../assets/images/pop-bp-wlflgnmgw-blp.jpg');
    background-position: center center;
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }
  .pod5 {
    background: url('./../assets/images/pop-dragonsluck-rdt.jpg');
    background-position: center center;
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }


</style>
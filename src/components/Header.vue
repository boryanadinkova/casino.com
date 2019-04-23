<template>
  <!--<nav class="navbar navbar-default">
  <div class="container-fluid">
   <div class="navbar-header">
       
      <router-link to = "/" class = "navbar-brand">Stock Trader</router-link>
    </div>
    <div class="collapse navbar-collapse">
      <ul class="nav navbar-nav">
          <router-link to = "/portfolio" activeClass = "active" tag = "li"><a>Portfolio</a></router-link>
          <router-link to = "/stocks" activeClass = "active" tag = "li"><a>Stocks</a></router-link>
      </ul> 
      <strong class="navbar-text navbar-right">Funds: {{ funds | currency }}</strong>      
      <ul class="nav navbar-nav navbar-right">
        <li><a href="#" @click = "endDay">End Day</a></li>
        <li class="dropdown" :class = "{open: dropdownOpen}" @click = "dropdownOpen = !dropdownOpen">
          <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Save & Load <span class="caret"></span></a>
          <ul class="dropdown-menu">
            <li><a href="#" @click = "saveData">Save Data</a></li>
            <li><a href="#" @click = "loadData">Load Data</a></li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</nav>-->

<div class="header">
  <ul>
    <li class="logo"><a href="http://www.casino.com/"><img src="./../assets/images/casino-com-logo.png"></a></li>
    <div class="navigationLinks">
      <div class="navigationLink" v-for="link in links" :key="link">
        
        {{link}}
      </div>
    </div>
  </ul>

</div>
</template> 
<script>
export default {
  name: 'Header',
  data(){
    return {
      links: ['GAMBLING COMMISSION', 'Secure Payments', 'Data protected', 'Login']
    }
  },
  computed: {
    funds() {
      return this.$store.getters.funds;
    }
  }, 
  methods: {
    
  }
}
</script>
<style lang="scss">
.header {
  background: rgba(1,1,1,0.3);
  position: fixed;
  width: 100%;
  height: 10%;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 100%;
}

.logo {
    width: 20%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    a {
      width: 90%;
      img {
        width: 100%;
      }
    }
}
.navigationLinks {
  display: flex;
  width: 40%;
  height: 100%;
  cursor:pointer;
}

.navigationLink {
    width: 17%;
    height: 100%;
    margin-right: 11%;
    display: flex;
    align-items: center;
}


.navigationLink:last-child {
    width: 16%;
    height: 100%;
    background: #EC8B2E;
    margin-right: 0%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}


</style>
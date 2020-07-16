<template>
<main>
  <Header/>
  <Receive/>
  <Expand/>
  <Process/>
  <Landing/>
  <Advertising/>
  <Marketing/>
  <Portfolio/>
  <Team/>
  <Clients/>
  <Footer/>
</main>
</template>
<style>
main {
  margin: 0;
  padding: 0;
}
</style>
<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Receive from '@/components/Receive.vue'
import Expand from '@/components/Expand.vue'
import Process from '@/components/Process.vue'
import Landing from '@/components/Landing.vue'
import Advertising from '@/components/Advertising.vue'
import Marketing from '@/components/Marketing.vue'
import Portfolio from '@/components/Portfolio.vue'
import Team from '@/components/Team.vue'
import Clients from '@/components/Clients.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'Home',
  components: {
    Header,
    Receive,
    Expand,
    Process,
    Landing,
    Advertising,
    Marketing,
    Portfolio,
    Team,
    Clients,
    Footer
  }
}
</script>

<template>
  <main>
    <px-header :links="links" />
    <router-view class="container px-5 sm:px-20 py-20 flex justify-center " />
    <px-footer />
  </main>
</template>

<script>
import PxHeader from '@/components/PxHeader.vue';
import PxFooter from '@/components/PxFooter';
export default {
  name: 'App',
  components: { PxHeader, PxFooter },
  data() {
    return {
      links: [
        {
          title: 'BTC',
          to: { name: 'coin-detail', params: { id: 'bitcoin' } }
        },
        {
          title: 'ETH',
          to: { name: 'coin-detail', params: { id: 'ethereum' } }
        },
        {
          title: 'USDT',
          to: { name: 'coin-detail', params: { id: 'tether' } }
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  oveflow-x: hidden;
}
</style>

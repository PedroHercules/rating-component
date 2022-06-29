<template>
  <main>
    <Rate v-if="currentComponent == 'Rate'" @click="changeComponent"/>
    <ThankYou v-if="currentComponent == 'ThankYou'" score/>
  </main>
</template>

<script>
  import Rate from '../components/Rate.vue';
  import ThankYou from '../components/ThankYou.vue';
  export default {
    data () {
      return {
        currentComponent: 'Rate'
      }
    },
    components: {
      Rate,
      ThankYou
    },
    methods: {
      changeComponent(component){
        this.currentComponent = component;
      }
    }
  }
</script>

<style>
  body{
    display: flex;
    align-items: center;
    justify-content: center;
  }

  main{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 40px;
    margin: 0 auto;
    width: 47%;
    height: 400px;
    padding: 0 30px;
    border-radius: 2rem;
    background: hsl(213, 19%, 18%);
  }

  @media only screen and (min-width: 501px) and (max-width: 600px) {
    body{
      padding: 20px;
    }
    main{
      width: 80%;
    }
  }
  

  @media only screen and (max-width: 500px) {
    body{
      padding: 20px;
    }
    main{
      width: 100%;
    }
  }
</style>
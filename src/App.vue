<template>
  <div id="app">
    
    <HeadProject :navBarHeader="navBar"/>
    <MainProject/>
    <CardsEmployee/>
    <WorkWithus />
    
  </div>
</template>

<script>
import HeadProject from './components/HeadProject.vue'
import MainProject from './components/MainProject.vue'
import CardsEmployee from './components/CardsEmployee.vue'
import WorkWithus from './components/WorkWithus.vue';


export default {
  name: 'App',
  components: {
    MainProject,
    HeadProject,
    CardsEmployee,
    WorkWithus
  },

  data() {
    return {
      navBar: [
        {
          name: "Home",
          link: "/",
        },
        {
          name: "Service",
          link: "/Service",
        },
        {
          name: "Why Us",
          link: "/WhyUS",
        },
        {
          name: "Case Studies",
          link: "/Service",
        },
        {
          name: "About",
          link: "/About",
        },
        {
          name: "Blog",
          link: "/Blog",
        },
      ],
    };
  },
};
</script>







<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  

}
</style>

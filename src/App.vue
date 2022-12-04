<template>
  <div id="app">

    <HeadProject :navBarHeader="navBar" />
    <MainProject :section="section" :brands="brands" />
    <CardsEmployee :cards="cards" />
    <WorkWithus :build="build" :awards="awards" />
    <ConsultantWork/>

  </div>
</template>

<script>
import HeadProject from './components/HeadProject.vue'
import MainProject from './components/MainProject.vue'
import CardsEmployee from './components/CardsEmployee.vue'
import WorkWithus from './components/WorkWithus.vue';
import ConsultantWork from './components/ConsultantWork.vue';


export default {
  name: 'App',
  components: {
    MainProject,
    HeadProject,
    CardsEmployee,
    WorkWithus,
    ConsultantWork
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
      section: [
        {
          image: "pic1.png",
          titolosmall: "Business Growth",
          titolo: "Increase Brand Awareness",
        },
        {
          invert: "rotate:180deg",
          image: "pic2.png",
          titolosmall: "Investors In People",
          titolo: "In-House Sales Training",

        },
        {
          image: "pic3.png",
          titolosmall: "Social Media Analysis",
          titolo: "Harness Your Social Proof"
        }

      ],
      brands: ["abstract.png", "cglobal.png", "next.png", "hemisferio.png", "spaces.png", "digitalbox.png"],
      cards: [
        {
          image: 'case-studies-1-400x450.jpg',
          about: 'How Spaces attracted five million visitors by improving the content',
          score: '200%',
          role: 'Higher revenue from digital'
        },
        {
          image: 'case-studies-4-400x450.jpg',
          about: 'Creativity helped Hemisferio to increase their brand reach vertically',
          score: '10x',
          role: 'Sales increase with the same ad spend'
        }, {
          image: 'case-studies-6-400x450.jpg',
          about: 'How DigitalBox used AI-powered data insight to boost sales',
          score: '3-year',
          role: 'Partnership with Avada Consultant'
        }
      ], build: [
        {
          titolo: 'We Build Relationship',
          contenuto: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante fin leo. Integer consectetur luctus dui id convallis.',
          icon: 'award-d.png',
          titoloicon: 'Accountability',
          contenutoicon: ' et mauris veldcec ante fincdcslkkc leo ger consectetur lu'
        },
        {
          titolo: 'Proprietary Process',
          contenuto: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante fin leo. Integer consectetur luctus dui id convallis.',
          icon: 'award-d.png',
          titoloicon: 'Transparency',
          contenutoicon: 'Vestibulum ftu bvece et mauris vel ante fin leo'
        },
        {
          contenuto: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante fin leo. Integer consectetur luctus dui id convallis.',
          icon: 'award-d.png',
          titoloicon: 'Investment',
          contenutoicon: 'lorem aveckncer ac leo nunante fin leo'
        }],
      awards: [
        {
          iconwin: "award-a-200x191.png",
          color: "background-color:aliceblue",
          contain: "Winner Seo Master MAGT Smart Start Award 2017"
        },
        {
          iconwin: "award-b-200x191.png",

          contain: "Top Social Media Agencies Next Partner 2018"
        },
        {
          iconwin: "award-c-200x191.png",
          color: "background-color:aliceblue",
          contain: "10 Fastest Growing Abstract Solution Providers 2019"
        },
        {
          iconwin: "award-d.png",
          color: "background-color:aliceblue",
          contain: "National Excellence Agencie Award Winner 2020"
        }

      ]



    }

  }
}


</script>







<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;


}
</style>

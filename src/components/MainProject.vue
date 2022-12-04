<template>
  <div class="section">

    <div class="sezioni flex" v-for='(elem, index) in section' :style="`${elem.invert}`" :key="index">

      <img class="pics" :style="`${elem.invert}`" :src="require(`../assets/${elem.image}`)" alt="#">

      <div :style="`${elem.invert}`" class="sezionip">
        <h4>{{ elem.titolosmall }}</h4>
        <h1>{{ elem.titolo }}</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor placerat luctus. Nullam sit amet ante sed
          orci convallis gravida et at massa.</p>
        <button>Get a consultation</button>
      </div>

    </div>
    <div class="section-foot">
      <h1>Some Brands We Work With</h1>
      <h4>Quisque aliquet, libero consequat elementum convallis.</h4>
    </div>
    <div class="brands flex">
      <div v-for='foto in brands' :key="foto">
        <img class="brandslogo" :src="require(`../assets/${foto}`)">
      </div>
    </div>
    <div class="contact flex">

      <div class="flex">
        <img src="../assets/marketing-expert-cta.png">
        <div>
          <h2>Sandy Reiff </h2><span>Marketing Consultant Expert</span>
        </div>
      </div>
      <h1>Drive Leads and Sales with Avada</h1>
      <button class="bt"><i class="fa-solid fa-phone"> </i><span class="tel">(555)802-1234 </span></button>

    </div>
  </div>
</template>

<script>


export default {
  name: 'MainProject',
  props: ['section', 'brands']

}</script>

<style lang="scss">
button {
  padding: 10px;
  height: 40px;
  border-style: none;
  border-radius: 10px;
  color: white;
  background-color: orange;

  &:hover {
    background-color: #f76210;
  }
}

@keyframes mymove {
  0% {
    transform: translate(0, 0) rotate(0deg);
  }

  25% {
    transform: translate(5px, 5px) rotate(5deg);
  }

  50% {
    transform: translate(0, 0) rotate(0eg);
  }

  75% {
    transform: translate(-5px, 5px) rotate(-5deg);
  }

  100% {
    transform: translate(0, 0) rotate(0deg);
  }
}

.pics {
  width: 50%;
  height: 40%;




  &:hover {
    animation: mymove 5s infinite;
  }
}


.sezioni {
  padding: 5% 15%;
}

.sezionip {font-size: larger;
  width: 40%;

  &:hover {
    transform: translateY(15%);
    transition: all .9s ease-in-out;
  }
}

.section {
  padding-top: 10%;
}

.section-foot {
  text-align: center;

}

.brands {
  padding-top: 2%;
  margin: 2% 10%;
}

.contact {
  margin: 0 auto;
  width: 73%;
  height: 63px;
  border: 1px solid rgb(213, 213, 213);
  border-radius: 10px;
  padding: 2px 7px;

}

.brandslogo {
  width: 150px;
}

.contact img {
  width: 60px;
  border-radius: 50%;
  margin-right: 15px;
}

.contact h1,
h2,
span {
  margin: 0;
  font-size: smaller;
}

.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.bt {
  color: #f8fcff;
  background-color: #fcb791;
  width: 15%;
}
</style>

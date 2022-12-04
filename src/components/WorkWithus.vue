<template>
    <div>           
    <div class="work-space">
        <div class="flex work">
            <div>
                <h1>We Boost Our Clients' Bottom Line by Optimizing Their Growth Potential.</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, reiciendis.lorem ipsum dolor cvgs</p>
                <button>Why Work With Us</button>
            </div>
            <img src="../assets/we-boost-our-clients-400x366.jpg">


        </div>
        <div class="flex work-ic" v-for='(elem, index) in build' :key='index'>
            <div class="work-left">
                <h4>{{ elem.titolo }}</h4>
                <p>{{ elem.contenuto }}</p>
            </div>
            <div class="flex work-right">
                <img class="icon" :src="require(`../assets/${elem.icon}`)">
                <div class="iconandcontenut">
                    <h5>{{ elem.titoloicon }}</h5>
                    <span>{{ elem.contenutoicon }}</span>
                </div>
            </div>

        </div> </div>
        <div class="premium">
            <h1>Awards</h1>
            <div class="flex">
                <a v-for='(award, index) in awards' :key='index'>
                    <img :style="`${award.color}`" class="boxicon" :src="require(`../assets/${award.iconwin}`)">
                    <p>{{award.contain}}</p>

                </a>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: 'WorkWithus',
    props:['build','awards']
}
</script>


<style lang="scss" scoped>
*{background-color: aliceblue;
padding-top:1%;}
.work {
    margin: 0 20%;
    justify-content: space-between;
}
.boxicon{width:20%;}
.icon {
    width: 50px;
}

.work-ic {
    margin: 0 20%;
}

.work-right {
    width: 50%;
}

.iconandcontenut {
    width: 80%;
}

.work-left {
    width: 70%;
}

.flex {
    justify-content: center !important;
    align-items: center;
}

.flex >a {align-items:center;}

h5 {
    margin: 0;
}
.premium{text-align: center;
margin:2% 10%;}
img:hover {filter: blur(3px);
  filter: grayscale(2);
  filter: saturate(3.2);}
</style>
<template>
    <div class="work-space">
        <div class="flex work">
            <div>
                <h1>We Boost Our Clients' Bottom Line by Optimizing Their Growth Potential.</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex, reiciendis.lorem ipsum dolor cvgs</p>
                <button>Why Work With Us</button>
            </div>
            <img src="../assets/we-boost-our-clients-400x366.jpg">


        </div>
        <div class="flex work-ic" v-for='(elem ,index) in build' :key='index'>
            <div class="work-left"><h4>{{elem.titolo}}</h4>
            <p>{{elem.contenuto}}</p></div>
            <div class="flex work-right">
                <img class="icon" :src="require(`../assets/${elem.icon}`)">           
                <div class="iconandcontenut">
                    <h5>{{elem.titoloicon}}</h5>
                    <span>{{elem.contenutoicon}}</span>
                </div>
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'WorkWithus',
    data() {
        return {
            build: [
                {
                    titolo: 'We Build Relationship',
                    contenuto: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante fin leo. Integer consectetur luctus dui id convallis.',
                    icon: 'award-d.png',
                    titoloicon: 'Accountability',
                    contenutoicon: ' et mauris vel ante fin leo ger consectetur lu'
                },
                {
                    titolo: 'Proprietary Process',
                    contenuto: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante fin leo. Integer consectetur luctus dui id convallis.',
                    icon: 'award-d.png',
                    titoloicon: 'Transparency',
                    contenutoicon: 'Vestibulum et mauris vel ante fin leo'
                },
                {
                    contenuto: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante fin leo. Integer consectetur luctus dui id convallis.',
                    icon: 'award-d.png',
                    titoloicon: 'Investment',
                    contenutoicon: 'r ac leo nunante fin leo'
                }] }


             
        
    }

    }
</script>


<style lang="scss" scoped>
.work {
    margin: 0 20%;
    justify-content: space-between;
}
.icon{width: 40px;}
.work-ic{margin:0 20%;}
.work-right,.iconandcontenut{width:50%;}
.work-left{width:60%;}
.flex{justify-content:flex-start!important;}
</style>
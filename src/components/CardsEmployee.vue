<template>
    <div>
        <h1>Trusted by Leading Organisations</h1>
        <div class="flex cards">
            <div v-for="(person, index) in cards" :key="index">
                <img :src="require(`../assets/${person.image}`)">
             

                <p>{{ person.about }}</p>
                <h2>{{ person.score }}</h2>
                <span>{{ person.role }}</span>
            </div>
        
        </div>
        <div class="button-center">                                     
        <button>Read More Case Studies</button></div>



    </div>
</template>
<script>



export default {
    name: 'CardsEmployee',
    data() {
        return {
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
            ]

        }
    }
}
</script>


<style scoped lang="scss">

.flex {
    display: flex;
    justify-content: space-between;

}

span {
    font-size: smaller;
}

p {
    font-size: large;
    &:hover {color:#eb621f;}
}

h1 {
    text-align: center;
    margin: 7%;
}

h2 {
    font-size: 40px;
    margin: 0;
    
}

.cards {
    margin: 0 8%;
}
.button-center {text-align: center; padding:2%;}
img:hover {filter:sepia(50%);
    

}

// effetto scapa

// :hover{
//     transform: translateX(-100%);
//  transition: all .3s ease-in-out;}

</style>
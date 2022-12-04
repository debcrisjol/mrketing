<template>
    <div>
        <h1>Trusted by Leading Organisations</h1>
        <div class="flex cards">
            <div v-for="(person, index) in cards" :key="index">
                <img :src="require(`../assets/${person.image}`)">


                <p><b> {{ person.about }}</b></p>
                <h2>{{ person.score }}</h2>
                <span>{{ person.role }}</span>
            </div>

        </div>
        <div class="button-center">
            <button>Read More Case Studies</button>
        </div>



    </div>
</template>
<script>



export default {
    name: 'CardsEmployee',
    props: ['cards'],
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
    font-size:larger;

    &:hover {
        color: #eb621f;
    }
}

h1 {
    text-align: center;
    margin: 4%;
}

h2 {
    font-size: 40px;
    margin: 0;

}

.cards {
    margin: 0 8%;
}

.button-center {
    text-align: center;
    padding: 2%;
}

img:hover {
    filter: sepia(30%)  brightness(120%);


}

// effetto scapa

// :hover{
//     transform: translateX(-100%);
//  transition: all .3s ease-in-out;}
</style>
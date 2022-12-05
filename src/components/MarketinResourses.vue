<template>
    <div>
        <div class="flex explore">
            <h1 style="width:60%"> Marketing Resources: Insider Advice on How to Increase Online Sales</h1>
            <button>Explore All Resorses</button>
        </div>
        <div class="flex explore">
            <div style="width:25%" v-for="(elem,index) in  technique" :key="index"><img  :src="require(`../assets/${elem.image}`)"> 
                <p><b>{{elem.title}}</b></p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['technique']
}
</script>

<style scoped lang="scss">
div {
    background-color: rgba(218, 220, 222, 0.314);
}
img{width:330px;
height:230px;

&:hover {box-shadow: 1px 5px 5px rgba(0, 0, 0, 0.229);
     filter: sepia(30%) brightness(110%);
 }}
.explore {
    padding: 0 15%;
    font-size: 20px;
    &:hover {
     filter: sepia(10%) brightness(110%);
 }
}
P:hover{color:#eb621f;}
h1 {
    font-size: 40px;
}
</style>
<template>
    <div>
        <div class="fott">
            <div class="uno">
                <h1>Grow Your Online Business Strategically, and Improve Customer Retention.</h1>
                <div class=" flex icone">
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-youtube"></i>
                    <i class="fa-brands fa-linkedin"></i>
                    <i class="fa-brands fa-tiktok"></i>
                </div>
            </div>

            <div class="services">

                <h3><b>Services</b></h3>
                <ul v-for="(lista, index) in services" :key="index">
                    <li>{{ lista }}</li>
                </ul>
            </div>
            <div class="resources">
                <h3><b> Resouces</b></h3>
                <ul v-for="(lista, index) in resources" :key="index">
                    <li>{{ lista }}</li>
                </ul>
            </div>
            <div class="company">
                <h3><b> Company</b></h3>
                <ul v-for="(lista, index) in company" :key="index">
                    <li>{{ lista }}</li>
                </ul>
            </div>
        </div>
        <div class="flex">
            <span>© 2020 • Avada Consultant • Powered by WordPress</span>
            <span>Call Us (555) 802-1234</span>
            <span>info@yourcompany.com</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterProject',
    props: ['services', 'resources', 'company']


}
</script>

<style lang="scss" scoped>
h1 {
    font-size: 25px;
    &:hover {color:orange;
    font-size: 30px;
font-style: oblique;}
}
i:hover {color:orange;
font-size:xx-large;}
.uno {
    width: 50%;
}

.fott {
    display: flex;
    justify-content: space-between;

    padding: 1% 15%;
}
.icone{width:200px;
height:50px;}
// ul {
// margin:3%;
// }
ul li {
    height:25px;
    list-style-type: none;
    color: grey;
    &:hover{border-right:5px solid rgba(138, 137, 136, 0.559);
        
        
        font-size:larger;
    color:orangered;}
}
span{color:grey; padding:1% 5%;}
.services,
.company,
.resources { width:35%;
    height:400px;
    align-content:center;
    display: flex;
    flex-direction: column;
    border-radius:20px;
    &:hover{  box-shadow: 1px 5px 5px rgba(0, 0, 0, 0.229);
    }
}

h3 {
    padding-left: 40px;
    &:hover{color:orangered;
    font-size: x-large;}
}
</style>
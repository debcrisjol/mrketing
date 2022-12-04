<template>
    <div>
        <fotter>
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
        </fotter>
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
}

.uno {
    width: 40%;
}

fotter {
    display: flex;
    justify-content: space-between;

    padding: 1% 15%;
}
.icone{width:200px;}
ul li {
    list-style-type: none;
    color: grey;
    height: 5px;
}
span{color:grey;}
.services,
.company,
.resources {
    display: flex;
    flex-direction: column;
}

h3 {
    padding-left: 35px;
}
</style>
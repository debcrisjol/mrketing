<template>
    <div class="consultant">
        <img src="../assets/large-testimonial-600x583.jpg" alt="testimonial">
        <div class="container">
            <h1> <b> “The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online and
                    offline. We have experienced year on year growth due to their progressive approach.”</b>
            </h1> <br>
            <h2>Kate Schadler</h2> <br>
            <span>Marketing Consultant Abstract</span>
        </div>

    </div>
</template>


<script>

export default {
    name: 'ConsultantWork',

}
</script>

<style lang="scss" scoped>
.consultant {
    display: flex;
    padding: 0 10%;
}

.container {
    margin: 3% 5%;
    &:hover{color:#668660;
    }


}

h2 {
    margin: 0;
    font-size: larger;
}

img {
    margin: 1%;

    &:hover {
        filter: sepia(10%) brightness(110%);
    }

}
</style>
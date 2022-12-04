

<template>
    <div class="makethings">
        <div class="flex">
            <div class="details">
                <h1>Let’s Make Things Happen</h1>
                <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur.
                </p>
                <hr /><br>
                <p><i>“The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online
                        and offline. We have experienced year on year growth due to their progressive approach.”</i></p>
                <br>
                <h4>George Anderson</h4>
                <h6>Digitalbox CEO</h6>
            </div>
            <div class="form">

                <div class="consultant-expert">
                    <img src="../assets/marketing-consultant-expert.jpg" alt="consultant-expert">
                    <h3>Richard Madsen</h3>
                    <p>Marketing Consultat Expert</p>
                    <i class="fa-solid fa-phone"> </i><span class="tel">(555)802-1234 </span>
                </div>

                <input type="name" placeholder="Your Name*">
                <input type="email" placeholder="Your Email*">
                <input type="phone" placeholder="Your Phone Number*">
                <button>Get a Callback</button>
                <span class="submydata">By submitting my data I agree to be contacted</span>
            </div>


        </div>

    </div>

</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.makethings {
    background-color: black;
    color: white;

    padding: 2% 15%;
}
.details{padding:0 5%;
width:40%;}
.form{position:static;
    width:30%;
    height:350px;
    margin-right:10%;
}
hr{width:30px; float:left; border-color:rgba(255, 246, 246, 0.493);
}
</style>
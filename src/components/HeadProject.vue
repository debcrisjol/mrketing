<template>
    <div>
        <nav class="navbar-menu">

          <img class="logo" src="../assets/avada-marketing-logo.png" alt="logo avada">
          <a v-for="(elem, index) in navBarHeader" :key="index" :href="elem.link">{{ elem.name }}</a>
          <div><i class="fa-solid fa-phone"> </i><span class="tel">(555)802-1234 </span></div>
          <button>Free Quote</button>

        </nav>   
        <div class="primaparte">
            <div class="unlockpotential"><h1> Unlock Your Online Growth Potential</h1>
            <p>Online marketing to secure customer retetion, leads and sales. We focus on the bigger picture.</p>
            <button class="btn services">Our Servises <i class="fa-solid fa-arrow-right"></i></button></div>
            
            <div class="form">
                <div class="consultant-expert">
                <img src="../assets/marketing-consultant-expert.jpg" alt="consultant-expert">
                <h3>Richard Madsen</h3>
                <p>Marketing Consultat Expert</p>
                <i class="fa-solid fa-phone"> </i><span class="tel">(555)802-1234 </span></div>

                <input type="name" placeholder="Your Name*"  v-model ="name">
                <input type="email" placeholder="Your Email*"  v-model ="email">
                <input type="phone" placeholder="Your Phone Number*"  v-model ="phone">
                <button @click='submit'>Get a Callback</button>
                <span class="submydata">By submitting my data I agree to be contacted</span>
            </div>
           
        </div> 
     
    </div>

    
  </template>
  
  <script>
  export default {
    props: {
    navBarHeader: Array,
  },data(){return{
    name:'',
    email:'',
    phone:''
  }
},
methods: {
  submit() {
    alert(`${this.name} will be contacted at this phone number ${this.phone} or by email at ${this.email}`)
    this.$emit('call')
    }
}
  }
  </script>
  
  <style scoped lang="scss">
  alert{background-color: #efd43f;}
  .navbar-menu{ padding:0 10%;
    height:10vh;
   color:#424242;
   display:flex;
   align-items: center;
justify-content: space-between;}
   .fa-phone{width:35px;
color:orange;}
button{padding:10px;
    height:40px;
    border-style: none;
border-radius: 10px;
color:white;
background-color: orange;
&:hover {background-color: #f76210; }}
a:hover, i:hover, .tel:hover {color:#efd43f;
font-size: larger;
}
.logo{width:18%;}
a{text-decoration: none;
color:#424242;}
a:hover {text-decoration: underline;
}
h1{font-size: 35px;}
.primaparte{height:65vh;
    width:100%;
background-image: url(../assets/marketing-intro.jpg);
background-repeat:no-repeat;
background-size:cover;
color:white;
}
.unlockpotential{text-align:start;
width:25%;
padding:5% 20%;
position: relative;}
.btn {color:black;
background-color: white;}

  </style>
  <style lang="scss">
  .form{width:20%;
    height:60%;
position:absolute;
top:30%;
right:20%;
background-color: white;
color:#686767;
display:flex;
flex-direction: column;
justify-content: space-between;
padding:10px 15px;
border-radius: 10px;
box-shadow: 1px 5px 5px rgba(0, 0, 0, 0.229);}
.form h3{color:black;}
.form img {width:20%;
border-radius: 50%; }
.form p { font-size: 14px; }
.form .submydata{font-size: 10px;
text-align: center;
color:#424242}
.form span{color:orange;}

.form .consultant-expert{text-align: center;}
.form input{ height:30px;
border-radius: 10px;
border-color: #d3d0d085;}

  </style>
  
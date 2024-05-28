<script>
import { RouterLink } from 'vue-router';


export default {
    data() {
        return {
            isOpen: false
        };
    },
    methods: {
        toggleMenu() {
            this.isOpen = !this.isOpen;
        }
    },
    components: { RouterLink }
};

</script>

<template>
  <div class="menu" v-if="isOpen">
    <a href="#">Page</a>
    <a href="#">Page</a>
    <a href="#">Page</a>
    <a href="/">page</a>
    <a href="/login">Login</a>
  </div>
    <div class="nav">
        <img src="https://media.discordapp.net/attachments/1242435349884436590/1243973774089392158/5c70fec03f23c7d670a63056ab0c639b-removebg-preview.png?ex=6656b81b&is=6655669b&hm=3e71d3a9c245caa495cc3b5fce3da050544d379508c75a412b83988114eeffae&=&format=webp&quality=lossless" alt="hl logo">
        <div class="right">
          <RouterLink class="btn" to="/login">Login</RouterLink>
          <div class="menu-toggle" @click="toggleMenu" :class="{ 'active': isOpen }">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>
        </div>
    </div>
</template>

<style scoped>

.menu{
  width:30vw;
  height:100%;
  position:fixed;
  top:0;
  left:0;
  display:flex;
  flex-direction:column;
  background-image:repeating-linear-gradient(90deg, rgba(0,0,0, 0.06) 0px, rgba(0,0,0, 0.06) 1px,transparent 1px, transparent 21px,rgba(0,0,0, 0.06) 21px, rgba(0,0,0, 0.06) 22px,transparent 22px, transparent 72px),repeating-linear-gradient(0deg, rgba(0,0,0, 0.06) 0px, rgba(0,0,0, 0.06) 1px,transparent 1px, transparent 21px,rgba(0,0,0, 0.06) 21px, rgba(0,0,0, 0.06) 22px,transparent 22px, transparent 72px),repeating-linear-gradient(135deg, rgba(0,0,0, 0.06) 0px, rgba(0,0,0, 0.06) 1px,transparent 1px, transparent 21px,rgba(0,0,0, 0.06) 21px, rgba(0,0,0, 0.06) 22px,transparent 22px, transparent 72px),linear-gradient(90deg, rgb(78, 64, 204),rgb(78, 64, 204));
  z-index:1500;
  box-shadow:1px 5px 5px rgba(0, 0, 0, 0.253);
  justify-content:center;
  align-items:center;
  gap:80px;
  z-index:1000000000;
}

.menu a{
  text-decoration:none;
  color:white;
  height:60px;
  font-size:30px;
}

.nav{
    display:none;
    width:100%;
    background-color:var(--background);
    height:10vh;
    align-items:center;
    flex-direction:row;
    justify-content:center;
    gap:60%;
    position:fixed;
    top:0;
    z-index:100000000;
}

.nav img{
  width:120px;
  height:100%;
  background-color:var(--primary);
}

.right{
  display:flex;
  justify-content:center;
  align-items:center;
  gap:60px;
}

.menu-toggle{
  display: block;
  width: 25px;
  height: 20px;
  position: relative;
  cursor: pointer;
}

.bar{
  display: block;
  width: 100%;
  height: 2px;
  background-color:var(--primary);
  position: absolute;
  transition: transform 0.3s ease;
}

.bar:nth-child(1){
  top: 0;
}

.bar:nth-child(2){
  top: 50%;
  transform: translateY(-50%);
}

.bar:nth-child(3){
  bottom: 0;
}

.menu-toggle.active .bar:nth-child(1){
  transform: translateY(9px) rotate(45deg);
  background-color:rgba(128, 128, 128, 0.363) !important;
}

.menu-toggle.active .bar:nth-child(2){
  opacity: 0;
}

.menu-toggle.active .bar:nth-child(3){
  transform: translateY(-9px) rotate(-45deg);
  background-color:rgba(128, 128, 128, 0.363);
}

.btn{
    text-transform:uppercase;
    padding:12px 30px;
    color:white;
    background-color:var(--primary);
    border-radius:8px;
    border-bottom:4px solid rgb(82, 72, 172);
    text-decoration:none;
    cursor:pointer;
}

.btn:hover{
    border-bottom:2px solid rgb(82, 72, 172);
}

@media (max-width:700px) {
  .nav{
    gap:30px;
  }

  .menu{
    width:60vw;
  }

  }

</style>
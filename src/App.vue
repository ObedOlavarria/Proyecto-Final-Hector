<script setup>
import Home from "./components/Home.vue";
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
import About from "./components/About.vue";
import Services from "./components/Services.vue";
import Team from "./components/Team.vue";
import Modal from "./components/Modal.vue";
import Projects from "./components/Projects.vue";
import Blog from "./components/Blog.vue";
import Contac from "./components/Contac.vue";
import ScrollUp from "./components/ScrollUp.vue";
</script>
  
<template>
  <div>
    <Navbar />
    <Home />
    <br /><br /><br /><br />
    <About />
    <br /><br /><br /><br />
    <Services />
    <br /><br /><br /><br />
    <Team />
    <br /><br /><br /><br />
    <Projects/>
    <br /><br /><br /><br />
    <Modal />
    <br /><br />
    <Blog/>
    <Contac/>
    <br /><br />
    <!--<Footer />-->
    <ScrollUp/>
  </div>
</template>

<style scoped></style>

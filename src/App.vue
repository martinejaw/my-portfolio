<template>
  <NavBar />
  <Header />
  <Proyects />
  <About />
  <Footer />
</template>

<script>
import NavBar from "./components/NavBar";
import Header from "./components/Header";
import Proyects from "./components/Proyects";
import About from "./components/About";
import Footer from "./components/Footer";


export default {
  name: "App",
  components: {
    NavBar,
    Header,
    Proyects,
    About,
    Footer
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

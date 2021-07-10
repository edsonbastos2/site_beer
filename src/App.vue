<template>
  <Header/>
  <Home/>
  <Footer/>
</template>

<script>
import Header from './components/Header';
import Home from './views/Home';
import Footer from './components/Footer';
import './styles/global.css';

export default {
  components:{
    Header,
    Home,
    Footer
  }
}
</script>

<style>
</style>

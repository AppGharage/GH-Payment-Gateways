<template>  
  <div>
    <Header></Header>

    <div style="margin-top: 50px;"></div>
    
    <div class="container">
      <div class="row">
          <Card v-for="paymentGateway of paymentGatewaysLists" 
            :key="paymentGateway.id" 
            :companyName="paymentGateway.name" />
      </div>
    </div>

    <div style="margin-top: 50px;"></div>

    <Footer></Footer>
  </div>
</template>

<script>
import axios from 'axios'
import Header from './Header'
import Footer from './Footer'
import Card from './Card'


export default {
  name: 'app',
  components: {
    Header,
    Footer,
    Card
  },
  data () {
    return {
      paymentGatewaysLists: []
    }
  },
  mounted() {
    axios.get('https://raw.githubusercontent.com/AppGharage/GH-Payment-Gateways/master/payment-gateways.json')
    .then(response => {this.paymentGatewaysLists = response.data})
  }
}
</script>

<style scoped>
  html{
    margin: 0;
    padding: 0;
  }

  body, div{
    font-family: 'Comfortaa', cursive;
    color: #fff;
    overflow: hidden;
  }

  h1, h2, h3, h4, h5, a, span{
    font-family: 'Comfortaa', cursive;
    color: #fff;
  }

  body{
    overflow-x: hidden;
  }

  .m{
    font-style: normal;
    font-weight: bold;
  }

  .m1{
    margin-top: 5px
  }

  .m2{
    margin-top: 5px;
  }

  .m4{
    margin-top: 20px;
    font-size: 14px;
    color: #fafafa
  }
  
  .header{
    text-align: center;
    height: 272px;
    left: 0;
    top: 0;
    background: linear-gradient(100.12deg, #3880FF 0%, #67A7FF 99.82%);
    box-shadow: 0px 4px 0px rgba(0, 0, 0, 0.25);
  }
</style>

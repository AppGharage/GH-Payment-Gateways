<template>
    <!-- Card -->
    <div class="col-md-6 col-lg-4">

        <div class="card">
            <div class="main-bg-area">
                <center>
                    <div class="card-logo">
                        <!-- <img class="card-img-top" src="elyse.png" alt="Card image cap"> -->
                    </div>
                </center>

                <div class="card-body">
                    <h5 class="card-title">Features <hr></h5>

                    <div class="card-text">
                        <p>Accept Mobile Money</p>
                        <p>Accept Ghana issued cards</p>
                        <p>USSD API</p>
                        <p>SMS API</p>
                    </div>
                    <div class="card-text margin-top-30">
                        <div class="row">
                            <div class="col-md-7 col-sm-7 charges-label">
                                <span>Payment Charges</span>
                            </div>

                            <div class="col-md-5 col-sm-5">
                                <div class="row">
                                    <div class="col-md-6 col-sm-6 divider">
                                        <div class="row">
                                            <div class="col-md-12 charges">1.95%</div>
                                            <div class="col-md-12 charges">LOC</div>
                                        </div>
                                    </div>
                                    <div class="col-md-6 col-sm-6 charges">
                                        <div class="row">
                                            <div class="col-md-12 charges">0.00%</div>
                                            <div class="col-md-12 charges">INTL</div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="card-footer">
                <div class="row">
                    <div class="col">
                        <span class="align-middle h3">
                        Hubtel
                        </span>
                    </div>
                    <div class="col">
                        <span class="float-right">
                            <a href="#" class="btn btn-primary">read more</a>
                        </span>
                    </div>
                </div>
            </div>

        </div>
    </div> 
    <!-- End  Card -->
</template>

<script>
import axios from 'axios';

export default {
  name: 'Card',
  data () {
    return {
      paymentGatewaysList: []
    }
  },
  mounted() {
    axios.get('')
    .then(response => {this.paymentGatewaysList = response.data.results})
  }
}
</script>
<style scoped>
  .main-bg-area{
    background-color: #147BED;
  }
  .charges-label{
    font-size: 12px;
  }

  .charges{
    font-size: 11px;
    font-style: normal;
    font-weight: bold;
    text-align: center;
  }

 .card{
    margin: 10px;
  }

  .card-logo{
    height: 50px;
    width: 150px;
    border-radius: 5px;
    background-image: url(https://hubtel.com/wp-content/themes/hubtel/html/assets/images/hubtel.png);
    background-position: center;
    background-repeat: no-repeat;
    background-size: 120px;
    box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.25);
    margin-top: 20px;
    border: 1px solid #fff;
  }

  .card-title{
    text-align: center;
    font-size: 16px;
    font-style: normal;
    font-weight: bold;
  }

  .card-text p{
    font-size: 12px;
    border-left: solid 2px #89B077;
    padding-left: 5px;
    padding-right: 5px;
    margin-top: 0;
    margin-bottom: 4px;
    margin-right: 0;
    margin-left: 0;
    font-style: normal;
    font-weight: bold;
  }

  .margin-top-30{
    margin-top: 30px;
  }

  .card-footer .h3{
    font-size: 16px;
    font-style: normal;
    font-weight: bold;
    color: #000;
  }

  .card-footer a{
    font-size: 11px;
  }

  .divider{
    border-right: 1px solid #fff;
  }

  .col-md-4{
    margin-bottom: 30px;
  }
</style>


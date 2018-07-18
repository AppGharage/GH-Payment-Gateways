<template>
    <!-- Card -->
    <div class="col-md-6 col-lg-4">

        <div class="card">
            <div class="main-bg-area" :style="{ backgroundColor: themeColor }">
                <center>
                    <div class="card-logo">
                         <img class="card-img" :src="logoUrl" alt="Logo"> 
                    </div>
                </center>

                <div class="card-body">
                    <h5 class="card-title">
                        Services 
                        <hr>
                    </h5>

                    <div class="card-text" v-for="service of services" :key="service">
                        <p>{{ service }}</p>
                    </div>

                    <div class="card-text margin-top-30">
                        <div class="row">
                            <div class="col-md-7 col-sm-7 charges-label">
                                <span>Processing Fee : </span>
                            </div>

                            <div class="col-md-5 col-sm-5">
                                <div class="row">
                                    <div class="col-md-6 col-sm-6 divider">
                                        <div class="row">
                                            <div class="col-md-12 charges">{{ localCharge }}</div>
                                            <div class="col-md-12 charges">LOC</div>
                                        </div>
                                    </div>
                                    <div class="col-md-6 col-sm-6 charges">
                                        <div class="row">
                                            <div class="col-md-12 charges">{{ intCharge }}</div>
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
                        {{companyName}}
                        </span>
                    </div>
                    <div class="col">
                        <span class="float-right">
                            <a :href="companyUrl" class="btn" :style="{ backgroundColor: themeColor }">Learn More</a>
                        </span>
                    </div>
                </div>
            </div>

        </div>
    </div> 
    <!-- End  Card -->
</template>

<script>

export default {
    name: 'Card',
    props: [
        'companyName',
        'logoUrl',
        'localCharge',
        'intCharge',
        'services',
        'companyUrl',
        'themeColor'
    ]
}
</script>
<style scoped>
  .charges-label{
    font-size: 12px;
  }

  .card-img{
    padding: 5px;
    height: 50px;
    width: 150px;
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
    font-weight: bold;
    color: #ffffff;
  }

  .divider{
    border-right: 1px solid #fff;
  }

  .col-md-4{
    margin-bottom: 30px;
  }

  hr{
      border-color: rgb(161, 163, 167);
  }
</style>


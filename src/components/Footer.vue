<template>
    <div>
        <div class="footer">
            <div class="row h-100">
                <div class="col-sm-12 my-auto">
                    <h4 class="align-middle m">Do you know any other Payment Gateway?</h4>
                    <p class="align-text-bottom m2">Update our list with a Github pull request!</p>
                    <a href="https://github.com/AppGharage/GH-Payment-Gateways" type="button" class="btn btn-secondary">
                        View Repo on Github
                    </a>
                </div>
            </div>
        </div>

        <div class="footer-end">
            <span style="color: #000;">&copy;2018. Designed by 
                <a href="#">Baffour Adu Boampong</a> &amp; <a href="#">Peter Perez</a>
            </span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>
<style scoped>

  .footer{
    text-align: center;
    height: 272px;
    left: 0;
    top: 0;
    background: #3880FF;
  }

  .footer-end{
    text-align: center;
    height: 40px;
    left: 0;
    top: 0;
    background: #fff;
    color: #000;
    font-size: 14px;
    padding-top: 10px;
  }

  .footer-end a{
    color: #3880FF;
  }
</style>


.<template>
  <section class="intro">
        <div class="overlay"></div>
        <div class="row m-0 content align-items-center">
            <div class="col-md-6">
                <h3>
                    Need a professional business consultation? Look no further. We are here to help!
                </h3>
                <p>
                    We offer a professional advice, guidance and actionable solutions to businesses experiencing issues they can’t deal with in-house.
                </p>
                <div class="btns">
                    <a href="#" class="btn btn-primary">
                        Get free consultation
                    </a>
                    <a href="#" class="btn btn-alt">
                        Get free consultation
                        <font-awesome-icon icon="fa-solid fa-angle-right" />
                    </a>
                </div>
            </div>
            <div class="col-md-6">
                <div class="image-1">
                    <img class="img-fluid" src="https://the7.io/consulting/wp-content/uploads/sites/67/elementor/thumbs/cons009-om2kpirnx6b0nfelfzr18xlon5e9gx4qk81mxtibl4.jpg" alt="">
                </div>
                <div class="image-2">
                    <img class="img-fluid" src="https://the7.io/consulting/wp-content/uploads/sites/67/elementor/thumbs/cons023-om42q8yrrghp7qkvlm1kz6rto42wszkd9qclh61i5k.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="row benifets">
            <div class="col">
                <div class="row">
                    <div class="col-auto">
                        <font-awesome-icon icon="fa-solid fa-address-card" />
                    </div>
                    <div class="col">
                        <h5>
                            A team of leading industry experts
                        </h5>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="row">
                    <div class="col-auto">
                        <font-awesome-icon icon="fa-solid fa-grip" />
                    </div>
                    <div class="col">
                        <h5>
                            A full range of consulting services
                        </h5>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="row">
                    <div class="col-auto">
                        <font-awesome-icon icon="fa-solid fa-handshake-simple" />
                    </div>
                    <div class="col">
                        <h5>
                            Exclusive extensive online consulting guides
                        </h5>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="row">
                    <div class="col-auto">
                        <font-awesome-icon icon="fa-solid fa-comments" />
                    </div>
                    <div class="col">
                        <h5>
                            100% free first consultation for all new clients
                        </h5>
                    </div>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeIntro'
}
</script>

<style>
    .intro {
        padding: 180px 30px 60px;
        background-color: rgb(15, 27, 45);
        position: relative;
    }
    .intro .overlay {
        background-image: url("https://the7.io/consulting/wp-content/uploads/sites/67/2020/05/wicked-bg-the7-5.svg");
        background-position-x: 50%;
        background-position-y: 50%;
        background-repeat: no-repeat;
        background-size: cover;
        box-sizing: border-box;
        left: 0px;
        mix-blend-mode: color-dodge;
        opacity: 0.5;
        position: absolute;
        top: 0px;
        transition-delay: 0s, 0s, 0s;
        transition-duration: 0.3s, 0.3s, 0.3s;
        transition-property: background, border-radius, opacity;
        transition-timing-function: ease, ease, ease;
        bottom: 0;
        right: 0;
        z-index: 0;
    }

    .intro .content {
        position: relative;
        z-index: 1;
    }

    .intro h3 {
        color: rgb(255, 255, 255);
        font-size: 35px;
        font-weight: 500;
        line-height: 42px
    } 
    .intro p {
        padding: 35px 0 0;
        color: rgb(255, 255, 255);
        font-size: 19px;
        line-height: 30.4px
    }
    .intro .btns {
        padding: 40px 0 0;
    }
    .intro .btns .btn-primary {
        margin: 0 30px 20px 0;
        background-color: var(--main-color);
        border-radius: 3px;
        border: none;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: rgb(17, 24, 28);
        display: inline-flex;
        font-size: 16px;
        font-weight: 500;
        justify-content: center;
        line-height: 16px;
        padding: 20px 24px;
        text-align: center;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease;
    }
    .intro .btns .btn-alt {
        margin: 0 30px 20px 0;
        background-color: transparent;
        border-radius: 3px;
        border: none;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: #fff;
        display: inline-flex;
        font-size: 16px;
        font-weight: 500;
        justify-content: center;
        line-height: 16px;
        padding: 20px 24px;
        text-align: center;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease;
        position: relative;
    }
    .intro .btns .btn-alt svg {
        margin: 0 5px;
    }
    .intro .btns .btn-alt:after {
        content: '';
        position: absolute;
        left: 24px;
        right: 24px;
        height: 1px;
        background: #f0c000;
        bottom: 12px;
    }
    .intro .btns .btn-primary:hover {
        background-color: rgb(238, 157, 43);
    }
    .intro .btns .btn-alt:hover {
        color: #f0c000;
    }
    .intro .image-1 {
        width: 372px
    }
    .intro .image-1 img{
        border-style: solid;
        border-width: 4px 0 0;
        border-color: var(--main-color);
        border-radius: 0% 33% 0% 33%;
    }
    .intro .image-2 {
        width: 275px;
        float: right;
        margin-top: -200px;
        z-index: 2;
        position: relative;
        margin-right: 50px;
    }
    .intro .image-2 img{
        border-style: solid;
        border-width: 4px 0 0;
        border-color: var(--main-color);
        border-radius: 33% 0% 33% 0%;
    }
    .intro .benifets {
        margin-top: 60px;
        
    }
    .intro .benifets svg {
        color: var(--main-color);
        font-size: 24px
    }
    .intro .benifets h5 {
        color: rgb(255, 255, 255);
        font-size: 15px;
        font-weight: 400;
        line-height: 22.5px
    }
</style>
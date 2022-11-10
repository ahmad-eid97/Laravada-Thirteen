<template>
  <section class="banner">
        <div class="overlay"></div>
        <div class="row content m-0 content align-items-center justify-content-center">
            <h2>
                Need a professional business consultation? Let's discuss your case!
            </h2>
            <div class="col-12 mt-5 text-center d-flex justify-content-center btns">
                <a href="#" class="btn-primary">
                    Contact us online
                </a>
                <div class="phone">
                    <font-awesome-icon icon="fa-solid fa-phone" />
                    1-001-234-5678
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeBanner'
}
</script>

<style lang="scss">
    .banner {
        padding: 90px 30px;
        background-color: rgb(15, 27, 45);
        position: relative;
    }
    .banner .overlay {
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
    .banner .content {
        z-index: 1;
        position: relative;
    }
    .banner h2 {
        color: rgb(255, 255, 255);
        font-size: 35px;
        font-weight: 500;
        line-height: 42px;
        text-align: center;
        max-width: 800px;
    }
    .banner .btn-primary {
        margin: 0 0 20px 0;
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
        padding: 17px 24px;
        text-align: center;
        transition-delay: 0s;
        transition-duration: 0.3s;
        transition-property: all;
        transition-timing-function: ease;
        text-decoration: none;
        min-height: 50px;
    }
    .banner .btn-primary:hover {
        background-color: rgb(238, 157, 43);
    }
    .banner .phone {
        display: inline-block;
        margin-left: 20px;
        box-shadow: rgba(0, 0, 0, 0) 0px 0px 10px 0px;
        color: var(--main-color);
        border: 1px solid var(--main-color);
        min-width: 240px;
        padding: 12px 24px;
        border-radius: 3px;
        min-height: 50px;
        margin-bottom: 20px;

    }
    @include xs {
        .btns {
            display: flex;
            flex-direction: column;
        }
    }
</style>
<template>
  <section class="Banner2">
        <div class="row content m-0 content align-items-center justify-content-center">
            <h2>
                Any questions? Request a call-back to get a free analysis of your business!
            </h2>
            <div class="col-12 mt-5 text-center form">
                <div class="row m-0">
                    <form  class="p-0 d-flex"> 
                        <b-form-input
                        placeholder="Enter your name"
                        ></b-form-input>

                        <b-form-input placeholder="Phone number"></b-form-input>
                    </form>
                </div>
                <a href="#" class="btn-primary d-block">
                    <font-awesome-icon icon="fa-solid fa-phone" />
                    Request a call-back
                </a>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeBanner22'
}
</script>

<style>
    .Banner2 {
        padding: 90px 30px;
        background-color: rgb(241, 243, 245);
        position: relative;
    }

    .Banner2 .content {
        z-index: 1;
        position: relative;
    }
    .Banner2 h2 {
        color: rgb(17, 24, 28);
        font-size: 35px;
        font-weight: 500;
        line-height: 42px;
        text-align: center;
        max-width: 800px;
    }
    .Banner2 .form {
        width: 600px;
        max-width: 100%;
    }
    .Banner2 .form .form-control {
        margin: 0 10px 20px;
        background-color: rgb(255, 255, 255);
        border: 0 solid rgba(0, 0, 0, 0.12);
        border-radius: 3px;
        color: rgb(17, 24, 28);
        font-size: 15px;
        font-weight: 400;
        height: 59px;
        line-height: 27px;
        min-height: 59px;
        outline-color: rgb(17, 24, 28);
        padding: 7px 20px;
    }
    .Banner2 .form .form-control:focus {
        box-shadow: none;
    }
    .Banner2 .btn-primary {
        margin: 0 10px 20px;
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
    .Banner2 .btn-primary:hover {
        background-color: rgb(238, 157, 43);
    }

</style>
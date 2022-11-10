<template>
  <section class="features">
        <div class="row m-0 content align-items-center">
            <div class="col-md-6 p-4">
                <h6>Welcome to seven consulting</h6>
                <h3>
                    Risk more than others think is safe. Dream more than others think is practical.
                </h3>
                <a href="#" class="btn-primary">
                    Let's discuss your case
                </a>
            </div>
            <div class="col-md-6">
                <div>
                    <b-tabs content-class="mt-3" fill>
                        <b-tab title="Why choose us" active>
                            <p>
                                Aliquam erat volutpat. Donec placerat metus erat, conubia nostra, per inceptos himenaeosnec vulputate nulla iaculis eu. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. In vel varius esteu! Suspendisse nec vulputate nulla iaculis eu potenti. 
                            </p>
                            <p>
                                Sed sagittis maximus quam, nec laoreet enim laoreet sed lorem ipsum placerat metus erat, nec vulputate nulla iaculis eu. Class aptent taciti sociosqu ad litora torquent per conubia.
                            </p>
                        </b-tab>
                        <b-tab title="Our principles">
                            <p>
                                Aliquam erat volutpat. Donec placerat metus, erat, nec vulputate nulla iaculis eu. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. In vel varius esteu! Donec placerat metus erat – nec vulputate nulla iaculis eu. 
                            </p>
                            <p>
                                Class nulla iaculis eu. Class aptent taciti sociosqu ad litora torquent aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos nulla iaculis eu.
                            </p>
                        </b-tab>
                        <b-tab title="Achivements">
                            <ol>
                                <li>
                                    Class aptent – nulla iaculis aptent taciti sociosqu ad litora torquenttaciti sociosqu
                                </li>
                                <li>
                                    Ad litora torquent per from glavrida ipsum
                                </li>
                                <li>
                                    Lorem ipsum dolor – nulla iaculis elass aptent taciti sociosqu
                                </li>
                                <li>
                                    In vel varius esteu gravidmi
                                </li>
                                <li>Ut elit tellus</li>
                                <li>
                                    Dolor nulla – iaculis elassnulla glavrida luctus nec nulla iaculis elass ullamcorper
                                </li>
                                <li>
                                    Class aptent taciti sociosqu dolor nulla
                                </li>
                            </ol>
                        </b-tab>
                    </b-tabs>
                </div>
            </div>
        </div>
        <div class="row mx-0 p-4 features-items">
            <div class="col-sm-6 col-lg-4 mb-4">
                <div class="feature">
                    <font-awesome-icon icon="fa-solid fa-chart-line" />
                    <p>Business development</p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-4 mb-4">
                <div class="feature">
                    <font-awesome-icon icon="fa-solid fa-gears" />
                    <p>Business optimisation</p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-4 mb-4">
                <div class="feature">
                    <font-awesome-icon icon="fa-solid fa-chart-pie" />
                    <p>Marketing planning</p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-4 mb-4">
                <div class="feature">
                    <font-awesome-icon icon="fa-solid fa-chess-knight" />
                    <p>Brand & strategy</p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-4 mb-4">
                <div class="feature">
                    <font-awesome-icon icon="fa-solid fa-user-group" />
                    <p>Human resources</p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-4 mb-4">
                <div class="feature">
                    <font-awesome-icon icon="fa-solid fa-calculator" />
                    <p>System analytics</p>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeFeatures'
}
</script>

<style>
    .features {
        padding: 90px 30px;
    }
    .features h6 {
        color: rgb(141, 149, 155);
        font-size: 19px;
        font-weight: 500;
        line-height: 26.6px;
        margin-bottom: 30px;
    }
    .features h3 {
        color: rgb(17, 24, 28);
        font-size: 27px;
        font-weight: 500;
        line-height: 35.1px;
        margin-bottom: 40px;
    }
    .features .btn-primary {
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
        text-decoration: none;
    }
    .features .btn-primary:hover {
        background-color: rgb(238, 157, 43);
    }
    .features .nav-tabs {
        border: none;
        padding-bottom: 20px;
    }
    .features .nav-tabs li {
        margin: 0;
        text-align: start;
    }
    .features .nav-tabs li a{
        color: rgb(141, 149, 155);
        cursor: pointer;
        font-size: 17px;
        font-weight: 500;
        line-height: 23.8px;
    }
    .features .nav-tabs li a:hover,
    .features .nav-tabs li a.active {
        border: none;
    }
    .features .nav-tabs li:hover::after {
        content: none;
    }
    .features .features-items {
        margin-top: 60px;
    }
    .features .features-items .feature{
        min-height: 220px;
        align-items: center;
        border-radius: 3px 3px 3px 3px;
        padding: 30px;
        background: #fff;
        border: 1px solid #e2e3e3;
        transition: all 0.3s linear;
        display: flex;
        flex-direction: column;
        justify-content: center;
        cursor: pointer;
    }
    .features .features-items .feature:hover{
        border-color: #fff;
        box-shadow: 0 0 20px 0 rgba(0,0,0,.2);
    }
    .features .features-items .feature svg {
        color: var(--main-color);
        font-size: 32px;
        margin-bottom: 20px;
    }
    .features .features-items .feature p {
        color: rgb(17, 24, 28);
        font-size: 19px;
        font-weight: 500;
        line-height: 26.6px;
    }
</style>
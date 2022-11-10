<template>
  <section class="why">
        <div class="row m-0 align-items-center">
            <div class="col-lg-6 p-4">
                <h6>Why choose our company</h6>
                <h3>
                    Here's how things are going to change for your business
                </h3>
                <ul>
                    <li>
                        <font-awesome-icon icon="fa-solid fa-check" />
                        150-180% more lorem volutpat donec glavrida ipsum dolor
                    </li>
                    <li>
                        <font-awesome-icon icon="fa-solid fa-check" />
                        Reative volutpat donec glavrida ipsum
                    </li>
                    <li>
                        <font-awesome-icon icon="fa-solid fa-check" />
                        Class aptent taciti sociosqu ad litora
                    </li>
                    <li>
                        <font-awesome-icon icon="fa-solid fa-check" />
                        100-200% of dolor nulla gravida et ipsum nulla
                    </li>
                    <li>
                        <font-awesome-icon icon="fa-solid fa-check" />
                        Amet lorem felis - dolor nulla gravida et nulla gravida 
                    </li>
                </ul>
            </div>
            <div class="col-lg-6 p-4">
                <iframe height="315" src="https://www.youtube.com/embed/XHOmBV4js_E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
        </div>
        <div class="row" style="padding: 0 10px;">

            <swiper :options="swiperOption">
                <swiper-slide>
                <div class="item">
                    <font-awesome-icon icon="fa-solid fa-quote-right" />
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut elit tellus luctu.
                    </p>
                    <h5>
                        Maria Green
                    </h5>
                    <h6>
                        Seven Dev - marketing director
                    </h6>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <font-awesome-icon icon="fa-solid fa-quote-right" />
                    <p>
                        Wow! Commodo egestas, feugiat leo eget ipsum dolor sitvulputate metus vestibulum ipsum.
                    </p>
                    <h5>
                        Bernard Blackwood
                    </h5>
                    <h6>
                        Seven & CO - marketing director
                    </h6>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <font-awesome-icon icon="fa-solid fa-quote-right" />
                    <p>
                        Super! 300%+ lorem neque mauris et leo ipsum ulvinar lorem neque. Thanx!
                    </p>
                    <h5>
                        John Richmond
                    </h5>
                    <h6>
                        Seven Consulting - executive director
                    </h6>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <font-awesome-icon icon="fa-solid fa-quote-right" />
                    <p>
                        Lorem metus vestibulum ipsum dolor sit amet, consectetur adipiscing elit odio nec urna metus vestibulum.
                    </p>
                    <h5>
                        Alexander Brown
                    </h5>
                    <h6>
                        Seven Creative - marketing director
                    </h6>
                </div>
                </swiper-slide>

                <swiper-slide>
                <div class="item">
                    <font-awesome-icon icon="fa-solid fa-quote-right" />
                    <p>
                        Consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis, pulvinar dapibus leo. Unbelievable!
                    </p>
                    <h5>
                        Tiffany Anderson
                    </h5>
                    <h6>
                        Seve Media - CEO
                    </h6>
                </div>
                </swiper-slide>
                <div class="swiper-button-prev" slot="button-prev"></div>
                <div class="swiper-button-next" slot="button-next"></div>
            </swiper>

        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomewhy',
    data() {
        return {
            swiperOption: {
                loop: true,
                slidesPerView: 3,
                spaceBetween: 50,
                breakpoints: {
                // when window width is >= 320px
                100: {
                    slidesPerView: 1,
                    spaceBetween: 5,
                },
                // when window width is >= 480px
                480: {
                    slidesPerView: 1,
                    spaceBetween: 5,
                },
                // when window width is >= 640px
                640: {
                    slidesPerView: 2,
                    spaceBetween: 5,
                },
                992: {
                    slidesPerView: 2,
                    spaceBetween: 5,
                },
                1200: {
                    slidesPerView: 3,
                    spaceBetween: 5,
                },
                },
            },
        }
    }
}
</script>

<style lang="scss">
    .why {
        padding: 90px 30px;
    }
    .why h6 {
        color: rgb(141, 149, 155);
        font-size: 19px;
        font-weight: 500;
        line-height: 26.6px;
        margin-bottom: 30px;
    }
    iframe {
        width: 100%;
    }
    @include xs {
        .why {
            padding: 50px 10px;
        }
    }
    .why h3 {
        color: rgb(17, 24, 28);
        font-size: 27px;
        font-weight: 500;
        line-height: 35.1px;
        margin-bottom: 40px;
    }
    .why ul {
        list-style: none;
        padding: 0;
    }
    .why li {
        color: rgb(95, 103, 109);
        font-size: 15px;
        margin: 7.5px 0;
    }
    .why li svg {
        color: var(--main-color);
        font-size: 14px;
        margin-right: 10px;
    }
    .why .progress {
        border-radius: 2px;
        margin-bottom: 30px;
    }
    .why .progress span {
        color: rgb(17, 24, 28);
        text-align: start;
        padding: 0 10px;
    }
    .why h5 {
        color: rgb(17, 24, 28);
        font-size: 17px;
        font-weight: 500;
        line-height: 23.8px
    }
    .why .item {
        padding: 30px;
        border: 1px solid #e2e3e3;
        max-width: 360px;
        margin: 0 auto;
        min-height: 320px;
    }
    .why .item svg {
        display: block;
        color: rgba(17, 24, 28, 0.12);
        font-size: 32px;
        margin-bottom: 25px;
    }
    .why .item p {
        color: rgb(95, 103, 109);
        font-size: 17px;
        line-height: 27.2px;
        margin-bottom: 25px;
        text-align: start;

    }
    .why .item h5 {
        color: rgb(17, 24, 28);
        font-size: 17px;
        font-weight: 500;
        line-height: 23.8px;
        margin-bottom: 5px;
        text-align: start;
        
    }
    .why .item h6 {
        color: rgb(141, 149, 155);
        font-size: 14px;
        font-weight: 400;
        line-height: 23.8px;
        margin-bottom: 15px;
        text-align: start;
    }

    .why .slick-slide > div {
        text-align: center;
    }
    .slick-prev {
        left: 7px;
    }
    .slick-next {
        right: 7px;
    }
    .slick-prev, .slick-next {
        width: 40px;
        height: 40px;
        z-index: 2;
    }
    .slick-prev::before, .slick-next::before {
        font-family: 'slick';
        font-size: 40px;
        line-height: 1;
        opacity: 0.75;
        color: #f0c000;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    .swiper-button-prev, .swiper-button-next {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-color: var(--main-color) !important;
        box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
    }
    .swiper-button-prev:after, .swiper-button-next:after {
        font-size: 20px;
        color: #fff;
    }
</style>
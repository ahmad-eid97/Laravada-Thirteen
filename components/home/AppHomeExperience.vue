<template>
  <section class="experience">
        <div class="row m-0 align-items-center">
            <div class="col-md-6 p-4">
                <h6>High level of competence</h6>
                <h3>
                    Our experience will help you create a quality product
                </h3>
                <p>
                    Aliquam erat volutpat. Donec placerat metus erat, nec vulputate nulla iaculis eu. Suspendisse potenti. Sed sagittis maximus quam, nec laoreet enim laoreet sed lorem ipsum vulputate nulla iaculis. Suspendisse euismod felis nunc, vitae aliquet lectus ornare.
                </p>
            </div>
            <div class="col-md-6 p-4">
                <h5> Online sevices </h5>
                <b-progress variant="warning" height="20px" :max="4.5" >
                    <b-progress-bar value="3">
                        <span>3 years</span>
                    </b-progress-bar>
                </b-progress>

                <h5> Finance management </h5>
                <b-progress variant="warning" height="20px" :max="7" >
                    <b-progress-bar value="5">
                        <span>5 years</span>
                    </b-progress-bar>
                </b-progress>

                <h5> Investment </h5>
                <b-progress variant="warning" height="20px" :max="12.5" >
                    <b-progress-bar value="10">
                        <span>10 years</span>
                    </b-progress-bar>
                </b-progress>

                <h5>Consulting</h5>
                <b-progress variant="warning" height="20px" :max="12" >
                    <b-progress-bar value="12">
                        <span>12 years</span>
                    </b-progress-bar>
                </b-progress>
            </div>
        </div>
        <div class="row" style="padding: 0 10px;">
            <div class="col-sm-6 col-lg-3 p-0">
                <div class="experience-item">
                    <span>01.</span>
                    <h4>
                        Experienced specialists
                    </h4>
                    <p>
                        Quisque in suscipit nisi, at auctor orci. Sed posuere ullamcorper molestie. Suspendisse euismod felis nunc, vitae aliquet lectus ornare.
                    </p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-3 p-0">
                <div class="experience-item">
                    <span>02.</span>
                    <h4>
                        Stable & predictable results
                    </h4>
                    <p>
                        Mauris eu ex nec felis sagittis efficitur. Suspendisse euismod felis nunc, vitae aliquet lectus ornare ac. Sed posuere ullamcorper molestie.
                    </p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-3 p-0">
                <div class="experience-item">
                    <span>03.</span>
                    <h4>
                        100% Satisfaction guarantee
                    </h4>
                    <p>
                        Mauris eu ex nec felis sagittis efficitur in suscipit nis posuere ullamcorper molestie. Suspendisse euismod!
                    </p>
                </div>
            </div>
            <div class="col-sm-6 col-lg-3 p-0">
                <div class="experience-item">
                    <span>04.</span>
                    <h4>
                        20+ Years in consulting business
                    </h4>
                    <p>
                        Sed posuere ullamcorper molestie. Suspendisse euismod felis nunc, vitae aliquet lectus ornare ac.
                    </p>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'AppHomeExperience'
}
</script>

<style>
    .experience {
        padding: 90px 30px;
    }
    .experience h6 {
        color: rgb(141, 149, 155);
        font-size: 19px;
        font-weight: 500;
        line-height: 26.6px;
        margin-bottom: 30px;
    }
    .experience h3 {
        color: rgb(17, 24, 28);
        font-size: 27px;
        font-weight: 500;
        line-height: 35.1px;
        margin-bottom: 40px;
    }
    .experience p {
        color: rgb(95, 103, 109);
        font-size: 15px;
    }
    .experience .progress {
        border-radius: 2px;
        margin-bottom: 30px;
    }
    .experience .progress span {
        color: rgb(17, 24, 28);
        text-align: start;
        padding: 0 10px;
    }
    .experience h5 {
        color: rgb(17, 24, 28);
        font-size: 17px;
        font-weight: 500;
        line-height: 23.8px
    }
    .experience .experience-item {
        padding: 30px;
    }
    .experience .experience-item span {
        color: rgb(241, 243, 245);
        font-size: 160px;
        line-height: 192px;
        margin-bottom: -100px;
        margin-left: -50px;
        display: block;
    }
    .experience .experience-item h4 {
        color: rgb(17, 24, 28);
        font-size: 19px;
        font-weight: 500;
        line-height: 26.6px;
        margin-bottom: 15px;
    }
</style>
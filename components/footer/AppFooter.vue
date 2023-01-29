<template>
  <footer class="bg-faded pt-70 pb-40 bg-theme-color-2">
    <subscribe />
    <!-- <div class="overlay"></div> -->
    <div class="content">
      <div class="row widgets m-0">
        <div class="col-sm-6 col-md-4 widget">
          <img
            :src="
              $store.state.websiteSettings.find((one) => one.key === 'logo')
                .plain_value
            "
            alt="logoImage"
            style="width: 200px"
          />
          <p>
            {{
              $store.state.websiteSettings.find(
                (one) => one.key === "description"
              ).plain_value
            }}
          </p>
        </div>
        <div class="col-sm-6 col-md-4 widget">
          <h5>Contact info</h5>
          <div class="row m-0">
            <div class="col-12 p-0 item">
              <p>
                <font-awesome-icon icon="fa-solid fa-phone" />
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "email"
                  ).phone || "No Number"
                }}
              </p>
            </div>
            <div class="col-12 p-0 item">
              <p>
                <font-awesome-icon icon="fa-solid fa-envelope" />
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "email"
                  ).plain_value
                }}
              </p>
            </div>
            <div class="col-12 p-0 item">
              <p>
                <font-awesome-icon icon="fa-solid fa-building" />
                {{
                  $store.state.websiteSettings.find(
                    (one) => one.key === "contact_phone"
                  ).plain_value
                }}
              </p>
            </div>
          </div>
        </div>
        <div class="col-sm-6 col-md-4 widget">
          <div class="footer-item">
            <div class="footer-title">
              <h5>Useful Links</h5>
            </div>
            <ul class="footer-list">
              <!-- <li><a href="#">About Us</a></li> -->
              <li>
                <nuxt-link :to="localePath('/about')">About Us</nuxt-link>
              </li>
              <li>
                <nuxt-link :to="localePath('/services')">Services</nuxt-link>
              </li>
              <li>
                <nuxt-link :to="localePath('/team')">Team</nuxt-link>
              </li>
              <li>
                <nuxt-link :to="localePath('/testimonials')">Gallery</nuxt-link>
              </li>
              <li>
                <nuxt-link :to="localePath('/blogs')">Blogs</nuxt-link>
              </li>
              <li>
                <nuxt-link :to="localePath('/contact')">Contact</nuxt-link>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <hr />
      <div class="row copyrights">
        <p>
          © Copyright 2022 - 2023 | Laravada Theme | All Rights Reserved |
          Powered by Rail Coder
          <span>
            <a href="#"><font-awesome-icon icon="fa-brands fa-instagram" /></a>
            <a href="#">
              <font-awesome-icon icon="fa-brands fa-twitter" />
            </a>
            <a href="#">
              <font-awesome-icon icon="fa-brands fa-facebook" />
            </a>
          </span>
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import Subscribe from "../subscribe/subscribe.vue";
export default {
  name: "AppFooter",
  components: { Subscribe },
  data() {
    return {};
  },
  beforeMount() {},
  methods: {
    generatePagePath(id) {
      switch (id) {
        case 1:
          return "/about";
        case 2:
          return "/contact";
        case 3:
          return "/terms";
        case 4:
          return "/policy";
      }
    },
  },
};
</script>
<style lang="scss">
footer {
  padding: 20px 30px 20px;
  background-color: rgb(15, 27, 45);
  position: relative;
}
footer .overlay {
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

footer .content {
  position: relative;
  z-index: 1;
}

footer .widgets {
  padding-bottom: 30px;
}
footer .widget {
  padding: 30px;
}

footer .widget p {
  margin-top: 30px;
  color: rgb(255, 255, 255);
  font-size: 15px;
  font-weight: 400;
  line-height: 27px;
}
footer .widget .item p {
  margin: 0;
}
footer .widget h5 {
  padding-bottom: 6px;
  padding-right: 30px;
  font-size: 15px;
  font-weight: 500;
  line-height: 21px;
  border-bottom: 1px solid #f0c000;
  color: #fff;
  display: inline-block;
  margin-bottom: 30px;
}
footer .widget svg {
  margin-right: 10px;
}
footer .widget span {
  display: block;
  color: rgba(255, 255, 255, 0.5);
  font-size: 13px;
  font-weight: 400;
  line-height: 16.9px;
  margin-left: 30px;
  margin-top: 6px;
}
footer .widget .item {
  margin-bottom: 25px;
}
footer .widget .item a {
  color: #fff;
  color: rgb(255, 255, 255);
  font-size: 15px;
  font-weight: 400;
  line-height: 27px;
  cursor: pointer;
}
footer .widget .item a:hover {
  color: #f0c000;
}
footer .widget .item a span {
  display: block;
  color: rgba(255, 255, 255, 0.5);
  font-size: 13px;
  font-weight: 400;
  line-height: 16.9px;
  margin-top: 6px;
  margin-left: 0;
}

footer hr {
  border-color: #8d97a6;
}
footer .copyrights {
  color: rgba(255, 255, 255, 0.5);
  font-size: 13px;
  font-weight: 400;
  line-height: 16.9px;
}

footer .copyrights span {
  float: right;
}
footer .copyrights span a {
  color: rgba(255, 255, 255, 0.5);
  font-size: 16px;
  margin-left: 16px;
}
.footer-list {
  padding: 0;
  list-style: none;
  li {
    padding: 5px 0;
    a {
      color: #fff;
      text-decoration: none;
    }
  }
}
</style>

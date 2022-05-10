<template>
  <div class="wrap-sidebar">
    <div class="sidebar">
      <ul class="sidebar_top">
        <li>
          <NuxtLink to="/forme">
            <b-icon icon="house-fill"> </b-icon>
            Dành cho bạn
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/following">
            <b-icon icon="people"> </b-icon>
            Đang follow
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/live">
            <b-icon icon="camera-video"> </b-icon>
            LIVE
          </NuxtLink>
        </li>
      </ul>
      <div class="sidebar_login">
        <p>Đăng nhập để follow các tác giả, thích video và xem bình luận</p>
        <b-button variant="outline-danger">Đăng nhập</b-button>
      </div>

      <div class="recommended_acc">
        <h6>Tài khoản được đề xuất</h6>
        <ul class="acc-info">
          <li v-for="(accT, index1) in recommendAccsT" v-bind:key="index1">
            <NuxtLink class="acc-info__item" :to="'/@' + accT.username">
              <div class="acc_img">
                <img :src="accT.img" :alt="accT.name" />
              </div>
              <div class="desc">
                <span class="acc_link">{{ accT.username }}</span>
                <span class="acc_name">{{ accT.name }}</span>
              </div>
            </NuxtLink>
            <div class="acc-info__hover">
              <b-row>
                <b-col md="6">
                  <NuxtLink :to="`/@` + accT.username">
                    <div class="img-hover">
                      <img :src="accT.img" :alt="accT.name" />
                    </div>
                    <div class="info-hover">
                      <h6 class="acc_link">{{ accT.username }}</h6>
                      <h6 class="acc_name">{{ accT.name }}</h6>
                    </div>
                  </NuxtLink>
                </b-col>
                <b-col md="6" style="cursor: default">
                  <div class="btn-follow">
                    <b-button>Follow</b-button>
                  </div>
                </b-col>
                <b-col md="12">
                  <div class="follow-info">
                    <p>
                      <span class="consume">{{ accT.follower }}M</span>
                      <span class="desc">Follower</span>
                    </p>
                    <p>
                      <span class="consume">{{ accT.like }}M</span>
                      <span class="desc">Thích</span>
                    </p>
                  </div>
                </b-col>
              </b-row>
            </div>
          </li>
          <b-collapse id="collapse-a">
            <li v-for="(accB, index2) in recommendAccsB" v-bind:key="index2">
              <NuxtLink class="acc-info__item" :to="'/@' + accB.username">
                <div class="acc_img">
                  <img :src="accB.img" :alt="accB.name" />
                </div>
                <div class="desc">
                  <span class="acc_link">{{ accB.username }}</span>
                  <span class="acc_name">{{ accB.name }}</span>
                </div>
              </NuxtLink>
              <div class="acc-info__hover">
                <b-row>
                  <b-col md="6">
                    <NuxtLink :to="`/@` + accB.username">
                      <div class="img-hover">
                        <img :src="accB.img" :alt="accB.name" />
                      </div>
                      <div class="info-hover">
                        <h6 class="acc_link">{{ accB.username }}</h6>
                        <h6 class="acc_name">{{ accB.name }}</h6>
                      </div>
                    </NuxtLink>
                  </b-col>
                  <b-col md="6" style="cursor: default">
                    <div class="btn-follow">
                      <b-button>Follow</b-button>
                    </div>
                  </b-col>
                  <b-col md="12">
                    <div class="follow-info">
                      <p>
                        <span class="consume">{{ accB.follower }}M</span>
                        <span class="desc">Follower</span>
                      </p>
                      <p>
                        <span class="consume">{{ accB.like }}M</span>
                        <span class="desc">Thích</span>
                      </p>
                    </div>
                  </b-col>
                </b-row>
              </div>
            </li>
          </b-collapse>
          <span
            class="toogle-acc-recommend"
            v-b-toggle.collapse-a
            @click="toggleAccRecommend = !toggleAccRecommend"
            >{{ toggleAccRecommend ? "Xem tất cả" : "Ẩn bớt" }}</span
          >
        </ul>
      </div>

      <div class="sidebar_footer">
        <ul>
          <li>Giới thiệu</li>
          <li>Bảng tin</li>
          <li>Liên hệ</li>
          <li>Sự nghiệp</li>
          <li>ByteDance</li>
          <li>Tiktok for Good</li>
          <li>Quảng cáo</li>
          <li>Developers</li>
          <li>Transparency</li>
          <li>Tiktok Rewards</li>
        </ul>

        <p>Trang Web được Clone bởi nanglc</p>
      </div>
    </div>

    <div class="sidebar-mobile">
      <ul class="top">
        <li>
          <NuxtLink to="/forme">
            <b-icon icon="house-fill"> </b-icon>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/following">
            <b-icon icon="people"> </b-icon>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/live">
            <b-icon icon="camera-video"> </b-icon>
          </NuxtLink>
        </li>
      </ul>

      <ul class="bottom" v-if="recommendAccsT.length">
        <li v-for="(accMobile, i) in recommendAccsT" v-bind:key="i">
          <NuxtLink :to="'/@' + accMobile.username">
            <div class="acc">
              <img :src="accMobile.img" :alt="accMobile.name" />
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      recommendAccs: [
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 1",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 2",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 3",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 4",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 5",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 6",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 7",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 8",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
        {
          username: "hoaa.hanassii",
          name: "Đào Lê Phương Hoa 9",
          img: "https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png",
          follower: 17,
          like: 169,
        },
      ],
      recommendAccsT: [],
      recommendAccsB: [],
      toggleAccRecommend: true,
    };
  },
  mounted() {
    this.recommendAccsT = this.recommendAccs.slice(0, 5);
    this.recommendAccsB = this.recommendAccs.slice(5);
    console.log(this.recommendAccsT);
  },
};
</script>

<style lang="scss">
.sidebar-mobile {
  width: 80px;
  height: 100vh;
  position: fixed;
  margin-top: 60px;
  box-shadow: 5px 5px 14px -4px #ccc;

  .top {
    list-style: none;
    padding: 10px;
    margin: 0;

    li {
      display: flex;
      justify-content: center;
      align-items: center;

      &:last-child {
        border-bottom: 1px solid #f1f1f2;
      }
      a {
        padding: 10px;
        color: #111;

        &.nuxt-link-active {
          color: #fe2c55;
        }
        svg {
          font-size: 30px;
        }
      }
    }
  }

  .bottom {
    list-style: none;
    padding: 0;
    margin: 0;

    li {
      padding: 8px 20px;
      a {
        .acc {
          img {
            width: 40px;
            height: 40px;
            border-radius: 50%;
          }
        }
      }
    }
  }
}

@media only screen and (min-width: 1200px) {
  .sidebar-mobile {
    display: none;
  }
}
</style>
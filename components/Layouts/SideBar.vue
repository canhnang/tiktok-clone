<template>
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
        <li>
          <NuxtLink class="acc-info__item" to="/acc-pt">
            <div class="acc_img">
              <img
                src="https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png"
                alt=""
              />
            </div>
            <div class="desc">
              <span class="acc_link">hoaa.hanassii</span>
              <span class="acc_name">Đào Lê Phương Thoa</span>
            </div>
          </NuxtLink>
          <div class="acc-info__hover">
            <b-row>
              <b-col md="6">
                <NuxtLink to="/acc-pt">
                  <div class="img-hover">
                    <img
                      src="https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png"
                      alt=""
                    />
                  </div>
                  <div class="info-hover">
                    <h6 class="acc_link">hoaa.hanassii</h6>
                    <h6 class="acc_name">Đào Lê Phương Thoa</h6>
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
                    <span class="consume">17M</span>
                    <span class="desc">Follower</span>
                  </p>
                  <p>
                    <span class="consume">169.69M</span>
                    <span class="desc">Thích</span>
                  </p>
                </div>
              </b-col>
            </b-row>
          </div>
        </li>
        <li>
          <NuxtLink class="acc-info__item" to="/acc-pt">
            <div class="acc_img">
              <img
                src="https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png"
                alt=""
              />
            </div>
            <div class="desc">
              <span class="acc_link">hoaa.hanassii</span>
              <span class="acc_name">Đào Lê Phương Thoa</span>
            </div>
          </NuxtLink>
          <div class="acc-info__hover">
            <b-row>
              <b-col md="6">
                <NuxtLink to="/acc-pt">
                  <div class="img-hover">
                    <img
                      src="https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png"
                      alt=""
                    />
                  </div>
                  <div class="info-hover">
                    <h6 class="acc_link">hoaa.hanassii</h6>
                    <h6 class="acc_name">Đào Lê Phương Thoa</h6>
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
                    <span class="consume">17M</span>
                    <span class="desc">Follower</span>
                  </p>
                  <p>
                    <span class="consume">169.69M</span>
                    <span class="desc">Thích</span>
                  </p>
                </div>
              </b-col>
            </b-row>
          </div>
        </li>
        <li>
          <NuxtLink class="acc-info__item" to="/acc-pt">
            <div class="acc_img">
              <img
                src="https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png"
                alt=""
              />
            </div>
            <div class="desc">
              <span class="acc_link">hoaa.hanassii</span>
              <span class="acc_name">Đào Lê Phương Thoa</span>
            </div>
          </NuxtLink>
          <div class="acc-info__hover">
            <b-row>
              <b-col md="6">
                <NuxtLink to="/acc-pt">
                  <div class="img-hover">
                    <img
                      src="https://lf16-tiktok-common.ibytedtos.com/obj/tiktok-web-common-sg/mtact/static/images/share_img.png"
                      alt=""
                    />
                  </div>
                  <div class="info-hover">
                    <h6 class="acc_link">hoaa.hanassii</h6>
                    <h6 class="acc_name">Đào Lê Phương Thoa</h6>
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
                    <span class="consume">17M</span>
                    <span class="desc">Follower</span>
                  </p>
                  <p>
                    <span class="consume">169.69M</span>
                    <span class="desc">Thích</span>
                  </p>
                </div>
              </b-col>
            </b-row>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<style lang="scss">
</style>
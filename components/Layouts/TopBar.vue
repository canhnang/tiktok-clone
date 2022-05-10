<template>
  <div class="topbar">
    <b-container>
      <b-row>
        <b-col lg="4" md="2" sm="6" cols="2">
          <b-navbar-brand href="#">NavBar</b-navbar-brand>
        </b-col>
        <b-col lg="4" md="6" class="search-wrap">
          <div class="search-form">
            <b-form-input
              placeholder="Tìm kiếm tài khoản và video"
              class="search-form__input"
            />
            <b-button class="search-form-btn">
              <b-icon icon="search" class="search-form-icon"></b-icon>
            </b-button>
          </div>
        </b-col>
        <b-col lg="4" md="4" sm="6" cols="10">
          <div class="ml-auto top-bar-right">
            <!-- <b-button class="btn-icon" title="Tải video lên">
              <b-icon icon="cloud-arrow-up"></b-icon>
            </b-button>
            <b-button class="btn-icon" title="Tin nhắn">
              <b-icon icon="chat-dots"></b-icon>
            </b-button>
            <b-button class="btn-icon" title="Hộp thư">
              <b-icon icon="bell"></b-icon>
            </b-button>
            <div class="profile">
              <ul class="profile-info">
                <li class="profile-info_item">
                  <NuxtLink to="/"> Xem hồ sơ</NuxtLink>
                </li>
                <li class="profile-info_item">
                  <NuxtLink to="/"> Xem hồ sơ</NuxtLink>
                </li>
                <li class="profile-info_item">
                  <NuxtLink to="/"> Xem hồ sơ</NuxtLink>
                </li>
                <li class="profile-info_item">
                  <NuxtLink to="/"> Xem hồ sơ</NuxtLink>
                </li>
                <li class="profile-info_item">
                  <NuxtLink to="/"> Xem hồ sơ</NuxtLink>
                </li>
              </ul>
            </div> -->

            <div class="link-upload">
              <NuxtLink to="/">Tải lên</NuxtLink>
            </div>
            <b-button variant="danger" class="btn-default">Đăng nhập</b-button>
            <b-button class="btn-icon menu">
              <b-icon icon="three-dots-vertical"> </b-icon>
              <ul class="menu-select-hover">
                <li>
                  <b-icon icon="translate"> </b-icon>
                  Tiếng Việt
                </li>
                <li>
                  <b-icon icon="question-circle"> </b-icon>
                  <NuxtLink to="/feedback">Phản hồi và trợ giúp</NuxtLink>
                </li>
                <li>
                  <b-icon icon="keyboard"> </b-icon>
                  <NuxtLink to="/hotkey">Phím tắt trên bàn phím</NuxtLink>
                </li>
              </ul>
            </b-button>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>


<script>
export default {
  name: "TopBar",
};
</script>
<style lang="scss">
</style>
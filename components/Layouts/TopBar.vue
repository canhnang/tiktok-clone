<template>
  <div class="topbar">
    <b-container>
      <b-row>
        <b-col md="2" sm="6">
          <b-navbar-brand href="#">NavBar</b-navbar-brand>
        </b-col>
        <b-col md="6" class="search-wrap">
          <div class="search-form">
            <b-form-input
              placeholder="Tìm kiếm tài khoản và video"
              class="search-form_input"
            />
            <b-button class="search-form-btn">
              <b-icon icon="search" class="search-form-icon"></b-icon>
            </b-button>
          </div>
        </b-col>
        <b-col md="4" sm="6">
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
              </ul>
            </div> -->

            <div class="link-upload">
              <NuxtLink to="/">Tải lên</NuxtLink>
            </div>
            <b-button variant="danger" class="btn-default">Đăng nhập</b-button>
            <b-button class="btn-icon menu">
              <b-icon icon="three-dots-vertical"></b-icon>
              <ul class="menu-select-hover">
                <li>Tiếng Việt</li>
                <li>
                  <NuxtLink to="/feedback">Phản hồi và trợ giúp</NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/hotkey">Phím tắt trên bàn phím</NuxtLink>
                </li>
              </ul>
            </b-button>

            <!-- <b-nav-item-dropdown text="Lang">
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown> -->
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
<style scoped>
.topbar {
  height: 60px;
  width: 100%;
  top: 0;
  position: fixed;

  box-shadow: 0 1px 0 1px rgba(0, 0, 0, 0.15);
  display: flex;
  align-items: center;
}
/* seach */
.search-input {
  width: 360px;
}

.search-form {
  width: 360px;
  height: 46px;
  background-color: #f1f1f2;
  border-radius: 20px;
  position: relative;
  overflow: hidden;
}

.search-form_input {
  width: 300px;
  height: 40px;
  margin: 3px 0;
  background: transparent;
  padding: 0 20px;
  font-size: 18px;
  color: #666;
  border: none;
}

.search-form::after {
  content: "";
  top: 0;
  right: 60px;
  transform: translateY(calc((46px - 100%) / 2));
  position: absolute;
  width: 1px;
  height: 28px;
  background-color: #666;
}

.btn-icon:focus,
.search-form-btn:focus,
.search-form_input:focus {
  outline: none;
  -webkit-box-shadow: none;
  box-shadow: none;
  outline-style: none;
}

.search-form-btn {
  position: absolute;
  height: 100%;
  width: 60px;
  top: 0;
  color: #666;
  right: 0;
  transform: translateY(calc((46px - 100%) / 2));
  background-color: transparent;
  border: none;
}

.search-form-btn:hover {
  background-color: rgba(0, 0, 0, 0.05);
}

.search-form-icon {
  position: absolute;
  font-size: 18px;
  top: 0;
  color: #666;
  right: calc((60px - 18px) / 2);
  transform: translateY(calc((46px - 100%) / 2));
}
/* ------------- */
.link-upload {
  width: max-content;
  font-size: 22px;
  margin: auto 10px;
}
.btn-default {
  width: 110px;
  background-color: #fe2c55;
  font-size: 16px;
  font-weight: 500;
}
.top-bar-right {
  width: max-content;
  display: flex;
  justify-content: space-around;
}

.btn-icon {
  background-color: transparent;
  color: #111;
  font-size: 22px;
  border: none;
  margin: 0 2px;
}

.btn-icon.menu::after {
  position: absolute;
  content: "";
  width: 40px;
  height: 20px;
  top: calc(100% - 6px);
  right: 20px;
}
.btn-icon.menu:hover .menu-select-hover {
  display: block;
}

.menu-select-hover {
  position: absolute;
  width: 230px;
  top: calc(100% + 4px);
  right: 10px;

  background-color: #fff;
  border-radius: 3px;
  box-shadow: 0px 0px 0px 3px rgba(0, 0, 0, 0.15);
  list-style: none;
  padding: 10px 0;

  display: none;
}

.menu-select-hover li {
  padding: 8px 20px;
  font-size: 16px;
  font-weight: 600;
}

.menu-select-hover li:hover {
  background-color: #f8f8f8;
}

.menu-select-hover li a {
  color: #111;
  text-decoration: none;
}
.profile {
  width: 32px;
  height: 32px;
  border-radius: 50%;

  margin: auto 12px;
  background: #ffffff
    url("https://photocross.net/wp-content/uploads/2020/03/anh-chan-dung.jpg")
    no-repeat center;
  cursor: pointer;
}

.profile-info {
  position: absolute;
  width: 230px;
  height: 300px;
  top: 100%;
  right: 20px;

  border-radius: 4px;
  background-color: #fff;
  box-shadow: 0px 2px 9px 0px #ccc;
  display: none;
  list-style-type: none;
  padding: 0;
}

.profile:hover .profile-info {
  display: block;
}

.profile-info_item {
  padding: 4px 20px;
  background-color: #ccc;
}

.profile-info_item a {
  color: #111;
  font-size: 18px;
}

@media only screen and (max-width: 768px) {
  .search-wrap {
    display: none;
  }
}
</style>
<template>
  <nav class="navigation-02 yamm navbar navbar-inverse fill-black normal">
    <div class="container-fluid">
      <div class="navbar-header">
        <button
          type="button"
          class="navbar-toggle collapsed"
          data-toggle="collapse"
          data-target="#navbar-02"
          aria-expanded="false"
          aria-controls="navbar-02"
        >
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <nuxt-link class="navbar-brand" to="/">
          <strong class="mau-trang mt-5">TUYỂN BẢO VỆ VĨNH PHÚC</strong>
        </nuxt-link>
      </div>
      <div id="navbar-02" class="navbar-collapse collapse">
        <ul class="nav navbar-nav right">
          <li><nuxt-link to="/">Trang chủ</nuxt-link></li>
          <li><NuxtLink to="/tuyen-dung/">Tin tuyển dụng</NuxtLink></li>
          <li><nuxt-link to="/nop-ho-so-ung-tuyen/">Giới thiệu</nuxt-link></li>
          <li>
            <a
              class="btn btn-primary"
              target="_blank"
              href="https://zalo.me/0978333963"
              >Tư vấn</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

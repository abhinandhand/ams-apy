<template>
<div  class="page_header_wrapper ls affix-wrapper">
  <header id="navbar-content" class="page_header with-dots with-topline justify-nav-end  ls    s-overlay affix-top"
  >
    <div class="container">
      <div class="row align-items-center justify-content-xl-center">
        <div class="col-xl-2 col-md-7 col-10 hidden-above-xl">
          <a
            href=""
            rel="home"
            class="logo logo_image_only"
          >
            <img width="210px"
              class="logo-color"
              src="~/assets/images/icons/mobile-brand.svg"
              alt=""
            />
          </a>
        </div>
        <div class="col-xl-10 col-1 flex-menu">
          <nav class="top-nav" style="">
            <ul
              id="menu-main_menu"
              class="sf-menu nav sf-js-enabled sf-arrows"
              style="touch-action: pan-y;"
            >
              <li
                id="menu-item-8211"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-home menu-item-8211"
              >
                <a href="">Home</a>
              </li>
              <li
                id="menu-item-549"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-3496"
              >
                <a href="#" >About</a
                >
              </li>
              <li
                id="menu-item-1897"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-3496"
              >
                <a href="">Benefits</a>
              </li>
              <li
                id="menu-item-3496"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-3496"
              >
                <a href="">Pricing</a>
              </li>
              <li
                id="menu-item-3190"
                class="menu-item menu-item-type-post_type menu-item-object-page current_page_parent menu-item-3190"
              >
                <a href="">Lab</a>
              </li>
              <li
                id="menu-item-1899"
                class="menu-item menu-item-type-post_type menu-item-object-page menu-item-1899"
              >
                <a href=""
                  >Contact Us</a
                >
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
    <!-- header toggler -->
    <span id="bread-menu" @click="toggleSideNav" class="toggle_menu"><span></span></span>
  </header>
  </div>
</template>

<script>
export default {
    data(){
        return {
            sideNav: false
        }
    },
    mounted(){
      window.addEventListener('scroll', this.handleScroll);
    },
    destroyed(){
      window.removeEventListener('scroll', this.handleScroll);
    },
    methods :{
        toggleSideNav(){
            if(!this.sideNav){
                document.getElementsByTagName('HEADER')[0].classList.add('mobile-active');
                document.getElementById('bread-menu').classList.add('mobile-active');
            } else{
                document.getElementsByTagName('HEADER')[0].classList.remove('mobile-active');
                document.getElementById('bread-menu').classList.remove('mobile-active');
            }
            this.sideNav = !this.sideNav;
        },
        handleScroll (event) {
          if( document.body.clientWidth < 1200){

          let headerHeight = document.getElementById('header').clientHeight;
          if(document.scrollingElement.scrollTop > headerHeight){
            document.getElementById('navbar-content').classList.add('affix');
            document.getElementById('navbar-content').classList.remove('affix-top');
          }else{
            document.getElementById('navbar-content').classList.remove('affix');
            document.getElementById('navbar-content').classList.add('affix-top');
          }
          }
    }
    }
};
</script>

<style lang="scss">
header {
  height: 60px;
}
.ls {
    background-color: #fff;
    color: #5c6f87;
}
.flex-menu {
  @media (min-width: 1200px){
    display: flex;
    align-items: center;
  }
}

.top-nav {
    @media (min-width: 1200px) {
    position: relative;
    flex-grow: 10;
    flex-wrap: nowrap;
    display: flex;
    align-items: center;
    }
}

/*
 ** WordPress Page Links and Pagination
 */
.ds .page-item > span, .ds .nav-links > span, .ds .page-links > span, .ds .page-item > a:not(.btn), .ds .nav-links > a:not(.btn), .ds .page-links > a:not(.btn) {
  color: #fff;
  border-color: rgba(255, 255, 255, .5);
}
.item-content .page-item, .item-content .nav-links, .item-content .page-links {
  justify-content: flex-start;
}
.item-content .page-item a:first-child, .item-content .nav-links a:first-child, .item-content .page-links a:first-child {
  margin-left: 0;
}
.page-item, .nav-links, .page-links {
  clear: both;
  display: flex;
  align-items: center;
  justify-content: center;
}
.page-item > span, .nav-links > span, .page-links > span, .page-item > a:not(.btn), .nav-links > a:not(.btn), .page-links > a:not(.btn) {
  display: flex;
  align-items: center;
  justify-content: center;
  color: #141d28;
  background-color: transparent;
  margin-right: 5px;
  margin-bottom: 10px;
  margin-left: 0;
  text-align: center;
  font-size: 16px;
  width: 40px;
  height: 40px;
  border-radius: 0;
  border: 1px solid rgba(20, 29, 40, 0.1);
}
.page-item > span:hover, .nav-links > span:hover, .page-links > span:hover, .page-item > a:not(.btn):hover, .nav-links > a:not(.btn):hover, .page-links > a:not(.btn):hover {
  background-color: #079d66;
}
@media (max-width: 768px) {
  .page-item > span, .nav-links > span, .page-links > span, .page-item > a:not(.btn), .nav-links > a:not(.btn), .page-links > a:not(.btn) {
    height: 45px;
    line-height: 15px;
    padding: 1.3em 1.2em;
    width: 45px;
  }
}
.page-item.active > a, .nav-links.active > a, .page-links.active > a, .page-item.active > .page-link, .nav-links.active > .page-link, .page-links.active > .page-link, .page-item > .current, .nav-links > .current, .page-links > .current {
  background-color: #079d66;
  cursor: not-allowed;
  color: #141d28;
}
.page-item > span:not(.current), .nav-links > span:not(.current), .page-links > span:not(.current) {
  pointer-events: none;
}
.page-item .fa, .nav-links .fa, .page-links .fa {
  font-size: 10px;
}
.page-links-title {
  width: auto !important;
  padding: 0 10px !important;
}
.page-links a:first-child {
  margin-left: 1em;
}
.pagination {
  justify-content: center;
  margin-bottom: -10px;
  margin-top: 65px;
}
.post-nav {
  margin: 60px 0 0;
  position: relative;
}
.post-nav .nav-links {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.post-nav .nav-links > div {
  width: 49%;
  height: auto;
  position: relative;
  padding: 30px;
  text-align: right;
  background-position: 50% 28%;
  transition: 0.2s opacity ease;
}
.post-nav .nav-links > div:hover {
  opacity: 0.9;
}
@media (max-width: 575px) {
  .post-nav .nav-links > div {
    width: 100%;
  }
  .post-nav .nav-links > div:first-child {
    margin-bottom: 30px;
  }
}
.post-nav .nav-links > div .fa {
  font-size: 20px;
  position: absolute;
  top: 50%;
  right: 0;
  transform: translateY(-50%);
}
.post-nav .nav-links > div:first-child {
  text-align: left;
}
.post-nav .nav-links > div:first-child .fa {
  right: auto;
  left: 0;
}
.post-nav .nav-links .nav-subtitle {
  font-style: normal;
  text-align: center;
  text-transform: capitalize;
  font-size: 16px;
  font-weight: 300;
  line-height: 1;
  text-align: center;
  min-width: 8em;
  padding: 0.25em 0.8em 0.05em;
  display: inline-block;
}
.post-nav .nav-links .nav-title {
  font-size: 20px;
  display: block;
  margin-top: 4px;
  text-transform: capitalize;
  line-height: 1.3;
  margin-bottom: 5px;
  text-transform: uppercase;
}
.post-nav .nav-links a {
  content: '';
  position: absolute;
  display: block;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.post-nav .post-nav-image {
  display: none;
}
.post-nav .cover-image .post-nav-text-wrap {
  text-align: center;
}
/*
 ** Main Menu styles
 */
.nav-wrap {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.nav-wrap > .top-nav + *:not(.top-includes) {
  padding-left: 30px;
  padding-right: 30px;
}
/* Desktop menu - (min 1200px) styles */
@media (min-width: 1200px) {
  /* menu layout */
  /* menu skin */
  /* second and next levels */
  /* third level */
  .left .top-nav {
    justify-content: flex-start !important;
  }
  .top-nav {
    position: relative;
    flex-grow: 10;
    flex-wrap: nowrap;
    display: flex;
    align-items: center;
  }
  .justify-nav-end .top-nav {
    justify-content: flex-end;
  }
  .justify-nav-center .top-nav {
    justify-content: center;
  }
  .top-nav ul > li {
    position: relative;
  }
  .top-nav ul > li .sf-with-ul {
    position: relative;
  }
  .top-nav ul > li .sf-with-ul::after {
    position: relative;
    content: '\f0d7';
    font-family: "FontAwesome", sans-serif;
    margin-left: 8px;
    display: inline-block;
    font-weight: bold;
    font-size: 16px;
  }
  .top-nav ul > li ul li .sf-menu-item-mobile-toggler::before {
    content: none;
  }
  .sf-menu {
    display: block;
  }
  .sf-menu, .sf-menu ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  .sf-menu li {
    position: relative;
  }
  .sf-menu li:first-child > ul {
    left: 0;
  }
  .sf-menu li > ul {
    position: absolute;
    display: none;
    top: 100%;
    left: 18px;
    z-index: 99;
  }
  .sf-menu li:hover > ul, .sf-menu li.sfHover > ul {
    display: block;
  }
  .sf-menu a {
    display: block;
    position: relative;
  }
  .sf-menu a {
    color: #141d28;
    padding: 5px 1.1em;
    text-decoration: none;
    text-align: left;
    zoom: 1;
    transition-property: color, background-color, border-color, padding-top, padding-bottom;
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 0.8px;
    line-height: 25px;
  }
  .sf-menu li {
    *white-space: normal;
  }
  .sf-menu > li {
    display: inline-block;
    position: relative;
  }
  .hover-2 .sf-menu > li > a::before {
    top: auto;
    bottom: 0;
  }
  .with-dots.with-topline .sf-menu > li:not(:last-child)::after {
    right: -18px;
  }
  .with-dots.with-topline .sf-menu > li > a {
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .with-dots.with-topline .sf-menu > li .mega-menu, .with-dots.with-topline .sf-menu > li > ul {
    margin-top: 2px !important;
  }
  .with-dots .sf-menu > li:not(:last-child)::after {
    content: '';
    display: inline-block;
    width: 4px;
    height: 4px;
    background-color: #141d28;
    position: absolute;
    top: 50%;
    transform: translateY(-100%);
    right: 0;
    border-radius: 50%;
  }
  .with-dots .sf-menu > li > a.sf-with-ul::after {
    content: '\f078';
    font-size: 10px;
    bottom: 2px;
  }
  .with-dots .sf-menu > li > a::before {
    display: none;
  }
  .without-dots.with-topline .sf-menu > li:not(:last-child)::after {
    right: -18px;
  }
  .without-dots.with-topline .sf-menu > li > a {
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .without-dots.with-topline .sf-menu > li .mega-menu, .without-dots.with-topline .sf-menu > li > ul {
    margin-top: 2px !important;
  }
  .without-dots .sf-menu > li > a.sf-with-ul::after {
    content: '\f078';
    font-size: 10px;
    bottom: 2px;
  }
  .without-dots .sf-menu > li > a::before {
    display: none;
  }
  .sf-menu > li > a {
    line-height: 14px;
    padding-top: 40px;
    padding-bottom: 40px;
    padding-right: 0;
    padding-left: 0;
    margin: 0 15px;
    transition-duration: 0.15s;
    position: relative;
  }
  .sf-menu > li > a::before {
    content: '';
    position: absolute;
    display: inline-block;
    top: 0;
    left: 50%;
    right: 50%;
    height: 2px;
    background-color: transparent;
    transition: all 0.3s ease-in-out;
  }
  .affix .sf-menu > li > a {
    padding-top: 30px;
    padding-bottom: 30px;
  }
  .sf-menu > li > a:hover, .sf-menu > li.active > a {
    color: #079d66;
  }
  .sf-menu > li > a:hover::before, .sf-menu > li.active > a::before {
    left: 0;
    right: 0;
    background-color: #079d66;
  }
  .nav-narrow .sf-menu > li {
    padding: 0;
  }
  .nav-narrow .sf-menu > li > a {
    padding-top: 24px;
    padding-bottom: 24px;
    margin-left: 29px;
    margin-right: 29px;
  }
  .nav-narrow .sf-menu > li.active > a:before {
    content: '';
    position: absolute;
    height: 1px;
    left: -20px;
    right: -20px;
    top: 0;
    z-index: 1;
    background-color: #079d66;
  }
  .nav-bordered .sf-menu > li + li:before {
    content: '';
    width: 1px;
    position: absolute;
    left: -2px;
    top: 0;
    bottom: 0;
    background-color: rgba(255, 255, 255, 0.15);
  }
  .cs .sf-menu > li > a {
    color: #fff;
  }
  .cs .sf-menu > li > a:hover, .cs .sf-menu > li.active > a {
    color: #141d28;
  }
  .ds .sf-menu > li > a {
    color: #fff;
  }
  .ds .sf-menu > li > a:hover, .ds .sf-menu > li.active > a {
    color: #079d66;
  }
  .ds .sf-menu > li.active .sf-menu-item-mobile-toggler::before, .ds .sf-menu > li.sfHover .sf-menu-item-mobile-toggler::before {
    color: #079d66;
  }
  .ls .sf-menu > li > a {
    color: #141d28;
  }
  .ls .sf-menu > li > a:hover, .ls .sf-menu > li.active > a {
    color: #079d66;
  }
  .ls .sf-menu > li > a:hover::before, .ls .sf-menu > li.active > a::before {
    color: #079d66;
  }
  .ls .sf-menu > li + li:before {
    background-color: rgba(20, 29, 40, 0.1);
  }
  .sf-menu li:hover, .sf-menu li.sfHover {
    /* only transition out, not in */
    -webkit-transition: none;
    transition: none;
  }
  .sf-menu > li .mega-menu, .sf-menu li > ul {
    margin-top: -15px !important;
    box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.15);
    text-align: center;
    list-style: none;
    padding-top: 38px;
    padding-bottom: 38px;
    background-color: #fff;
    min-width: 19em;
    /* allow long menu items to determine submenu width */
    max-width: 19em;
    *width: 19em;
    /* no auto sub width for IE7, see white-space comment below */
  }
  .sf-menu > li .mega-menu li, .sf-menu li > ul li {
    padding-right: 48px;
    padding-left: 48px;
  }
  .sf-menu > li .mega-menu li.mega-menu-col, .sf-menu li > ul li.mega-menu-col {
    padding: 0;
  }
  .sf-menu > li .mega-menu li.mega-menu-col > a, .sf-menu li > ul li.mega-menu-col > a {
    border: none;
  }
  .sf-menu > li .mega-menu li a, .sf-menu li > ul li a {
    padding-right: 0;
    padding-left: 0;
    display: block;
  }
  .sf-menu > li .mega-menu {
    max-width: unset;
  }
  .sf-menu > li .mega-menu {
    padding-left: 0;
    padding-right: 0;
  }
  .sf-menu.nav ul a {
    padding-left: 0;
    padding-right: 0;
    color: #141d28;
  }
  .sf-menu .mega-menu ul {
    box-shadow: none;
    padding: 0;
    background: transparent;
  }
  .sf-menu .mega-menu ul a {
    padding-left: 0;
    padding-right: 0;
    color: #141d28;
  }
  .sf-menu ul a:hover, .sf-menu ul li.active > a {
    color: #079d66 !important;
  }
  .sf-menu ul ul {
    margin-top: 0;
    top: -23px;
    transform: none;
    margin-left: 2px;
    right: 0;
  }
}
@media (min-width: 1200px) and (min-width: 1500px) {
  .sf-menu > li > a {
    margin: 0 25px;
  }
}
.sf-menu i[class] {
  margin-right: 7px;
  font-size: 1.1em;
}
/* hidden menu items */
@media (min-width: 1200px) {
  .sf-menu .sf-xl-hidden {
    display: none !important;
  }
}
@media (max-width: 1199px) {
  .sf-more-li {
    display: none;
  }
}
/* Mobile menu toggler */
@media (min-width: 1200px) {
  .page_header .toggle_menu, .page_toplogo .toggle_menu {
    display: none;
  }
  .page_header .toggle_menu.active::before, .page_toplogo .toggle_menu.active::before, .page_header .toggle_menu.mobile-active::before, .page_toplogo .toggle_menu.mobile-active::before {
    transform: none;
  }
}
.page_header_side_special .toggle_menu_side {
  background-color: transparent !important;
}
.page_header_side_special .toggle_menu::before {
  width: 17px;
  height: 17px;
  background: url("/images/icon-menu.png") no-repeat center / contain;
  background-color: transparent !important;
}
.toggle_menu {
  position: absolute;
  top: 50%;
  right: 0;
  margin-left: -30px;
  margin-top: -30px;
  padding: 0 !important;
  width: 60px;
  height: 60px;
  cursor: pointer;
  z-index: 1002;
  visibility: visible;
  opacity: 0.95;
}
.page_header_wrapper .toggle_menu {
  z-index: 1003;
}
.ls .toggle_menu {
  background-color: #fff;
}
.ls .toggle_menu:before, .ls .toggle_menu span, .ls .toggle_menu span:before, .ls .toggle_menu span:after {
  background-color: #141d28;
}
.page_toplogo .toggle_menu {
  position: fixed;
  top: 0;
  left: auto;
  right: 0;
  margin: 0;
}
.toggle_menu:hover span:before {
  top: -9px;
}
.toggle_menu:hover span:after {
  top: 9px;
}
.toggle_menu:before, .toggle_menu span, .toggle_menu span:before, .toggle_menu span:after {
  display: block;
  width: 30px;
  position: absolute;
  background-color: #fff;
  content: '';
  left: 0;
  transform: rotate(0deg);
  transition: 0.25s ease-in-out;
  height: 2px;
}
.toggle_menu:before, .toggle_menu span {
  left: 15px;
  top: 50%;
}
.toggle_menu span:before {
  opacity: 1;
  top: -8px;
}
.toggle_menu span:after {
  opacity: 1;
  top: 8px;
}
.toggle_menu.mobile-active {
  background: #079d66;
  border: none;
  left: auto;
  top: 0;
  right: 0;
  position: fixed;
  margin: 0;
  z-index: 3000;
}
.toggle_menu.mobile-active:before {
  background-color: #fff;
  transform: rotate(45deg);
}
.toggle_menu.mobile-active span {
  background-color: #fff;
  transform: rotate(-45deg);
}
.toggle_menu.mobile-active span:before, .toggle_menu.mobile-active span:after {
  opacity: 0;
}
.toggle_menu.active:before {
  transform: rotate(45deg);
}
.toggle_menu.active span {
  transform: rotate(-45deg);
}
.toggle_menu.active span:before, .toggle_menu.active span:after {
  opacity: 0;
}
/* Mobile Menu (max 991px) styles */
@media (max-width: 767px) {
  .nav-wrap {
    justify-content: space-between;
  }
}
@media (max-width: 1199px) {
  /* arrows (for all except IE7) */
  /* styling for both css and generated arrows */
  .page_header [class*="col"] {
    min-height: 0;
  }
  .top-nav {
    position: fixed;
    visibility: hidden;
    z-index: 10;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    background-color: transparent;
    opacity: 0;
    transition: all 0.3s ease-in-out;
  }
  .mobile-active .top-nav {
    visibility: visible;
    opacity: 1;
    background-color: #111;
    background-color: rgba(0, 0, 0, 0.9);
    z-index: 1002;
  }
  .nav-justified > li > a {
    text-align: left;
  }
  .sf-menu {
    display: block;
    position: fixed;
    overflow: auto;
    background-color: #f8f8f9;
    border-top: 61px solid #141d28;
    padding: 20px 10px;
    top: 0;
    left: 0;
    bottom: 0;
    right: 100%;
    text-align: left;
    font-style: normal;
    text-align: center;
    text-transform: capitalize;
    font-size: 16px;
    font-weight: 300;
    line-height: 1;
    font-size: 14px;
    opacity: 0;
    transition: all 0.4s ease-in-out;
  }
  .sf-menu .sfHover a {
    font-size: 12px;
  }
  .sf-menu .sfHover > a {
    font-size: 14px;
  }
  .mobile-active .sf-menu {
    opacity: 1;
    right: 0;
  }
  .sf-menu li {
    position: relative;
    text-align: left;
  }
  .top-nav .sf-menu a {
    color: #141d28;
    z-index: 2;
    display: block;
    padding: 7px 10px;
    font-size: 18px;
  }
  .top-nav .sf-menu a:hover {
    color: #079d66;
  }
  .sf-menu ul {
    list-style: none;
    margin-top: 0 !important;
    margin-left: 20px;
  }
  .top-nav .sf-menu ul li a {
    font-weight: 400;
    letter-spacing: 0.1em;
    font-size: 16px;
  }
  .sf-arrows .sf-with-ul {
    padding-right: 3.5em;
  }
  .sf-arrows .sf-with-ul + .sf-menu-item-mobile-toggler {
    position: absolute;
    right: 5px;
    top: 5px;
    width: 30px;
    height: 30px;
    line-height: 30px;
    border-radius: 50%;
    text-align: center;
    z-index: 1;
  }
  .sf-arrows .sf-with-ul + .sf-menu-item-mobile-toggler:after {
    font-family: "FontAwesome", sans-serif;
    content: '\f105';
    color: #141d28;
    font-weight: 700;
  }
  .sfHover > .sf-with-ul + .sf-menu-item-mobile-toggler:after {
    content: '\f107';
  }
}
/* Mega Menu */
@media screen and (min-width: 1199px) {
  /* row */
  /* column */
  .top-nav ul .mega-menu ul {
    border: none;
    min-width: auto;
  }
  .top-nav .menu-item-has-mega-menu {
    position: relative;
  }
  .top-nav .mega-menu {
    display: none;
    position: absolute;
    width: 940px;
    top: 100%;
    z-index: 10;
  }
  .top-nav .menu-item-has-mega-menu:hover .mega-menu {
    display: block;
  }
  .top-nav .mega-menu-row {
    position: static;
    display: table;
    table-layout: fixed;
  }
  .top-nav .mega-menu-row ul {
    position: static;
    display: block;
  }
  .top-nav .mega-menu-col {
    display: table-cell;
    width: 2000px;
    padding: 0 15px;
    border-left: 1px solid rgba(20, 29, 40, 0.1);
    /* overrides from settings / styling / mega-menu */
  }
  .top-nav .mega-menu-col > a {
    padding-left: 40px !important;
    margin-bottom: 20px;
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    text-transform: uppercase;
    font-weight: 700 !important;
    letter-spacing: 0.05em;
  }
  .top-nav .mega-menu-col:first-child {
    border-left: none;
  }
  .top-nav ul ul .mega-menu {
    width: auto;
    top: -20px;
    margin-left: 1px;
    display: block;
  }
  .top-nav ul ul .mega-menu li {
    display: block;
    width: auto;
    border: none;
  }
}
@media screen and (min-width: 1200px) {
  .top-nav .mega-menu {
    width: 1170px;
  }
  .top-nav ul .mega-menu ul {
    min-width: 10em;
  }
  .top-nav .mega-menu-col {
    padding: 0 40px;
  }
}
@media screen and (max-width: 991px) {
  .top-nav .mega-menu {
    position: static;
  }
}
/* side clickable menu styles */
.page_header_side_special .menu-click a {
  text-transform: capitalize;
  font-size: 16px;
  text-align: left;
  font-weight: 400;
  padding-top: 27px;
  padding-bottom: 27px;
}
.page_header_side_special .menu-click a:hover {
  background-color: transparent;
}
.page_header_side_special .menu-click > li {
  border-top: 1px solid rgba(20, 29, 40, .1);
}
.page_header_side_special .menu-click > li ul li a {
  padding-left: 40px;
  color: #b3b3b3;
  padding-top: 17px;
  padding-bottom: 17px;
}
.page_header_side_special .menu-click > li ul li:last-child a {
  padding-bottom: 27px;
}
.page_header_side_special .menu-click .active-submenu > a {
  background-color: transparent;
  padding-bottom: 17px;
}
.ds .menu-click .toggle_submenu:before {
  color: #fff;
}
.menu-click {
  padding: 0;
}
.menu-click i {
  width: 1em;
  text-align: center;
  margin-right: 10px;
}
.menu-click li .toggle_submenu {
  top: 8px;
}
.menu-click li li .toggle_submenu {
  top: 6px;
}
.menu-click .toggle_submenu {
  cursor: pointer;
  position: absolute;
  right: 20px;
  font-size: 8px;
  text-align: center;
  opacity: 0.9;
  border-radius: 50%;
  width: 3em;
  height: 3em;
  line-height: 3em;
}
.menu-click .toggle_submenu:before {
  content: '\f078';
  font-family: 'FontAwesome';
  top: 0;
  left: 0;
  position: absolute;
  width: 3em;
  height: 3em;
  line-height: 3em;
  transition: 0.25s ease-in-out;
  font-weight: 700;
}
.menu-click .toggle_submenu .toggle_submenu {
  top: 8px;
}
.menu-click ul {
  padding: 0;
}
.menu-click li {
  position: relative;
  list-style: none;
  width: 100%;
}
.menu-click > li {
  transition: 0.3s ease-in-out;
}
.menu-click a {
  display: block;
  padding: 10px 40px;
  font-style: normal;
  text-align: center;
  text-transform: capitalize;
  font-size: 16px;
  font-weight: 300;
  line-height: 1;
}
.menu-click a:hover {
  background-color: rgba(150, 150, 150, 0.05);
}
.menu-click .active-submenu > a {
  background-color: rgba(150, 150, 150, 0.05);
}
.menu-click .active-submenu > .toggle_submenu::before {
  transform: rotate(90deg);
}
.menu-click li.active > a {
  color: #079d66;
}
.menu-click ul {
  opacity: 0;
  height: 0;
}
.menu-click ul a {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 50px;
}
.menu-click ul ul a {
  padding-left: 60px;
}
.menu-click ul ul ul a {
  padding-left: 70px;
}
.menu-click ul ul ul ul a {
  padding-left: 80px;
}
.menu-click .active-submenu > div.mega-menu {
  height: auto;
}
.menu-click .active-submenu > ul, .menu-click .active-submenu > div.mega-menu > ul {
  opacity: 1;
  height: auto;
}
.menu-click ul, .menu-click div.mega-menu {
  height: 0;
  overflow: hidden;
  transition: opacity 0.6s, margin-top 0.4s, margin-bottom 0.4s, height 0.3s ease-in-out;
}
.menu-click ul li.sfHover > .mega-menu ul {
  display: block;
  height: 100%;
}
.menu-click div.mega-menu > ul {
  margin-right: 0;
  height: auto;
}
/*
 ** Header
 */
.page_header {
  /* transition: 0.5s ease-in-out; */
  position: relative;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  z-index: 1000;
  margin: 0;
  padding: 0;
  height: auto;
}
.page_header a.fab {
  color: #5c6f87;
}
.boxed .page_header, .page_header.affix {
  position: fixed !important;
  z-index: 1001;
  box-shadow: 0 0 5px 0 rgba(0, 0, 0, 0.15);
  opacity: 0.98;
}
.boxed .page_header:after, .page_header.affix:after {
  background-color: transparent;
}
.page_header.affix.s-bordertop::before {
  display: none;
}
@media (max-width: 991px) {
  .page_header.mobile-active {
    z-index: 1003;
    opacity: 1;
  }
}
.page_header.affix-bottom {
  top: 0 !important;
  position: fixed;
}
.page_header .row {
  min-height: 60px;
}
@media (max-width: 1199px) {
  .page_header .row {
    min-height: 80px;
  }
}
.page_header a {
  display: inline-block;
}
.page_header .btn {
  margin-bottom: 0;
}
.page_topline.church {
  color: #ababaa;
}
.page_topline.church a:not(.btn) {
  color: #ababaa;
}
.page_topline.church a:not(.btn):hover {
  color: #fff;
}
.page_header_wrapper .color-change.only_color_logo .logo-color {
  display: inline-block !important;
}
.page_header_wrapper .color-change.only_color_logo .logo-white {
  display: none;
}
.page_header_wrapper .color-change.ds .logo-color {
  display: none;
}
.page_header_wrapper .color-change.ls .logo-white {
  display: none;
}
.header_absolute {
  position: absolute;
  left: 0;
  right: 0;
}
.header_absolute .page_header, .header_absolute .page_topline, .header_absolute .page_header_wrapper {
  z-index: 1002;
  position: absolute;
  right: 0;
  left: 0;
}
.header_absolute .page_topline, .header_absolute .page_toplogo, .header_absolute .page_header_wrapper, .header_absolute .page_title {
  background-color: transparent;
}
.header_absolute .page_topline.ds.church, .header_absolute .page_toplogo.ds.church {
  background-color: rgba(20, 29, 40, .6);
  border: none;
}
.header_absolute .page_topline.ls.church, .header_absolute .page_toplogo.ls.church {
  background-color: rgba(255, 255, 255, .6);
  border: none;
}
#canvas:not(.boxed) .header_absolute .page_header.affix-top {
  background-color: transparent;
}
#canvas:not(.boxed) .header_absolute .page_header.affix-top.ds.church {
  background-color: rgba(20, 29, 40, .4);
  border: none;
}
#canvas:not(.boxed) .header_absolute .page_header.affix-top.ls.church {
  background-color: rgba(255, 255, 255, .4);
  border: none;
}
@media (min-width: 1200px) {
  .flex-menu {
    display: flex;
    align-items: center;
  }
  .flex-menu .nav {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
  }
  .flex-menu.justify-nav-end .nav {
    justify-content: flex-end;
  }
  .flex-menu.justify-nav-start .nav {
    justify-content: flex-start;
  }
}
@media (min-width: 1200px) {
  .default-header .sf-menu > li > a {
    padding-top: 20px;
    padding-bottom: 20px;
  }
}
.page_header .header-icons a, .page_topline .header-icons a {
  font-size: 14px;
  line-height: 1;
  padding: 0;
}
.page_header .header-icons a:not(:last-child), .page_topline .header-icons a:not(:last-child) {
  margin-right: 20px;
}
.page_header .social-icons a.fab:not(:last-child), .page_topline .social-icons a.fab:not(:last-child), .page_header .social-icons a.fas:not(:last-child), .page_topline .social-icons a.fas:not(:last-child), .page_header .social-icons a.far:not(:last-child), .page_topline .social-icons a.far:not(:last-child) {
  margin-right: 15px;
}
.page_topline div > span {
  display: inline-block;
}
.page_topline.small-text i {
  font-size: 14px;
}
.page_topline .icon-inline {
  justify-content: center;
}
.page_topline .icon-inline > .icon-styled:first-child {
  margin-right: 7px;
}
.page_topline .icon-inline + .icon-inline {
  margin-left: 23px;
}
@media (max-width: 430px) {
  .page_topline .icon-inline + .icon-inline {
    margin-left: 0;
  }
}
.page_topline .social-icons {
  display: inline-block;
  font-weight: 400;
}
.page_topline .header_info_text {
  color: #fff;
  font-weight: 500;
  position: relative;
}
.page_topline .header_info_text::after {
  content: "\f0d7";
  font-family: FontAwesome;
  position: absolute;
  bottom: -16px;
  right: 50%;
  transition: top 0.2s ease 0s;
}
@media (max-width: 767px) {
  .page_topline [class*="col-"] {
    margin: 0;
  }
}
.page_topline .widget_nav_menu {
  display: inline-block;
}
.page_topline ul {
  margin: 0;
  padding: 0;
}
.page_topline ul li {
  display: inline-block;
}
.page_topline .dropdown-menu {
  margin: 23px 0 0 -25px;
  min-width: auto;
}
.page_topline .dropdown-language a > img {
  max-width: 16px;
  position: relative;
  bottom: 1px;
  margin-right: 6px;
}
.page_topline .owl-news-slider-dates {
  font-weight: 300;
}
.page_topline .topline-news-item {
  font-weight: 300;
  height: 2em;
  line-height: 2em;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  margin: 0 90px;
}
.page_topline .topline-news-item .cat-links {
  display: inline;
}
.page_topline .topline-news-nav-arrow {
  border: 3px solid #3b6291;
  font-size: 10px;
  position: relative;
  bottom: 20px;
  line-height: 34px;
  width: 40px;
  transition: opacity 0.2s ease-in-out;
}
.page_topline .topline-news-nav-arrow:hover {
  opacity: 0.8;
}
.page_topline .owl-nav > div {
  opacity: 1;
}
@media (min-width: 992px) {
  .page_toplogo .media + .media {
    margin-left: 60px;
  }
}
.page_toplogo .widget_search form, .page_toplogo .widget_product_search form, .page_toplogo .widget_search input, .page_toplogo .widget_product_search input {
  max-width: none;
}
@media (max-width: 991px) {
  .page_toplogo .media {
    margin: 10px;
  }
}
@media (min-width: 1500px) {
  .page_topline .container-fluid, .page_toplogo .container-fluid, .page_header .container-fluid {
    padding-left: 60px;
    padding-right: 60px;
  }
}

</style>
 
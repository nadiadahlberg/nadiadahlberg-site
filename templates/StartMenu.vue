<template>
  <div class="menu" style="z-index: 1000000">
    <div class="sidebar">
      <img class="sidebar-image" src="@/assets/sidebar-image.png" />
    </div>

    <div class="socials">

      <a href="https://www.instagram.com/nadiasagadahlberg/" target="_blank">
        <div class="bar">
          <img class="social-image" src="@/assets/iPhone-Icons/Instagram.webp" />
          <div class="social-text"><u>I</u>nstagram</div>
        </div>
      </a>

      <a href="https://www.reddit.com/user/satoshigekkouga2303" target="_blank">
        <div class="bar">
          <img class="social-image" src="@/assets/iPhone-Icons/Reddit.webp" />
          <div class="social-text"><u>R</u>eddit</div>
        </div>
      </a>

      <a href="https://www.linkedin.com/" target="_blank">
        <div class="bar">
          <img class="social-image" src="@/assets/iPhone-Icons/Linkedin.webp" />
          <div class="social-text"><u>L</u>inkedIn</div>
        </div>
      </a>

      <a href="https://twitter.com/" target="_blank">
        <div class="bar">
          <img class="social-image" src="@/assets/iPhone-Icons/Twitter.webp" />
          <div class="social-text"><u>T</u>witter</div>
        </div>
      </a>

      <a href="https://github.com/nadiadahlberg" target="_blank">
        <div class="bar">
          <img class="social-image" src="@/assets/iPhone-Icons/Github.webp" />
          <div class="social-text"><u>G</u>itHub</div>
        </div>
      </a>

      <div class="divider"></div>

      <a href="/files/resume.pdf" target="_blank">
        <div class="bar">
          <img class="social-image" src="@/assets/win95Icons/resume.png" />
          <div class="social-text"><u>R</u>ésumé</div>
        </div>
      </a>

    </div>
  </div>
</template>

<style scoped>
.menu {
  width: 165px;
  height: 282px;
  background: rgb(195, 195, 195);
  overflow: hidden;
  border-top: solid rgb(250, 250, 250) 2px;
  border-left: solid rgb(250, 250, 250) 2px;
  border-right: solid rgb(90, 90, 90) 1.5px;
  border-bottom: solid rgb(90, 90, 90) 1.5px;
  box-shadow: 1.5px 1.5px black;
  max-height: 100%;
  max-width: 100%;
  outline: rgb(222, 222, 222) 1px solid;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  font-size: 12px;
}

a {
  color: black;
  text-decoration: none;
}

.sidebar {
  width: 25px;
  background: rgb(123, 125, 123);
  height: 100%;
  display: flex;
  align-items: flex-end;
}

.sidebar-image {
  width: 100%;
}

.divider {
  width: 100%;
  height: 1px;
  background: rgb(123, 125, 123);
  border-bottom: white solid 1px;
}

.socials {
  flex-grow: 1;
}

.social-image {
  width: 30px;
  height: 30px;
  margin-right: 10px;
  border-radius: 6px;
}

.social-text {
  display: flex;
  align-items: center;
}

.bar {
  display: flex;
  flex-direction: row;
  padding: 5px 10px 5px 10px;
  align-items: center;
}

.bar:hover {
  background: rgb(0, 0, 118);
  color: white;
}
</style>

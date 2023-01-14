<script setup></script>

<template>
  <div class="kk-footer">
    <p class="kk-footer__subhl">KAPPES</p>
    <div class="kk-footer__links">
      <div class="kk-footer__social">
        <a href="mailto:kappes-kimchi@gmx.de" target="_blank">
          <img src="../assets/social_icons/mail_icon.svg" class="social-mail" />
        </a>
        <a href="https://www.instagram.com/kappes_kimchi/" target="_blank">
          <img
            src="../assets/social_icons/insta_icon.svg"
            class="social-insta"
          />
        </a>
      </div>
      <button class="kk-footer__legal">IMPRESSUM</button>
    </div>
    <div class="kk-footer__placeholder"></div>
  </div>
</template>

<style lang="scss">
.kk-footer {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #fff;

  @media screen and (min-width: 768px) {
    flex-direction: row;
  }

  &__subhl {
    font-family: "Revive80Phatt", sans-serif;
    font-size: 16px;
    margin-top: 10px;
    color: #181818;

    @media screen and (min-width: 768px) {
      font-size: 22px;
      margin-left: 30px;
      flex: 1;
    }
  }

  &__links {
    display: flex;
    flex-direction: column;
    align-items: center;

    &__social {
      display: flex;
    }
  }

  &__legal {
    font-size: 8px;
    background: none;
    color: #181818;
    border: none;
    padding: 0;
    cursor: pointer;
    outline: inherit;
    font-family: "Lexend Zetta", sans-serif;
    letter-spacing: -1px;
    margin-bottom: 10px;

    @media screen and (min-width: 768px) {
      font-size: 12px;
    }
  }

  &__placeholder {
    @media screen and (min-width: 768px) {
      flex: 1;
    }
  }

  img {
    height: 40px;
    width: 40px;
    cursor: pointer;
    margin: 10px 8px;
    @media screen and (min-width: 768px) {
      margin: 20px 8px 10px;
    }
  }
}
</style>

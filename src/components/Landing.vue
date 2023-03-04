<script setup></script>

<template>
  <div class="kk-landing">
    <!-- <div class="landing__inner-wrapper">
      <h2 class="headline-m">KIM</h2>
      <h2 class="headline-m flipped">CHI</h2>
    </div> -->
    <div class="kk-desc">
      <!-- <h3>
        <p>organic & regional</p>
        <p>traditional & handmade</p>
        <p>probiotic & unpasteurized</p>
      </h3>

      <h4>we value tradition</h4> -->
      <h4>Our Product? Unpasteurized And Vivid Kimchi</h4>
      <h5>Our Motivation? Traditional And Handcrafted Healthy Food</h5>
      <h6>What We Actually do? ..</h6>
    </div>

    <div class="kk-process">
      <div class="kk-process-item">
        <img src="../assets/process_icons/ingredients.png" alt="ingredients" />
        <div>
          <p class="kk-process-item--headline">Ingredients</p>
          <p>
            For our Kimchi we use locally produced, organic ingredients,
            unprocessed sea-salt and intense korean gochugaru
          </p>
        </div>
      </div>
      <div class="kk-process-item">
        <img src="../assets/process_icons/processing.png" alt="processing" />
        <div>
          <p class="kk-process-item--headline">Processing</p>
          <p>
            For our Kimchi we use locally produced, organic ingredients,
            unprocessed sea-salt and intense korean gochugaru
          </p>
        </div>
      </div>
      <div class="kk-process-item">
        <img
          src="../assets/process_icons/fermentation-pot.png"
          alt="fermentation-pot"
        />
        <div>
          <p class="kk-process-item--headline">Fermentation</p>
          <p>
            For our Kimchi we use locally produced, organic ingredients,
            unprocessed sea-salt and intense korean gochugaru
          </p>
        </div>
      </div>
      <div class="kk-process-item">
        <img
          src="../assets/process_icons/lacto-bacteria.png"
          alt="lacto-bacteria"
        />
        <div>
          <p class="kk-process-item--headline">Lacto-Bacteria</p>
          <p>
            For our Kimchi we use locally produced, organic ingredients,
            unprocessed sea-salt and intense korean gochugaru
          </p>
        </div>
      </div>
      <div class="kk-process-item">
        <img src="../assets/process_icons/finished-product.png" alt="product" />
        <div>
          <p class="kk-process-item--headline">Product</p>
          <p>
            For our Kimchi we use locally produced, organic ingredients,
            unprocessed sea-salt and intense korean gochugaru
          </p>
        </div>
      </div>
    </div>

    <!--  <img class="stage-image__img" src="../assets/kimchi21.jpg" alt="kimchi" /> -->
  </div>
</template>

<style lang="scss">
.kk-landing {
  line-height: 1;
  width: 100%;
  display: flex;
  flex-direction: column;
  padding: 0 30px;

  @media screen and (min-width: 1024px) {
  }

  &__inner-wrapper {
    border-right: 5px white solid;
    border-left: 5px white solid;

    width: fit-content;
    padding: 50px;
  }

  .kk-desc {
    text-align: left;
    padding: 30px 0;

    @media screen and (min-width: 1024px) {
      padding: 50px 0;
    }

    h4,
    h5,
    h6 {
      font-size: 30px;
      margin: 30px 0;
    }

    p {
      margin: 4px 0;
    }
  }

  .kk-process {
    background-color: black;
    padding: 30px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 50px;

    @media screen and (min-width: 1024px) {
      padding: 60px;
    }

    p {
      color: white;
      font-size: 16px;
      margin-left: 20px;
      line-height: 1.5;

      @media screen and (min-width: 1024px) {
        font-size: 16px;
      }
    }

    &-item {
      display: flex;
      align-items: flex-start;
      width: 100%;

      @media screen and (min-width: 1024px) {
        width: 45%;
      }

      &--headline {
        font-size: 26px !important;
        font-weight: bold;

        @media screen and (min-width: 1024px) {
          font-size: 44px !important;
        }
      }
    }

    img {
      height: 64px;

      @media screen and (min-width: 1024px) {
        height: 90px;
      }
    }
  }
}
</style>

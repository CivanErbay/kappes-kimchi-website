<script setup></script>

<template>
  <div class="kk-products">
    <div class="kk-products--headline">
      <h3 class="headline-l">Produkte</h3>
      <p class="headline-s">
        Premium Kimchi aus Köln - traditionell nach koreanischer Rezeptur
      </p>
    </div>
    <div class="kk-products--content">
      <div class="kk-products--content--box">
        <img
          class="product-image"
          src="../assets/photos/kimchi_mild.jpg"
          alt="Kimchi Mild"
        />
        <h5 class="headline-m">Kimchi #1</h5>
        <p class="headline-s">mild</p>
      </div>
      <div class="kk-products--content--box">
        <img
          class="product-image"
          src="../assets/photos/kimchi_spicy.jpg"
          alt="Kimchi Mild"
        />
        <h5 class="headline-m">Kimchi #2</h5>
        <p class="headline-s">spicy</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.kk-products {
  &--headline {
    padding: 35px 20px;

    p {
      margin-left: 5px;
    }

    @media (min-width: 1024px) {
      padding: 80px 0 40px;
    }
  }

  &--content {
    display: flex;
    flex-direction: column;
    align-items: space-between;
    /*    background-color:  #181818; */
    border-radius: 5px;
    padding: 30px 0;

    @media (min-width: 768px) {
      flex-direction: row;
      justify-content: space-around;
    }

    &--box {
      flex-basis: 40%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      overflow: hidden;
      padding: 30px 30px 30px 30px;
      border-radius: 5px;

      @media (min-width: 768px) {
        border: 5px solid black;
        box-shadow: 30px 34px 0px 8px #000000;
      }

      .headline-m {
        letter-spacing: -4px;
        margin-top: 15px;
      }
      .product-image {
        height: 150px;
        transform: scale(1);
        transition: transform 0.5s ease-in-out;
        border: 3px solid black;
        border-radius: 5px;

        &:hover {
          transform: scale(1.1);
          transition: transform 0.5s ease-in-out;
        }

        @media (min-width: 768px) {
          height: 300px;
        }
      }
    }
  }
}
</style>

<template>
  <div class="product">
    <header-section />

    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="breadcrumb-text product-more text-left">
              <router-link to="/" ><i class="fa fa-home"></i> Home</router-link>
              <span>Detail</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img class="product-big-img" :src="default_image" alt="" />
                </div>
                <div class="product-thumbs">
                  <carousel
                    class="product-thumbs-track ps-slider"
                    :nav="false"
                    :dots="false"
                  >
                    <div v-for="item in thumbs" :key="item.id">
                      <div
                        class="pt"
                        @click="changeImage(item.image)"
                        :class="item.image == default_image ? 'active' : ''"
                      >
                        <img :src="item.image" alt="" />
                      </div>
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title">
                    <span>oranges</span>
                    <h3>Pure Pineapple</h3>
                  </div>
                  <div class="pd-desc">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit.
                      Corporis, error officia. Rem aperiam laborum voluptatum
                      vel, pariatur modi hic provident eum iure natus quos non a
                      sequi, id accusantium! Autem.
                    </p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                      Quam possimus quisquam animi, commodi, nihil voluptate
                      nostrum neque architecto illo officiis doloremque et
                      corrupti cupiditate voluptatibus error illum. Commodi
                      expedita animi nulla aspernatur. Id asperiores blanditiis,
                      omnis repudiandae iste inventore cum, quam sint molestiae
                      accusamus voluptates ex tempora illum sit perspiciatis.
                      Nostrum dolor tenetur amet, illo natus magni veniam quia
                      sit nihil dolores. Commodi ratione distinctio harum
                      voluptatum velit facilis voluptas animi non laudantium, id
                      dolorem atque perferendis enim ducimus? A exercitationem
                      recusandae aliquam quod. Itaque inventore obcaecati, unde
                      quam impedit praesentium veritatis quis beatae ea atque
                      perferendis voluptates velit architecto?
                    </p>
                    <h4>$495.00</h4>
                  </div>
                  <div class="quantity">
                    <router-link to="/cart" class="primary-btn pd-cart"
                      >Add To Cart</router-link
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->
    <related-product-section />

    <footer-section />
  </div>
</template>

<script>
import HeaderSection from "@/components/HeaderSection.vue";
import FooterSection from "../components/FooterSection.vue";
import carousel from "vue-owl-carousel";
import RelatedProductSection from "../components/RelatedProductSection.vue";

export default {
  name: "Product",
  components: {
    HeaderSection,
    FooterSection,
    carousel,
    RelatedProductSection,
  },
  data() {
    return {
      default_image: "img/mickey1.jpg",
      thumbs: [
        { id: 1, image: "img/mickey1.jpg" },
        { id: 2, image: "img/mickey2.jpg" },
        { id: 3, image: "img/mickey3.jpg" },
        { id: 4, image: "img/mickey4.jpg" },
      ],
    };
  },
  methods: {
    changeImage(imageUrl) {
      this.default_image = imageUrl;
    },
  },
};
</script>

<style scoped>
</style>
<template>
  <div class="card">
    <div class="card-content">
      <div class="content">
        <h4>{{ productItem.title }}</h4>
        <router-link to="/cart">
        <a
            class="button is-rounded is-pulled-left"
            @click="addCartItem(productItem)"
        >
          <strong>Add to Cart</strong>
        </a>
        </router-link>
        <br />
        <img :src="productItem.image" class="mt-4">


      </div>
      <div class="media">
        <div class="media-right">
          <a class="button is-primary is-light">
            <strong>{{ productItem.price }} TL</strong>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import {mapActions} from 'vuex'
export default {
  name: "ProductListItem",
  props: ["productItem"],
  methods: {
    ...mapActions(["addCartItem"]),
  },
};
</script>
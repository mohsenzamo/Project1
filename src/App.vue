<template>
  <div>
    <product
      v-for="(item, index) in productList"
      :key="item.id"
      :title="item.title"
      :image="item.image"
      :price="item.price"
    >
      <template v-slot:input>
        <myButton @deleteClicked="deleteFunction(index)">
          <template v-slot:button> Delete </template>
        </myButton>
      </template>
    </product>
  </div>
</template>

<script>
import product from "./components/product.vue";
import myButton from "./components/myButton.vue";
export default {
  name: "App",
  components: {
    product,
    myButton,
  },
  data() {
    return {
      productList: [
        {
          id: 0,
          title: "Product1",
          image: "https://picsum.photos/200",
          price: "200$",
        },
        {
          id: 1,
          title: "Product2",
          image: "https://picsum.photos/201",
          price: "300$",
        },
        {
          id: 2,
          title: "Product3",
          image: "https://picsum.photos/202",
          price: "400$",
        },
      ],
    };
  },
  methods: {
    deleteFunction(x) {
      this.productList.splice(x, 1);
    },
  },
};
</script>

<style>
div {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
</style>

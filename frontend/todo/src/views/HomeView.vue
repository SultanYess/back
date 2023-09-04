<template>
  <div class="home">
    <div class="row">
      <div class="col">
        <ItemList />
      </div>
      <div class="col-9">
        <ItemDetails />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import ItemList from "@/components/ItemList.vue";
import ItemDetails from "@/components/ItemDetails.vue";

export default {
  name: "HomeView",
  components: {
    ItemList,
    ItemDetails,
  },
};
</script>

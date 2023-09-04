<template>
  <div class="q-pa-md" style="max-width: 350px">
    <q-list>
      <span v-for="item in items" v-bind:key="item.id">
        <q-item>
          <q-item-section>
            <q-item-label>{{ item.creator }}</q-item-label>
            <q-item-label caption lines="2">
              {{ item.title }}
            </q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>
              {{ item.created_at }}
            </q-item-label>
          </q-item-section>
        </q-item>
        <q-separator spaced inset />
        <q-item>
          <q-item-section>
            <q-item-label>{{ item.creator }}</q-item-label>
            <q-item-label caption lines="2">
              {{ item.title }}
            </q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>
              {{ item.created_at }}
            </q-item-label>
          </q-item-section>
        </q-item>
      </span>
    </q-list>
  </div>
</template>

<style></style>

<script>
import axios from "axios";
export default {
  name: "ItemList",
  data() {
    return {
      items: [
        {
          id: 1,
          title: "tets",
          creator: "sultan",
          created_at: "2023-09-01T23:12:11",
        },
      ],
    };
  },

  created() {
    let self = this;
    axios.get("http://127.0.0.1:8000/main/items/").then((response) => {
      self.items = response.data;
      console.log(response);
    });
  },
};
</script>

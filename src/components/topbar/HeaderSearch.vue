<template>
  <div class="search-form">
    <div class="icon left">
      <IconSearch />
    </div>
    <div @click="value = ''" v-show="value" class="icon right">
      <IconX />
    </div>
    <input
      type="text"
      placeholder="What do you want to listen to"
      v-model="value"
    />
  </div>
</template>

<script>
import IconSearch from "../icons/IconSearch.vue";
import IconX from "../icons/IconX.vue";
export default {
  data() {
    return {
      value: "",
    };
  },
  components: { IconSearch, IconX },
};
</script>

<style scoped>
.search-form {
  width: 370px;
  height: 40px;
  align-items: center;
  position: relative;
}
input {
  border-radius: 500px;
  height: 40px;
  padding: 6px 48px;
  text-overflow: ellipsis;
  text-justify: auto;
  width: 100%;
  border: none;
  color: black;
}
input:focus {
  outline: none;
}
.icon {
  display: flex;
  position: absolute;
  align-items: center;
  height: 40px;
  color: black !important;
}
.left {
  left: 12px;
}
.right {
  right: 12px;
}
</style>

<template>
  <div class="col-lg-4 col-md-6">
    <div
      class="recent-track rounded"
      @mouseenter="hover = !hover"
      @mouseleave="hover = !hover"
    >
      <div class="custom">
        <img
          src="https://i.scdn.co/image/ab6761610000e5eb9896fc9a2e28384f2d705c45"
          alt="test image"
          draggable="false"
        />
        <span>Vũ</span>
      </div>
      <IconPlayGreen v-show="hover" />
    </div>
  </div>
</template>

<script>
import IconPlayGreen from "../icons/IconPlayGreen.vue";
export default {
  name: "TrackRecent",
  data() {
    return {
      hover: false,
    };
  },
  components: { IconPlayGreen },
};
</script>

<style scoped>
.recent-track {
  align-items: center;
  display: flex;
  justify-content: space-between;
  background-color: #2d3232;
  color: var(--hover-color);
  height: 80px;
  padding-right: 16px;
  overflow: hidden;
}
.recent-track:hover {
  background-color: #3a4444;
}

img {
  height: 80px;
  width: 80px;
}
.custom {
  display: flex;
  flex-direction: row;
  gap: 16px;
  align-items: center;
}
</style>

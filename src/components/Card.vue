<template>
  <div class="card" style="max-height: 250px; overflow: hidden;">
    <div class="card-header" :style="`background-image: url('${image}');`">
      <div class="card-title">{{title}}</div>
    </div>
    <div class="card-body">
      {{description}}
      <button
        v-if="button"
        class="el-button el-button-sm el-button--primary card-button"
        @click="button.click"
      >{{button.label}}</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: String,
    description: String,
    image: String,
    button: Object,
  },
};
</script>

<style scoped>
.card {
  background-color: var(--white);
  border-radius: 10px;
  border: var(--border-lg);
  color: var(--black);
  width: 90%;
  margin-left: 5%;
  max-height: none !important;
  padding-bottom: 20px;
}

.card-header {
  height: 100px;
  border-radius: 10px 10px 0 0;
  border-bottom: var(--border-lg);
  background-size: cover;
  background-position: bottom;
  background-repeat: no-repeat;
  position: relative;
}

.card-header .card-title {
  position: absolute;
  bottom: 10px;
  left: 10px;
  font-size: 23px;
  color: white;
  font-weight: bold;
}

.card-body {
  padding: 15px;
  padding-bottom: 0;
}

.card-button {
  margin-top: 10px;
}
</style>

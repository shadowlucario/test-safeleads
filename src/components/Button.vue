<template>
  <q-btn
  :text-color="textColor"
  :color="color"
  :no-caps="noCaps"
  :outline="outline"
  :class="['button1',
  dark ? 'background-second' : 'background-primary']"
  :label="title" />
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    outline: {
      type: Boolean,
    },
    noCaps: {
      type: Boolean,
    },
    dark: {
      type: Boolean,
    },
    color: {
      type: String,
    },
    textColor: {
      type: String,
    },
  },
};
</script>

<style lang="scss">
.button1 {
  width: 200px;
  height: 40px;
  padding: 28px;
  justify-content: center;
  box-sizing: border-box;
  border-radius: 8px;
}
.background-primary {
  background-color: #FA00EF;
}
.background-second {
  background-color: #3B004B;
}
</style>

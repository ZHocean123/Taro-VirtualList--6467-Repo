<template>
  <view :class="index % 2 ? 'ListItemOdd' : 'ListItemEven'" :style="css">
    Row {{ index }}
  </view>
</template>
<script>
export default {
  props: ["index", "data", "css"]
};
</script>
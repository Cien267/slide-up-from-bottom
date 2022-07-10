<template>
   <div class="box" v-if="isShowNormal">
        <div class="content">
          <p>1</p>
          <p>2</p>
          <p>3</p>
          <p>4</p>
          <p>5</p>
          <p>6</p>
          <p>7</p>
          <p>8</p>
          <p>9</p>
          <p>10</p>
          <p>11</p>
          <p>12</p>
          <p>13</p>
          <p>14</p>
          <p>15</p>
        </div>
        <div>
            <button @click="close">X</button>
        </div>
      </div>
</template>

<script>
export default {
  name: 'NormalModal',
  props: {
    isShowNormal: Boolean
  },
  methods: {
    close() {
      this.$emit('updateIsShowNormal', false)
    }
  },
}
</script>

<style scoped> 
.box {
    margin-top: 50px;
  width: 500px;
  height: 300px;
  position: relative;
  background-color: chartreuse;
}

.content {
  overflow: auto;
  width: 100%;
  height: 100%;
}

button {
  position: absolute;
  bottom: 0rem;
  right: 50%;
}
</style>

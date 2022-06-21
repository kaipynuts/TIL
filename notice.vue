<template>
  <div class="column items-center bg-white">
    <div class="header">소식</div>
    <div class="contents">
      <div class="column justify-center notice-item" v-for="n in 15" :key="n">
        <div v-if="n > 1" class="spacer"></div>
          <div class="title">
            [공지]
          </div>
          <div class="date">
            2022. 06. 15
          </div>
      </div>
    </div>
  </div>
</template>

<script>

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageNotice'
})

</script>
<style lang="scss" scoped>
@import "src/css/app.scss";
.header {
  @include font-one;
  font-size: 5.33vw;
  margin: 3.2vw 0 0 0;
}

.contents {
  width: 100vw;
  padding: 5.33vw 6.13vw 0;

}
.notice-item {
  height: 21.86vw;
  .spacer {
    border-bottom: 1px solid #D2D2D2;
  }
  .title {
    @include font-one;
    font-size: 4.26vw;
    margin: 5.33vw 0 0 0;
  }
  .date {
    @include font-one;
    width: 100%;
    font-size: 13px;
    color: #A7ACB7;
  }
}
</style>

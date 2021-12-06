<template>
  <div>
    <Test v-if="isShow" />
    <button type="button" @click="clickHandler">Click</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component({
  name: 'IndexPage',
  components: {
    Test: () => import('@/modules/test/components/Test.vue'),
  },
})
export default class Index extends Vue {
  isShow = false

  clickHandler(): void {
    this.isShow = !this.isShow
  }
}
</script>

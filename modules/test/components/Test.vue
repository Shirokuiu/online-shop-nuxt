<template>
  <div>
    <h1>{{ greet }}</h1>
    {{ fullName }}
  </div>
</template>

<script lang="ts">
import Component from 'vue-class-component'
import Vue from 'vue'

@Component({
  name: 'Test',
})
export default class Test extends Vue {
  greet = 'hello'
  firstName = 'John'
  lastName = 'Doe'

  get fullName(): string {
    return `${this.firstName} ${this.lastName}`
  }
}
</script>

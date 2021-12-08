<template>
  <div>
    <h1>{{ greet }}</h1>
    {{ fullName }}
    {{ testProp }}
  </div>
</template>

<script lang="ts">
import Component from 'vue-class-component'
import Vue from 'vue'
import { Prop } from 'vue-property-decorator'

@Component({
  name: 'Test',
})
export default class Test extends Vue {
  @Prop({ type: String, required: true }) readonly testProp!: string

  greet = 'hello'
  firstName = 'John'
  lastName = 'Doe'

  get fullName(): string {
    return `${this.firstName} ${this.lastName}`
  }
}
</script>

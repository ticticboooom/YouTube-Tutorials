<template>
  <div>
      <h4>{{title}}</h4>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component({})
export default class TodoListItem extends Vue {
    @Prop({required: true})
    private title!: string;
}
</script>

<style lang="scss" scoped>

</style>
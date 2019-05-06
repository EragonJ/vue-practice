<template>
  <div class="hello">
    test
  </div>
</template>

<script>
import OurButtonList from './OurButtonList.vue';

export default {
  name: 'HelloWorld',
  template: `
		<our-button-list v-bind:button-type="'a'">
			<template v-slot:submit>HIII</template>
			<template v-slot:cancel>Cancel</template>
		</our-button-list>
  `
}
</script>

<style scoped>
</style>

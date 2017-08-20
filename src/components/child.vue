<template>
  <div class="child">
  	<button @click="add">+</button>
  	{{num}}
  	<button @click="decrease">-</button>
  </div>
</template>

<script>
export default {
	props: {
		num: {
			type: Number,
			default: 0
		}
	},
	// data () {
	// 	return {
	// 		num: 10
	// 	};
	// },
	methods: {
		add () {
			// this.num++;
			this.$emit('forChildAdd');
		},
		decrease () {
			// this.num--;
			this.$emit('forCHildDecrease');
		}
	}
};
</script>

<style scoped lang="scss">
	.child{

	}
</style>

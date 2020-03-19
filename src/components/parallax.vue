<template lang="html">

	<section class="parallax">
		<div class="parallax" :style="imageStyle">.</div>
		<div class="content" :style="contentStyle">
			<slot></slot>
		</div>
	</section>

</template>

<script lang="js">

	export default {
		name: 'parallax',
		props: {
			image: {
				type: String
			}
		},
		mounted () {

		},
		data () {
			return {

			}
		},
		methods: {

		},
		computed: {
			imageStyle: function(){
				return {
					minHeight: "calc(100vh)",
					width: "100%",
					backgroundAttachment: "fixed",
					backgroundPosition: "center",
					backgroundRepeat: "no-repeat",
					backgroundSize: "cover",
					backgroundImage: "url(" + this.image + ")"
				};
			},
			contentStyle: function(){
				return {
					backgroundColor: "#fff",
					color: "#000",
					padding: "10px"
				};
			}
		}
}


</script>

<style scoped lang="scss">
	.parallax {

	}
</style>

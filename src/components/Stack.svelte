<script>
	export let space = "2";
</script>

<style lang="scss">
	@use "../scss/utils/all" as *;

	.un-stack {
		// Spacing
		@each $size, $space in $spacers {
			&.has-space-#{$size} {
				:global(> * + *) {
					margin-top: $space;
				}
			}
		}
	}
</style>

<div
	class="un-stack"
	class:has-space-1="{space === '1'}"
	class:has-space-2="{space === '2'}"
	class:has-space-3="{space === '3'}"
	class:has-space-4="{space === '4'}"
	class:has-space-5="{space === '5'}"
	class:has-space-6="{space === '6'}"
	class:has-space-7="{space === '7'}"
	class:has-space-8="{space === '8'}"
>
	<slot />
</div>

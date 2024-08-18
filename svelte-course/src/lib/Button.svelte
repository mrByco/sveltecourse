<script>
	export let size = 'small';
	export let shadow = false;
	export let bgColor = undefined;
	export let textColor = undefined;
</script>

<button
	style:--buttonBgColor={bgColor}
	style:--buttonTextColor={textColor}
	class:size-sm={size == 'small'}
	class:size-lg={size == 'large'}
	class:shadow><slot>Fallback content</slot></button
>

<style lang="scss">
	button {
		border: none;
		background-color: var(--buttonBgColor);
		color: var(--buttonTextColor);
		padding: 15px 20px;
		font-weight: bold;
		border-radius: 5px;
		cursor: pointer;

		&:hover {
			background-image: linear-gradient(rgba(0, 0, 0, 0.4) 0 0);
		}

		&:active {
			background-image: linear-gradient(rgba(255, 255, 255, 0.1) 0 0);
		}

		&.size-sm {
			padding: 15px 20px;
		}
		&.size-lg {
			padding: 25px 30px;
		}
		&.shadow {
			box-shadow: 0 0 10px rgba(1, 1, 1, 1);
		}
	}
</style>

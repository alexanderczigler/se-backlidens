<script lang="ts">
</script>

<block>
	<side>
		<slot />
	</side>
</block>

<style>
	@media (min-width: 800px) {
		block {
			display: flex;
			flex-direction: row;
			flex-wrap: nowrap;
			justify-content: left;
			align-items: center;
			align-content: stretch;
			max-width: 1000px;
			margin: 2em auto;
		}

		side {
			max-width: 80%;
		}

		side:last-child {
			display: unset;
		}
	}
</style>

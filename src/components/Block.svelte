<script lang="ts">
	export let alternate;
</script>

<block alternate={alternate || undefined}>
	<side>
		<slot />
	</side>
	<side>
		<i class="fa fa-paw" />
	</side>
</block>

<style>
	side:last-child {
		display: none;
	}

	@media (min-width: 800px) {
		block {
			display: flex;
			flex-direction: row;
			flex-wrap: nowrap;
			justify-content: center;
			align-items: center;
			align-content: stretch;
			max-width: 1000px;
			margin: 2em auto;
		}

		block[alternate] {
			flex-direction: row-reverse;
		}

		side:last-child {
			display: unset;
		}

		side {
			text-align: center;
			vertical-align: middle;
			width: 50%;
		}

		i {
			font-size: 6em;
			text-align: center;
		}
	}
</style>

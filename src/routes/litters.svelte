<script>
	import Block from "../components/Block.svelte";
	import Hero from "../components/Hero.svelte";
</script>

<svelte:head>
	<title>SE*Bäcklidens | Kattungar</title>
</svelte:head>

<Hero />

<Block>
	<h3>Kommande</h3>
	<p>
		Lorem, ipsum dolor sit amet consectetur adipisicing elit. Inventore totam
		assumenda magnam doloribus odio sint laudantium saepe consequatur corrupti
		quisquam itaque, voluptates tempora vel explicabo error dicta eius
		voluptatibus asperiores.
	</p>
</Block>

<Block alternate>
	<h3>Tidigare kullar</h3>
	<p>
		Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis impedit
		aut, blanditiis ratione eos accusamus ab enim laboriosam voluptates numquam
		ad quis quod fugiat amet saepe ipsam fugit doloribus dignissimos.
	</p>
	<p>
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Et at atque
		distinctio ab obcaecati, neque delectus repellat autem, temporibus ad sequi?
		Voluptatem enim nihil quaerat ullam debitis tempora quibusdam ipsa.
	</p>
	<p>
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore reiciendis
		consequuntur molestias aspernatur dolore pariatur repudiandae recusandae
		debitis vel perspiciatis illum sapiente ullam fugiat voluptatum, minima
		tenetur officiis iusto. Iusto.
	</p>
</Block>

<style>
	@media (min-width: 480px) {
	}
</style>

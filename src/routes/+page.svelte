<script>
	import { Heading, GradientButton } from 'flowbite-svelte'
	import { Avatar } from 'flowbite-svelte'
	import {
		ArrowUpRightFromSquareOutline,
		GithubSolid,
		LinkedinSolid,
		EnvelopeOpenSolid
	} from 'flowbite-svelte-icons'

	import 'devicon'
</script>

<div class="h-screen flex flex-col justify-center items-center text-center">
	<Heading tag="h1" class="mb-2" customSize="text-4xl font-extrabold md:text-5xl lg:text-6xl">
		Hi! I'm Gabriel
	</Heading>
	<Heading tag="h3" class="mb-4" customSize="text-2xl font-extrabold md:text-2xl lg:text-2xl">
		Software Engineer
	</Heading>
	<Avatar src="propic.jpeg" size="xl" border class="mb-4 ring-orange-600 dark:ring-orange-600" />

	<GradientButton href="/about" color="pinkToOrange" shadow={true}>
		Learn More
		<ArrowUpRightFromSquareOutline class="w-3.5 h-3.5 ml-2" />
	</GradientButton>
	<div class="flex flex-row justify-center space-x-3 mt-4">
		<a href="https://www.linkedin.com/in/gabriel-monti-floppy/">
			<LinkedinSolid class="dark:text-gray-300  dark:hover:text-orange-600 hover:text-orange-600" />
		</a>
		<a href="https://github.com/raspFloppy">
			<GithubSolid class="dark:text-gray-300 dark:hover:text-orange-600 hover:text-orange-600" />
		</a>
		<a href="mailto:gabriel.monti@tutamail.com">
			<EnvelopeOpenSolid
				class="dark:text-gray-300 dark:hover:text-orange-600 hover:text-orange-600"
			/>
		</a>
	</div>
</div>

<script>
	import { ChevronRightIcon } from '@rgossiaux/svelte-heroicons/outline';
	import { slide } from 'svelte/transition';
	export let href = '/';
	let isClicked = false;
	const handleClick = () => {
	  isClicked = true;
	};
  </script>
  
  <a on:click={handleClick} transition:slide {href} class="w-full p-2 flex justify-center items-center group">
	<ChevronRightIcon class="w-6 h-6 group {isClicked ? 'opacity-100' : 'opacity-0'} transition-opacity duration-300"/>
	<slot />
  </a>
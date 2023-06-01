<script>
	import BlogCard from '../../../lib/components/BlogCard.svelte';
	import { blogData } from '../../../lib/utils/blog-data';
</script>

<div>
	<BlogCard title={'title'} />
	<div class="flex flex-row max-w-3xl flex-wrap">
		{#each blogData as data}
			<BlogCard title={data.title} image={data.image} />
		{/each}
	</div>
</div>

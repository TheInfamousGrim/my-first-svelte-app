<script lang="ts">
	import { enhance } from '$app/forms';
	import type { PageData } from './$types';

	export let data: PageData;
</script>

<h1>{data.boatName}</h1>

<form method="POST" action="?/rename" use:enhance>
	<input type="text" name="boatName" id="boatName" />
	<button type="submit">Submit</button>

	<button formaction="?/capitalize">Capitalize</button>
</form>

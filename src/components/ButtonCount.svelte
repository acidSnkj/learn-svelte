<script>
	import { count } from "../store/store.js";
</script>

<button on:click={() => count.update(n => n+1)}>
	Click {$count === 0 ? "" : $count}
</button>
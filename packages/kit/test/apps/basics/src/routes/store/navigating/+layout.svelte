<script>
	import { navigating } from '$app/stores';
</script>

<nav>
	<a href="/store/navigating/a">a</a>
	<a href="/store/navigating/b">b</a>
	<a href="/store/navigating/c">c</a>
</nav>

<div id="nav-status">
	{#if $navigating}
		<p id="navigating">
			navigating from {$navigating.from.url.pathname} to {$navigating.to.url.pathname} ({$navigating.type})
		</p>
	{:else}
		<p id="not-navigating">not currently navigating</p>
	{/if}
</div>

<slot />

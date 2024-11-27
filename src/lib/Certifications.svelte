<script lang="ts">
	import CertificationElement from '$lib/CertificationElement.svelte';
</script>

<section id="certifications">
	<h1>Mes certifications</h1>
	<div>
		<CertificationElement name="CSM" />
	</div>
</section>

<style lang="scss">
  section {
    margin: auto;
    padding: 6rem var(--container-padding);
    max-width: var(--container-max-width);
    display: flex;
    align-items: center;
    flex-direction: column;
  }
</style>
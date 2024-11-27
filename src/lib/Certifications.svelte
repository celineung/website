<script lang="ts">
	import CertificationElement from '$lib/CertificationElement.svelte';
</script>

<section id="certifications">
	<h1>Mes certifications</h1>
	<div class="certifications__content">
		<CertificationElement name="CSM" />
	</div>
</section>

<style lang="scss">
  section {
    margin: auto;
    padding: 1rem var(--container-padding);
    max-width: var(--container-max-width);
    display: flex;
    align-items: center;
    flex-direction: column;

  }

	.certifications__content {
		margin: 1rem 0;
	}
</style>

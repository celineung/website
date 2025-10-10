<script lang="ts">
import A11YAudit from "$lib/assets/certifications/a11y-audit.svg";
import CsmImg from "$lib/assets/certifications/csm.webp";
import CertificationElement from "$lib/CertificationElement.svelte";

type Certification = {
	name: string;
	by: string;
	img: string;
	description: string;
};

const certificationData: Certification[] = [
	{
		name: "CSM",
		by: "Scrum Alliance",
		img: CsmImg,
		description:
			"J’accompagne les équipes dans l’adoption des méthodes agiles, en favorisant la collaboration, l’autonomie et l’amélioration continue.",
	},
];
</script>

<section id="certifications">
	<h1>Mes certifications</h1>
	<div class="certifications__content">
    {#each certificationData as certification}
      <CertificationElement name={certification.name} img={certification.img} description={certification.description} by={certification.by} />
    {/each}
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
    display: flex;
    justify-content: space-between;
	}
</style>

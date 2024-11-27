<script lang="ts">
	import CsmImg from "$lib/assets/certifications/csm.webp";

	export let name: ReferenceName;

	type ReferenceName = "CSM";

	const certificationData: Record<ReferenceName, { img: string, website: string, description: string }> = {
		CSM: {
			img: CsmImg,
			website: "https://www.scrumalliance.org/",
			description: "Le ScrumMaster agit en tant que leader au service de l’équipe (servant leader) en aidant l’équipe et l’organisation à faire le meilleur usage de Scrum."
		}
	}

</script>

<article>
	<img src={certificationData[name].img} alt={name}/>
	<p>{certificationData[name].description}</p>
</article>

<style lang="scss">
	article {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 300px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
		padding: 30px 20px;

		img {
			height: 100px;
			width: auto;
		}

		p {
			text-align: center;
		}
	}
</style>
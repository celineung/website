<script lang="ts">
	export let name: string;
	export let img: string;
	export let by: string;
	export let description: string;
</script>

<article>
  <img src={img} alt="Délivré par {by}"/>
  <h2>{name}</h2>
  <p>{description}</p>
</article>

<style lang="scss">
	article {
    background-color: #fff;
		display: flex;
    margin: 1rem;
		flex-direction: column;
		align-items: center;
		width: 300px;
    box-shadow: rgba(0, 0, 0, 0.2) 0px 4px 12px;
		padding: 30px 20px;
    width: 250px;

		img {
			height: 100px;
			width: auto;
		}

		h2, p {
      margin-bottom: 0;
			text-align: center;
		}
	}
</style>
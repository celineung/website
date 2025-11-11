<script>
  import Navigation from "$lib/Navigation.svelte";
  import './styles.css';
</script>


<Navigation />

<main>
  <slot />
</main>

<p class="accessibility-status">Accessibilité : étude en cours</p>

<style lang="scss">
  .accessibility-status {
    background-color: var(--primary-color);
    color: #fff;
    padding: 2rem 0;
    margin: 0;
    text-align: center;
  }
</style>

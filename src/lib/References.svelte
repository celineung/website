<script lang="ts">
  import ReferenceElement from "$lib/ReferenceElement.svelte";
</script>


<section id="work-references">
  <h1>Mes références</h1>
  <p>Lorsqu'ils sont publics, les liens d'accès aux sites et bases de code des projets auxquels j'ai participé s'affichent sous les logos des sociétés.</p>
  <div class="work-references__content">
    <ReferenceElement name="immersion-facilitee"/>
    <ReferenceElement name="invivo"/>
    <ReferenceElement name="pix"/>
    <ReferenceElement name="jcdecaux"/>
    <ReferenceElement name="bnpparibas"/>
    <ReferenceElement name="cision"/>
    <ReferenceElement name="zenika"/>
  </div>
</section>

<style lang="scss">
  section {
    margin: auto;
    padding: 3rem var(--container-padding) 0;
    max-width: var(--container-max-width);
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  p {
    text-align: center;
    line-height: 1.5rem;
    margin: 1rem 0 3rem 0;
  }

  .work-references__content {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
  }
</style>

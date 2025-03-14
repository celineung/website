<script lang="ts">
  import LinkedInIcon from "$lib/assets/social-media-icons/linkedin.svg"
  import GithubIcon from "$lib/assets/social-media-icons/github.svg"

  function smoothAnchorClick (event: MouseEvent & {currentTarget: (EventTarget & HTMLAnchorElement)}) {
    event.preventDefault();
    const anchor = document.getElementById("work-references");
    if (!anchor) return;
    window.scrollTo({
      top: anchor.offsetTop,
      behavior: 'smooth'
    })
  }
</script>

<section>
  <div class="container">
    <div>Bonjour, je suis</div>
    <h1>Céline Ung</h1>
    <h2>Développeuse web fullstack</h2>
    <p class="description">
      Depuis 2015, j’accompagne mes clients dans la réalisation de leurs projets web. J'ai récemment rejoint
      <a href="https://aycandoo.fr/" target="_blank" rel="noopener noreferrer" id="aycandoo">AYCANDO</a>.
    </p>
    <p class="description">
      Vous avez une idée ou un projet de site ou d'application web ? Je peux vous accompagner aussi bien dans sa réalisation que sa maintenance.<br><a href="mailto:celine.ung.pro@gmail.com" class="cu-contact">Prenons contact: celine.ung.pro@gmail.com.</a>
    </p>
    <p class="social-medias">
      <a href="https://www.linkedin.com/in/celine-ung" target="_blank" rel="noopener noreferrer" id="cu-linkedin"><img src={LinkedInIcon} alt="Profile LinkedIn de Céline"></a>
      <a href="https://github.com/celineung" target="_blank" rel="noopener noreferrer" id="cu-github"><img src={GithubIcon} alt="Profile Github de Céline"></a>
      <a href="https://aycandoo.fr/contact/" target="_blank" rel="noopener noreferrer" class="cu-contact">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="2 2 21 20" stroke-width="1.5" stroke="currentColor" class="w-6 h-6" role="img" aria-label="Prise de contact par mail">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 12 3.269 3.125A59.769 59.769 0 0 1 21.485 12 59.768 59.768 0 0 1 3.27 20.875L5.999 12Zm0 0h7.5" />
        </svg>
      </a>
    </p>
    <a class="navigate-down" href="#work-references" on:click={smoothAnchorClick}>
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6" role="img" aria-label="Aller à la section suivante">
        <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
      </svg>
    </a>
  </div>
</section>

<style lang="scss">
  %icon {
    margin: 0 4px;
    width: 1.3rem;
  }

  section {
    background-color: var(--primary-color);
    color: #fff;
		height: calc(100dvh - 50px);
		max-height: 750px;
		display: flex;
		margin-bottom: 3rem;
		padding-bottom: 50px;
    align-items: center;
    justify-content: center;
  }

  .container {
    padding: 0 var(--container-padding);
    max-width: var(--container-max-width);
    display: flex;
    align-items: center;
    flex-direction: column;

    h1 {
      margin: 3px 0;
      color: var(--secondary-color);
      font-size: 1.3rem;
    }

    h2 {
      margin: 20px 0;
      font-size: 2rem;
      text-align: center;

      @media (min-width: 768px) {
        margin-top: 32px;
      }
    }

    .description {
      text-align: center;
      line-height: 1.5rem;
			margin: 8px 0;

      @media (min-width: 768px) {
        margin: 16px 0;
      }
    }

    .social-medias {
      display: flex;
      padding-top: 16px;

      a {
        @extend %icon;
      }
    }
  }

  a {
    text-decoration: none;
    color: var(--secondary-color);

    &:hover {
      text-decoration: underline;
      filter: grayscale(0.7);
    }

    &.navigate-down {
      @extend %icon;
      margin-top: 2rem;
      width: 2.25rem;

      @media (min-width: 768px) {
        margin-top: 5rem;
      }
    }
  }
</style>

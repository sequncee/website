<!-- FadeInText.svelte -->
<!-- TODO: remove it to components -->
<script>
  export let text = "Enter your text here";
  const words = text.split(" ");
</script>

<h1 class="fade-in-text">
  {#each words as word, i}
    {#if i !== 0}&nbsp;{/if}
    <span class="fade-in-text-word" style="--fade-in-text-delay: {i * 0.1}s">{word}</span>
  {/each}
</h1>


<style>
  @import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");

  .fade-in-text {
    font-family: "Montserrat Medium";
    /* max-width: 40ch; */ 
    /* 通过控制maxwidth和位置来进行自定义 */
    text-align: center;
    transform: scale(0.94);
    animation: scale 3s forwards cubic-bezier(0.5, 1, 0.89, 1);
  }

  .fade-in-text-word {
    display: inline-block;
    opacity: 0;
    filter: blur(4px);
    animation: fade-in 0.8s forwards cubic-bezier(0.11, 0, 0.5, 0);
    animation-delay: var(--fade-in-text-delay);
  }

  @keyframes scale {
    100% {
      transform: scale(1);
    }
  }

  @keyframes fade-in {
    100% {
      opacity: 1;
      filter: blur(0);
    }
  }
</style>
<script lang="ts">
  export let title: string = "";
  export let imageSrc: string = "";
  export let alt: string = "";
</script>

<figure class="range-image">
  <figcaption>{title}</figcaption>
  <img src={imageSrc} {alt} />
</figure>

<style>
  .range-image {
    margin-top: 2em;
    padding-top: 1em;
    border-top: 1px solid #ccc;
  }

  .range-image figcaption {
    font-weight: 700;
    text-align: left;
    margin-bottom: 0.5em;
  }
</style>

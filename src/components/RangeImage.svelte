<script lang="ts">
  export let title: string = "";
  export let imageSrc: string = "";
  export let alt: string = "";
</script>

<figure>
  <figcaption>{title}</figcaption>
  <img src={imageSrc} {alt} />
</figure>

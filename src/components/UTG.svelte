<script lang="ts">
  import RangeImage from "./RangeImage.svelte";

  interface RangeImageInterface {
    title: string;
    imageSrc: string;
    alt: string;
  }

  let images: RangeImageInterface[] = [
    {
      title: "Open",
      imageSrc: "assets/images/open_UTG.png",
      alt: "Open UTG Image",
    },
  ];
</script>

<h3>Under the gun (UTG)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

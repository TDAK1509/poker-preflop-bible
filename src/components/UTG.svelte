<script lang="ts">
  import RangeImage from "./RangeImage.svelte";
  import type { RangeImageInterface } from "../types/RangeImage";

  let images: RangeImageInterface[] = [
    {
      title: "Open",
      imageSrc: "assets/images/open_UTG.png",
      alt: "Open UTG Image",
    },
    {
      title: "vs 3bet",
      imageSrc: "assets/images/vs3bet_UTG-IP-OOP.png",
      alt: "UTG vs 3bet Image",
    },
  ];
</script>

<h3>Under the gun (UTG)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

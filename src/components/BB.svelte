<script lang="ts">
  import RangeImage from "./RangeImage.svelte";
  import type { RangeImageInterface } from "../types/RangeImage";

  let images: RangeImageInterface[] = [
    {
      title: "BB v UTG-MP",
      imageSrc: "assets/images/BBvUTG.png",
      alt: "BBvUTG.png",
    },
    {
      title: "BB v CO",
      imageSrc: "assets/images/BBvCO.png",
      alt: "BBvCO.png",
    },
    {
      title: "BB v BTN",
      imageSrc: "assets/images/BBvBTN.png",
      alt: "BBvBTN.png",
    },
    {
      title: "BB v SB",
      imageSrc: "assets/images/BBvSB.png",
      alt: "BBvSB.png",
    },
    {
      title: "vs 4bet v UTG-MP",
      imageSrc: "assets/images/vs4bet_BBvUTG-MP.png",
      alt: "vs4bet_BBvUTG-MP.png",
    },
    {
      title: "vs 4bet v CO",
      imageSrc: "assets/images/vs4bet_BBvCO.png",
      alt: "vs4bet_BBvCO.png",
    },
    {
      title: "vs 4bet v BTN",
      imageSrc: "assets/images/vs4bet_BBvBTN.png",
      alt: "vs4bet_BBvBTN.png",
    },
    {
      title: "vs 4bet v SB",
      imageSrc: "assets/images/vs4bet_BBvSB.png",
      alt: "vs4bet_BBvSB.png",
    },
  ];
</script>

<h3>Small Blind (BTN)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

<script lang="ts">
  import RangeImage from "./RangeImage.svelte";
  import type { RangeImageInterface } from "../types/RangeImage";

  let images: RangeImageInterface[] = [
    {
      title: "Open",
      imageSrc: "assets/images/open_SB.png",
      alt: "open_SB.png",
      className: "open",
    },
    {
      title: "3bet v UTG & MP",
      imageSrc: "assets/images/3bet_SBvUTG-MP.png",
      alt: "3bet_SBvUTG.png",
      className: "three-bet",
    },
    {
      title: "3bet v CO",
      imageSrc: "assets/images/3bet_SBvCO.png",
      alt: "3bet_SBvCO.png",
    },
    {
      title: "3bet v BTN",
      imageSrc: "assets/images/3bet_SBvBTN.png",
      alt: "3bet_SBvBTN.png",
    },
    {
      title: "vs 3bet v BB",
      imageSrc: "assets/images/vs3bet_SBvBB.png",
      alt: "vs3bet_SBvBB.png",
      className: "vs3bet",
    },
    {
      title: "vs 4bet v UTG-MP",
      imageSrc: "assets/images/vs4bet_SBvUTG-MP.png",
      alt: "vs4bet_SBvUTG-MP.png",
      className: "vs4bet",
    },
    {
      title: "vs 4bet v CO",
      imageSrc: "assets/images/vs4bet_SBvCO.png",
      alt: "vs4bet_SBvCO.png",
    },
    {
      title: "vs 4bet v BTN",
      imageSrc: "assets/images/vs4bet_SBvBTN.png",
      alt: "vs4bet_SBvBTN.png",
    },
  ];
</script>

<h3>Small Blind (BTN)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

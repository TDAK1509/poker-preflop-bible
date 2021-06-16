<script lang="ts">
  import RangeImage from "./RangeImage.svelte";
  import type { RangeImageInterface } from "../types/RangeImage";

  let images: RangeImageInterface[] = [
    {
      title: "Open",
      imageSrc: "assets/images/open_BTN.png",
      alt: "open_BTN.png",
      className: "open",
    },
    {
      title: "3bet v UTG",
      imageSrc: "assets/images/3bet_BTNvUTG.png",
      alt: "3bet_BTNvUTG.png",
      className: "three-bet",
    },
    {
      title: "3bet v MP",
      imageSrc: "assets/images/3bet_BTNvMP.png",
      alt: "3bet_BTNvMP.png",
    },
    {
      title: "3bet v CO",
      imageSrc: "assets/images/3bet_BTNvCO.png",
      alt: "3bet_BTNvCO.png",
    },
    {
      title: "vs 3bet",
      imageSrc: "assets/images/vs3bet_BTN.png",
      alt: "vs3bet_BTN.png",
      className: "vs3bet",
    },
    {
      title: "vs 4bet v UTG",
      imageSrc: "assets/images/vs4bet_BTNvUTG.png",
      alt: "vs4bet_BTNvUTG.png",
      className: "vs4bet",
    },
    {
      title: "vs 4bet v MP",
      imageSrc: "assets/images/vs4bet_BTNvMP.png",
      alt: "vs4bet_BTNvMP.png",
    },
  ];
</script>

<h3>Button (BTN)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

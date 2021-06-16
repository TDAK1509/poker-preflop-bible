<script lang="ts">
  import RangeImage from "./RangeImage.svelte";
  import type { RangeImageInterface } from "../types/RangeImage";

  let images: RangeImageInterface[] = [
    {
      title: "Open",
      imageSrc: "assets/images/open_MP.png",
      alt: "open_MP.png",
      className: "open",
    },
    {
      title: "3bet",
      imageSrc: "assets/images/3bet_MPvUTG.png",
      alt: "3bet_MPvUTG.png",
      className: "three-bet",
    },
    {
      title: "vs 3bet IP",
      imageSrc: "assets/images/vs3bet_MP-IP.png",
      alt: "vs3bet_MP-IP.png",
      className: "vs3bet",
    },
    {
      title: "vs 3bet OOP",
      imageSrc: "assets/images/vs3bet_MP-OOP.png",
      alt: "vs3bet_MP-OOP.png",
    },
    {
      title: "vs 4bet",
      imageSrc: "assets/images/vs4bet_MPvUTG.png",
      alt: "vs4bet_MPvUTG.png",
      className: "vs4bet",
    },
  ];
</script>

<h3>Middle position (MP)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

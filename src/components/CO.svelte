<script lang="ts">
  import RangeImage from "./RangeImage.svelte";
  import type { RangeImageInterface } from "../types/RangeImage";

  let images: RangeImageInterface[] = [
    {
      title: "Open",
      imageSrc: "assets/images/open_CO.png",
      alt: "open_CO.png",
    },
    {
      title: "3bet CO v UTG",
      imageSrc: "assets/images/3bet_COvUTG.png",
      alt: "3bet_COvUTG.png",
    },
    {
      title: "3bet CO v MP",
      imageSrc: "assets/images/3bet_COvMP.png",
      alt: "3bet_COvMP.png",
    },
    {
      title: "vs 3bet IP",
      imageSrc: "assets/images/vs3bet_CO-IP.png",
      alt: "vs3bet_CO-IP.png",
    },
    {
      title: "vs 3bet OOP",
      imageSrc: "assets/images/vs3bet_CO-OOP.png",
      alt: "vs3bet_CO-OOP.png",
    },
    {
      title: "vs 4bet CO v UTG",
      imageSrc: "assets/images/vs4bet_COvUTG.png",
      alt: "vs4bet_COvUTG.png",
    },
    {
      title: "vs 4bet CO v MP",
      imageSrc: "assets/images/vs4bet_COvMP.png",
      alt: "vs4bet_COvMP.png",
    },
  ];
</script>

<h3>Cut off (CO)</h3>

{#each images as image}
  <RangeImage {...image} />
{/each}

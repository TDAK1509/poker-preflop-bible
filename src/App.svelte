<script lang="ts">
  import UTG from "./components/UTG.svelte";
  import MP from "./components/MP.svelte";
  import CO from "./components/CO.svelte";
  import SB from "./components/SB.svelte";
  import BB from "./components/BB.svelte";
  import BTN from "./components/BTN.svelte";

  enum Tab {
    UTG,
    MP,
    CO,
    BT,
    SB,
    BB,
  }

  const tabs = [
    {
      tab: Tab.UTG,
      label: "UTG",
    },
    {
      tab: Tab.MP,
      label: "MP",
    },
    {
      tab: Tab.CO,
      label: "CO",
    },
    {
      tab: Tab.BT,
      label: "BTN",
    },
    {
      tab: Tab.SB,
      label: "SB",
    },
    {
      tab: Tab.BB,
      label: "BB",
    },
  ];

  let activeTab: Tab = Tab.UTG;

  let getButtonClass: (tab: Tab) => string;
  $: getButtonClass = (tab: Tab) => {
    return activeTab === tab ? "active" : "";
  };

  function changeTab(tab: Tab) {
    activeTab = tab;
  }

  function goToOpenSection() {
    const section = document.querySelector(".open");

    if (section) {
      section.scrollIntoView(true);
    }
  }

  function goTo3betSection() {
    const section = document.querySelector(".three-bet");

    if (section) {
      section.scrollIntoView(true);
    }
  }

  function goToVs3betSection() {
    const section = document.querySelector(".vs3bet");

    if (section) {
      section.scrollIntoView(true);
    }
  }

  function goToVs4betSection() {
    const section = document.querySelector(".vs4bet");

    if (section) {
      section.scrollIntoView(true);
    }
  }
</script>

<main>
  <header class="header">
    <nav class="nav">
      <ul>
        {#each tabs as tab}
          <li>
            <button
              class={getButtonClass(tab.tab)}
              on:click={() => {
                changeTab(tab.tab);
              }}>{tab.label}</button
            >
          </li>
        {/each}
      </ul>
    </nav>

    <ul class="filter">
      <li><button on:click={goToOpenSection}>Open</button></li>
      <li><button on:click={goTo3betSection}>3bet</button></li>
      <li><button on:click={goToVs3betSection}>vs 3bet</button></li>
      <li><button on:click={goToVs4betSection}>vs 4bet</button></li>
    </ul>
  </header>

  {#if activeTab === Tab.UTG}
    <UTG />
  {:else if activeTab === Tab.MP}
    <MP />
  {:else if activeTab === Tab.CO}
    <CO />
  {:else if activeTab === Tab.BT}
    <BTN />
  {:else if activeTab === Tab.SB}
    <SB />
  {:else}
    <BB />
  {/if}
</main>

<style>
  main {
    text-align: center;
    width: 600px;
    margin: 0 auto;
  }
  .header {
    position: sticky;
    top: 0;
    background: #fff;
    padding: 2em 0;
  }
  .nav ul {
    display: flex;
  }
  .nav li {
    flex: 1;
  }
  .nav button {
    width: 100%;
    font-size: 1rem;
    padding: 0.5em 1em;
    background: none;
    border: none;
    border: 1px solid transparent;
    border-bottom: 1px solid #ccc;
  }
  .nav button:hover {
    opacity: 0.7;
  }
  .nav button.active {
    border: 1px solid #ccc;
    border-top-left-radius: 4px;
    border-top-right-radius: 4px;
    background: #333;
    color: #fff;
  }
  .filter {
    display: flex;
    justify-content: center;
    margin-top: 1em;
  }
  .filter button {
    font-size: 1rem;
    padding: 0.5em 1em;
    background: lightgrey;
    border: none;
  }
  .filter li ~ li {
    margin-left: 1em;
  }
</style>

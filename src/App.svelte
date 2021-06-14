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

  function changeTab(tab: Tab) {
    activeTab = tab;
  }
</script>

<main>
  <nav>
    <ul>
      {#each tabs as tab}
        <li>
          <button
            on:click={() => {
              changeTab(tab.tab);
            }}>{tab.label}</button
          >
        </li>
      {/each}
    </ul>
  </nav>

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

  nav {
    position: sticky;
    top: 0;
    background: #fff;
    padding: 2em 0;
  }

  ul {
    display: flex;
    justify-content: space-between;
  }

  ul button {
    font-size: 1rem;
    padding: 0.5em 1em;
    background: green;
    color: #fff;
    border: none;
    border-radius: 4px;
  }

  ul button:hover {
    opacity: 0.7;
  }
</style>

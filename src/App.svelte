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
</script>

<main>
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

<style lang="scss">
  main {
    text-align: center;
    width: 600px;
    margin: 0 auto;
  }

  .nav {
    position: sticky;
    top: 0;
    background: #fff;
    padding: 2em 0;

    ul {
      display: flex;
    }

    li {
      flex: 1;
    }

    button {
      width: 100%;
      font-size: 1rem;
      padding: 0.5em 1em;
      background: none;
      border: none;
      border: 1px solid transparent;
      border-bottom: 1px solid #ccc;

      &:hover {
        opacity: 0.7;
      }

      &.active {
        border: 1px solid #ccc;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        background: #333333;
        color: #fff;
      }
    }
  }
</style>

<script lang="ts">
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
  {#if activeTab === Tab.UTG}
    <p>UTG</p>
  {:else if activeTab === Tab.MP}
    <p>MP</p>
  {:else if activeTab === Tab.CO}
    <p>CO</p>
  {:else if activeTab === Tab.BT}
    <p>BTN</p>
  {:else if activeTab === Tab.SB}
    <p>SB</p>
  {:else}
    <p>BB</p>
  {/if}
</main>

<style>
</style>

<script lang="ts">
  enum Tab {
    UG,
    MP,
    CO,
    BT,
    SB,
    BB,
  }

  let activeTab: Tab = Tab.UG;

  function changeTab(tab: Tab) {
    activeTab = tab;
  }
</script>

<main>
  <ul>
    <li>
      <button
        on:click={() => {
          changeTab(Tab.UG);
        }}>UG</button
      >
    </li>
    <li>
      <button
        on:click={() => {
          changeTab(Tab.MP);
        }}>MP</button
      >
    </li>
    <li>
      <button
        on:click={() => {
          changeTab(Tab.CO);
        }}>CO</button
      >
    </li>
    <li>
      <button
        on:click={() => {
          changeTab(Tab.BT);
        }}>BT</button
      >
    </li>
    <li>
      <button
        on:click={() => {
          changeTab(Tab.SB);
        }}>SB</button
      >
    </li>
    <li>
      <button
        on:click={() => {
          changeTab(Tab.BB);
        }}>BB</button
      >
    </li>
  </ul>
  {#if activeTab === Tab.UG}
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

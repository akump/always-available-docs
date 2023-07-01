<script>
  import { Tabs, Tab, TabList, TabPanel } from "svelte-tabs";
  import Lifetime from "./Lifetime.svelte";
  import Help from "./Help.svelte";
</script>

<main>
  <h1 class="header">
    <a
      id="teams-link"
      href="https://chrome.google.com/webstore/detail/microsoft-teams-always-av/klbhkcdmilipmdaejfmhmphbdfiofoen"
      >MS Teams: Always Available Docs</a
    >
  </h1>
  <Tabs>
    <TabList>
      <Tab>Lifetime Subscription</Tab>
      <Tab>Wiki</Tab>
    </TabList>
    <TabPanel>
      <Lifetime />
    </TabPanel>
    <TabPanel>
      <Help />
    </TabPanel>
  </Tabs>
</main>

<style>
  main {
    padding-left: 8px;
    padding-bottom: 50px;
    background-color: 37383a;
  }

  .header {
    font-size: 4em;
    margin-bottom: 0;
  }
</style>

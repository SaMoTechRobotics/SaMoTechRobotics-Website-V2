<script>
  import LinkButton from "../components/Interactive/LinkButton.svelte";
  import Background from "../components/Sections/Background.svelte";
  import Hero from "../components/Sections/Hero.svelte";
  import SplitSection from "../components/Sections/SplitSection.svelte";
  import Stat from "../components/Sections/Stats/Stat.svelte";
  import StatsBar from "../components/Sections/Stats/StatsBar.svelte";
</script>

<Background />

<Hero img="images/photos/team/samotech-team1.jpg" />

<!-- <SectionBackground> -->
<StatsBar>
  <Stat
    title="Schools Represented"
    icon="material-symbols:school-outline"
    value="2"
  />
  <Stat title="Team Members" icon="pepicons-pencil:people" value="9" />
  <Stat title="Top Score" icon="lucide:medal" value="210" />
  <Stat title="Ranking" icon="lucide:medal" value="4" />
</StatsBar>

<SplitSection
  title="About Us"
  img="images/photos/team/samotech-team2.jpg"
  textSide="left"
>
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge.
  <div slot="buttons">
    <LinkButton to="/about">Learn More</LinkButton>
    <LinkButton to="/donate">Donate</LinkButton>
  </div>
</SplitSection>
<!-- </SectionBackground> -->

<SplitSection
  title="FIRST Tech Challenge"
  img="images/photos/samotech-winning1.webp"
  textSide="right"
>
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  SaMoTech robotics is a community based robotics team that participates in the
  FIRST Tech Challenge. SaMoTech robotics is a community based robotics team
  that participates in the FIRST Tech Challenge. SaMoTech robotics is a
  community based robotics team that participates in the FIRST Tech Challenge.
  <div slot="buttons">
    <LinkButton to="/about">Learn More</LinkButton>
  </div>
</SplitSection>

<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />

<style>
</style>

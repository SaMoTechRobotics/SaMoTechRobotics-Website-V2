<script>
  import Icon from "@iconify/svelte";
  import DonateCard from "../../components/Donate/DonateCard.svelte";
  import DonateOptions from "../../components/Donate/DonateOptions.svelte";
  import SponsorBenefits from "../../components/Donate/SponsorBenefits.svelte";
  import Background from "../../components/Sections/Background.svelte";
</script>

<Background />

<DonateOptions>
  <div slot="donate">
    <DonateCard
      title="GoFundMe"
      to="https://www.gofundme.com/f/teen-rookie-robotics-team"
      type="donate"
    >
      <Icon
        slot="icon"
        icon="simple-icons:gofundme"
        color="#02a95c"
        height="60"
      />
      Donate to our GoFundMe (GoFundMe takes a 2.9% cut of your donation).
    </DonateCard>

    <DonateCard
      title="PayPal"
      to="https://www.paypal.com/donate/?hosted_button_id=6M6HKRXT9468Y"
      type="donate"
    >
      <Icon slot="icon" icon="logos:paypal" height="60" />
      Donate directly to us through PayPal!
    </DonateCard>

    <DonateCard
      title="Other"
      to="mailto:samotechrobotics@gmail.com?subject=Donating to SaMoTech Robotics"
      type="donate"
    >
      <Icon slot="icon" icon="fontisto:email" height="60" color="black" />
      Contact us to donate with another method!
    </DonateCard>
  </div>

  <div slot="sponsor">
    <DonateCard title="1 - 100" type="sponsor" tier="1">
      <SponsorBenefits included="Website" />
    </DonateCard>

    <DonateCard title="100 - 1000" type="sponsor" tier="2">
      <SponsorBenefits included="Website,Robot" />
    </DonateCard>

    <DonateCard title="1000+" type="sponsor" tier="3">
      <SponsorBenefits included="Website,Robot,T-Shirt" />
    </DonateCard>
  </div>
</DonateOptions>

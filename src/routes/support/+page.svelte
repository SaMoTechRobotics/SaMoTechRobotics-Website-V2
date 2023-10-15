<script>
    import Icon from "@iconify/svelte";
    import DonateCard from "../../components/Donate/DonateCard.svelte";
    import DonateOptions from "../../components/Donate/DonateOptions.svelte";
    import SponsorBenefits from "../../components/Donate/SponsorBenefits.svelte";
    import Background from "../../components/Sections/Background.svelte";
    import SplitSection from "../../components/Sections/SplitSection.svelte";
    import SponsorsSection from "../../components/Sections/Sponsors/SponsorsSection.svelte";
    import DonateButton from "../../components/Donate/DonateButton.svelte";
</script>

<Background/>


<SplitSection
        title="Support Us"
        imgs="images/photos/samotech-building1.jpg"
        textSide="left"
        noBackground="true"
>
    <p>
        Our costs for the 23/24 regular season are estimated at $8,700, with an additional $6,400 required if (when) we
        make the World Championship in Texas. As all members of SaMoTech, including coaches and mentors, serve as unpaid
        volunteers, every donation will be used to cover practical expenses such as robot components, control systems,
        tools, registration fees, as well as marketing and travel/transport expenses. Any surplus funds will go to
        support SaMoTech’s future FIRST seasons or will be donated to other FTC teams in need.
        Donations to SaMoTech can be made through SaMoTech Booster Club, a 501c3 non-profit charity. Donations are
        typically 100% tax deductible in the US.
        Thank you for any consideration you may give to supporting our team.
    </p>
    <div slot="buttons">
        <DonateButton to="https://www.paypal.com/donate/?hosted_button_id=6M6HKRXT9468Y" title="Donate With PayPal">
            <Icon
                    slot="icon"
                    icon="logos:paypal"
                    color="#02a95c"
                    height="60"
            />
        </DonateButton>
    </div>
</SplitSection>


<SplitSection
        title="Sponsor Us"
        imgs="images/photos/samotech-building1.jpg"
        textSide="right"
        noBackground="true"
>
    <p>
        If you or your company has interest in sponsoring SaMoTech, please contact us at <a
            href="mailto:samotechrobotics@gmail.com"
            style="color: var(--dark);">SaMoTechRobotics@gmail.com</a>.
    </p>
    <h3>
        Benefits
    </h3>
    <p>
        We would be proud to include your company’s name and/or logo as our sponsor on all promotional materials
        including on our website, social media accounts, team banner and t-shirts worn at all competitions. The size and
        placement of the name/logo will be dependent on the number of sponsors we require and will reflect their
        relative contributions. We also welcome any discussion on how else we could show our thanks.
        If you would like more information, including a detailed budget, please contact us at any time. We welcome
        questions about our team, the competition, and about how your company might help these inspirational students.
    </p>
    <h3>
        Legacy
    </h3>
    <p>
        Your contributions will fund not just SaMoTech’s sophomore season but will also provide the foundation for our
        members to pursue their engineering dreams through all 4 years of high school. It is also our long-term hope to
        have such undeniable success in the FIRST competitions that it will compel our local public school system to
        establish robotics teams for credit as many private and some public schools across the country have already
        done.
    </p>
</SplitSection>

<SponsorsSection/>

<!--<DonateOptions>-->
<!--    <div slot="donate">-->
<!--        <DonateCard-->
<!--                title="GoFundMe"-->
<!--                to="https://www.gofundme.com/f/teen-rookie-robotics-team"-->
<!--                type="donate"-->
<!--        >-->
<!--            <Icon-->
<!--                    slot="icon"-->
<!--                    icon="simple-icons:gofundme"-->
<!--                    color="#02a95c"-->
<!--                    height="60"-->
<!--            />-->
<!--            Donate to our GoFundMe (GoFundMe takes a 2.9% cut of your donation).-->
<!--        </DonateCard>-->

<!--        <DonateCard-->
<!--                title="PayPal"-->
<!--                to="https://www.paypal.com/donate/?hosted_button_id=6M6HKRXT9468Y"-->
<!--                type="donate"-->
<!--        >-->
<!--            <Icon slot="icon" icon="logos:paypal" height="60"/>-->
<!--            Donate directly to us through PayPal!-->
<!--        </DonateCard>-->

<!--        <DonateCard-->
<!--                title="Other"-->
<!--                to="mailto:samotechrobotics@gmail.com?subject=Donating to SaMoTech Robotics"-->
<!--                type="donate"-->
<!--        >-->
<!--            <Icon slot="icon" icon="fontisto:email" height="60" color="black"/>-->
<!--            Contact us to donate with another method!-->
<!--        </DonateCard>-->
<!--    </div>-->

<!--    <div slot="sponsor">-->
<!--        <DonateCard title="1 - 100" type="sponsor" tier="1">-->
<!--            <SponsorBenefits included="Website"/>-->
<!--        </DonateCard>-->

<!--        <DonateCard title="100 - 1000" type="sponsor" tier="2">-->
<!--            <SponsorBenefits included="Website,Robot"/>-->
<!--        </DonateCard>-->

<!--        <DonateCard title="1000+" type="sponsor" tier="3">-->
<!--            <SponsorBenefits included="Website,Robot,T-Shirt"/>-->
<!--        </DonateCard>-->
<!--    </div>-->
<!--</DonateOptions>-->

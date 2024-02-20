<script>
    import Profile from "../../components/Sections/About/Profile.svelte";
    import TeamProfiles from "../../components/Sections/About/TeamProfiles.svelte";
    import Background from "../../components/Sections/Background.svelte";
    import SplitSection from "../../components/Sections/SplitSection.svelte";
</script>

<Background/>

<SplitSection
        title="Our Story"
        imgs="images/photos/samotech-garage.webp,images/photos/ilt2-winning-alliance.jpg"
        textSide="right"
        noBackground="true"
>
    <p>
        SaMoTech Robotics was founded by 6 freshmen in the fall of 2022 after they couldn't find support for a robotics
        team at their public high school. The team is now a 501c3 charity, entirely student-led with volunteer coaches
        and funded by donations, grants, and community sponsors.
    </p>

    <p>
        Despite their limited resources, SaMoTech enjoyed an extraordinary rookie year, ending the regular season as
        League W Champions and ranked #1 in all of SoCal (170 Teams). At the Regional Championship, the team battled to
        a semi-final tie-breaker, finally eliminated by the eventual World Champions.
    </p>

    <p>
        Now in their sophomore season (2023/24), SaMoTech has again achieved elite status as League W Champions,
        InterLeague Winning Alliance Captains, and ranked #1 in the entire state for their autonomous program (#11 in
        the world among 5000+ teams). Undefeated this season with 24 straight victories and several top-10 record
        scores, SaMoTech is now preparing for the Regional Championships on March 9 with the goal of earning a spot at
        the 2024 World Championship in Houston, Texas.
    </p>
</SplitSection>

<TeamProfiles>
    <Profile name="Alexa">
        Outside of robotics, I enjoy reading and writing. I contribute to the team
        by organizing our outreach and portfolio, and by strategizing. My favorite
        thing about FTC is supporting and coaching my teammates during the matches.
    </Profile>
    <Profile name="Ari">
        I enjoy video games, soccer, rock climbing, writing, and math. I contribute
        to the team by 3D printing the claw and beacon. In FTC, I like that you can
        iterate through meets, and see how robots improve through the challenge.
    </Profile>
    <Profile name="Brandon">
        Aside from robotics, I run and work on coding projects. I focus on coding
        teleop and autonomous, as well as building mechanical features on the robot. My
        favorite thing about FTC is being amazed by the many different approaches teams
        come up with for their robots.
    </Profile>
    <Profile name="Cameron">
        I really enjoy cycling, and getting fit for that. I've been helping by
        creating pods for our dead wheel odometry. I also helped CAD, and brainstorm
        for the claw. I like FTC because I learn a ton of new skills from it, and I
        love seeing the progression of our robot.
    </Profile>
    <Profile name="Camille">
        Outside of robotics, I enjoy rock climbing and music. My contribution to the
        team is mostly building and being a human player. My favorite thing about
        FTC is that it has helped me find an amazing community, and something that I
        enjoy.
    </Profile>
    <Profile name="Georgia">
        I enjoy playing soccer and doing art outside of robotics. My roles on the
        team are driving, building, and designing the t-shirt. My favorite thing
        about FTC is that it is a great community and everyone is so nice.
    </Profile>
    <Profile name="Jasmine">
        Outside of robotics, I play volleyball and make art. I help with driving,
        organizing the portfolio, and designing the t-shirt and logo. My favorite
        thing about FTC is the competitions and learning from other teams.
    </Profile>
    <Profile name="Waylon">
        I am Waylon. I will write my bio soon.
    </Profile>
</TeamProfiles>

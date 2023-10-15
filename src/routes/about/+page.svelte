<script>
    import Profile from "../../components/Sections/About/Profile.svelte";
    import TeamProfiles from "../../components/Sections/About/TeamProfiles.svelte";
    import Background from "../../components/Sections/Background.svelte";
    import SplitSection from "../../components/Sections/SplitSection.svelte";
</script>

<Background/>

<SplitSection
        title="Our Story"
        imgs="images/photos/e-hub-thanks.jpg,images/photos/rank-trophy.jpg"
        textSide="right"
        noBackground="true"
>
    <p>
        SaMoTech Robotics was founded by 6 freshmen in the fall of 2022 after they couldn't find support for a robotics
        team at their public high school. The team is entirely student-led with volunteer coaches and funded by
        donations, grants, and community sponsors.
    </p>
    <p>
        Despite their limited resources, SaMoTech recently completed an extraordinary rookie year. By the end of regular
        season the team had set 4 top-10 scores for the region and battled to #1 ranking in Los Angeles, as well as
        being listed among the top 50 teams worldwide (6000+). SaMoTech entered the postseason as League W Champions,
        then extended their winning streak to 23 consecutive matches to become their Inter-League Winning Alliance
        Captains. At the Regional Championship, the team battled to a semi-final tie-breaker, finally eliminated by the
        eventual World Champions.
    </p>
    <p>
        For their sophomore season (2023/24), SaMoTech students are committed to pushing themselves even further. They
        have already started developing more advanced engineering and coding techniques to build an even more complex
        robot, with the goal of earning a spot at the 2024 World Championship in Houston, Texas.
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
        Aside from robotics, I play tennis and do coding projects. I focus on coding
        teleop and autonomous, and building mechanical features on the robot. My
        favorite thing about FTC is being amazed by different approaches robots and
        teams have.
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
    <Profile name="Abigail">
        I'm the official cute distraction of the team. My job is to strut around the
        field during driving practice so no one can focus- they're too busy oohing
        and aahing over my cuteness. I love FTC because all these amazing humans
        come to pet me.
    </Profile>
</TeamProfiles>

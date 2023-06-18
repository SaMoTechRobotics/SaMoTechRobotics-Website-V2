<script lang="ts">
  import Profile from "./Profile.svelte";

  export let year: string;
</script>

{#if year == "2022-2023"}
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
  <Profile name="Griffin">
    My main hobbies outside of FTC are reading and playing video games. I help
    with building our robot and coaching. I like the opportunity for learning
    and thinking that FTC provides by making you find innovative solutions to
    any of the problems the challenge provides.
  </Profile>
  <Profile name="Jasmine">
    Outside of robotics, I play volleyball and make art. I help with driving,
    organizing the portfolio, and designing the t-shirt and logo. My favorite
    thing about FTC is the competitions and learning from other teams.
  </Profile>
  <Profile name="Tobin">
    My hobbies are running, touching grass, and coding. I contribute to the team
    by programming. My favorite thing about FTC is seeing the other teams'
    robots at meets and the similarities and differences between them and our
    robot.
  </Profile>
  <Profile name="Abigail">
    I'm the official cute distraction of the team. My job is to strut around the
    field during driving practice so no one can focus- they're too busy oohing
    and aahing over my cuteness. I love FTC because all these amazing humans
    come to pet me.
  </Profile>
{:else}
  Error, year not found
{/if}

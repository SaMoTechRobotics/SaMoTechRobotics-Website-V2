<script lang="ts">
    import PreviousTeamProfiles from "./PreviousTeamProfiles.svelte";

    const years = ["2023-2024", "2022-2023"] as const;
    let year: (typeof years)[number] = "2023-2024";
</script>

<div class="wrapper">
    <div class="top-content">
        <!-- <Select options={years.join(",")} bind:selectedOption={year} /> -->
        <select bind:value={year}>
            {#each years as y}
                <option value={y}>{y}</option>
            {/each}
        </select>
    </div>
    <div class="content">
        <h1>SaMoTech Team of {year}</h1>
        <img src={`images/photos/team/team${year}.jpg`} alt=""/>
        <div class="profiles">
            {#if year === "2023-2024"}
                <slot/>
            {:else if year === "2022-2023"}
                <PreviousTeamProfiles {year}/>
            {/if}
        </div>
    </div>
</div>

<style lang="scss">
  .wrapper {
    background-color: var(--bg);
    margin: 2rem 2rem;
    border-radius: 1rem;
    padding: 1rem;

    font-family: var(--font);
    color: var(--text);

    box-shadow: var(--box-shadow);

    @media (max-width: 700px) {
      margin: 2rem 1rem;
    }

    .top-content {
      padding: 1rem 1rem 0;
      display: flex;
      justify-content: flex-end;

      select {
        background-color: transparent;
        border: none;
        font-size: 1rem;
        cursor: pointer;

        font-family: var(--font);
        color: var(--text);

        transition: color 100ms ease-in-out;

        &:hover {
          color: var(--dark);
        }

      }

      @media (max-width: 1012px) {
        padding-bottom: 2rem;
      }
    }

    .content {
      display: flex;
      flex-direction: column;
      align-items: center;

      img {
        width: 50%;
        height: 100%;
        object-fit: cover;
        border-radius: 1rem;
        box-shadow: var(--img-shadow);
      }

      h1 {
        margin-top: 0;
        font-size: 2rem;
      }

      .profiles {
        padding-top: 2rem;
        display: grid;
        grid-template-columns: repeat(2, minmax(300px, 1fr));
        grid-gap: 1rem;

        @media (max-width: 1012px) {
          grid-template-columns: repeat(1, minmax(300px, 1fr));
        }
      }
    }
  }
</style>

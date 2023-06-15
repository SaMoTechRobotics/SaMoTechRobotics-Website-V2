<script lang="ts">
  import Icon from "@iconify/svelte";

  export let included: string;

  const benefits = ["Website", "Robot", "T-Shirt"];
</script>

{#each benefits as benefit}
  <div class="item">
    <Icon
      icon={included.includes(benefit) ? "ic:round-check" : "tabler:x"}
      color={included.includes(benefit) ? "#02a95c" : "#ff0000"}
      height="30"
    />
    <span>{benefit}</span>
  </div>
{/each}

<style lang="scss">
  .item {
    display: flex;
    align-items: center;
    justify-content: left;

    margin: 0.5rem 0;

    span {
      margin-left: 1rem;
    }
  }
</style>

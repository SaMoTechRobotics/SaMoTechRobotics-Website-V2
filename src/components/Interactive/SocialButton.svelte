<script lang="ts">
  import Icon from "@iconify/svelte";

  export let to: string;
  export let icon: string;
  export let size: string = "2";
</script>

<a href={to} target="_blank">
  <div>
    <Icon {icon} width={`${size}rem`} height={`${size}rem`} />
  </div>
</a>

<style lang="scss">
  a {
    display: flex;
    align-items: center;
    justify-content: center;

    color: var(--text-inv);
    transition: color 300ms ease-in-out;

    div {
      transition: transform 200ms ease-in-out;
    }

    &:hover {
      div {
        transform: translateY(-0.2rem);
      }
    }
  }
</style>

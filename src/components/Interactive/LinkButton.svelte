<script lang="ts">
  export let to: string;
</script>

<a href={to}>
  <button>
    <slot />
  </button>
</a>

<style lang="scss">
  a {
    button {
      margin: 0.5rem 0.5rem;
      padding: 0.5rem 1rem;
      border-radius: 0.5rem;

      left: 50%;

      background-color: transparent;
      border: 3px outset var(--primary);

      color: var(--text);
      font-size: 1rem;
      font-weight: 600;

      cursor: pointer;

      box-shadow: var(--box-shadow);

      transition: box-shadow 300ms ease-in-out,
        background-color 300ms ease-in-out;

      &:hover {
        background-color: var(--bg-hover);
        box-shadow: var(--box-shadow-hover);
      }
    }
  }
</style>

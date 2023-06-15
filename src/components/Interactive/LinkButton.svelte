<script lang="ts">
  export let to: string;
</script>

<a href={to}>
  <button>
    <slot />
  </button>
</a>

<style>
  button {
    margin: 0.5rem;
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
    border: none;
    background-color: rgba(0, 0, 0, 0.2);
    color: var(--text-inv);
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;

    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);

    transition: background-color 300ms ease-in-out;
  }

  button:hover {
    background-color: rgba(0, 0, 0, 0.3);
  }
</style>

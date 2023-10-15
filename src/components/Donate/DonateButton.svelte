<script lang="ts">
    export let title: string;
    export let to: string;
</script>

<a href={to} target="_blank">
    <div>
        <slot name="icon"/>
        <span>{title}</span>
    </div>
</a>

<style lang="scss">
  a {
    text-decoration: none;
  }

  div {
    background: var(--primary);
    border-radius: 5rem;
    border: none;
    padding: 0.5rem 2rem;
    cursor: pointer;

    display: flex;
    align-items: center;
    justify-content: center;

    transition: all 0.2s ease-in-out;

    span {
      margin-left: 10px;
      font-family: var(--font);
      font-size: 1.5rem;
      color: var(--text-inv);
    }

    &:hover {
      background: var(--secondary);

    }
  }
</style>
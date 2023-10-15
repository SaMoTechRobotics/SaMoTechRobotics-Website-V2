<div
        class="content"
>
    <slot/>
</div>

<style lang="scss">
  .content {
    background-color: var(--bg);
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    gap: 0px 0px;
    height: 100%;

    font-family: var(--font);
    color: var(--text);

    padding: 2rem 2rem;
  }
</style>

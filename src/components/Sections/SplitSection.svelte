<script lang="ts">
  export let title: string;
  export let img: string;
</script>

<div class="content">
  <div class="card">
    <h1>{title}</h1>
    <p>
      <slot />
    </p>
    <slot class="buttons" name="buttons" />
  </div>
  <img src={img} alt="" />
</div>
<div class="stats" />

<style>
  .content {
    display: grid;
    grid-template-columns: 1fr 1.5fr;
    grid-template-rows: 1fr;
    gap: 0px 0px;
    height: 100%;

    font-family: var(--font);

    padding: 4rem 2rem;
  }
  .stats {
    background-color: white;
    border-radius: 2rem;
    width: 80%;
    height: 6rem;
    margin-left: 10%;
    margin-top: -3rem;

    box-shadow: var(--box-shadow);

    transform: translateY(50%);

    transition: transform 300ms ease-in-out, box-shadow 300ms ease-in-out;
  }

  .stats:hover {
    box-shadow: var(--box-shadow-hover);
  }

  @media (max-width: 980px) {
    .content {
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;
    }
    .content > .card {
      order: 1;
    }
    .content > img {
      order: -1;
    }
  }

  @media (max-width: 550px) {
    .content {
      grid-template-rows: 1fr 0.4fr;
    }
  }

  .card {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    color: var(--text-inv);
    text-shadow: var(--text-shadow);
  }

  .card > .buttons {
    margin-top: 1rem;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  .card h1 {
    font-size: 2rem;
    text-align: center;
    margin-bottom: 0;
  }

  .card p {
    font-size: 1rem;
    text-align: center;
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 1rem;

    box-shadow: var(--box-shadow);
  }
</style>

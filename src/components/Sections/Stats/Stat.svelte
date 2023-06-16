<script lang="ts">
  import Icon from "@iconify/svelte";

  export let title: string;
  export let icon: string;
  export let value: string;

  /**
   * Animates the number from 0 to the target value when the element is in the viewport.
   * @param element The element to animate.
   */
  function animateOnScroll(element: HTMLElement) {
    // Create a new IntersectionObserver that will observe the given element
    const observer = new IntersectionObserver((entries) => {
      // For each entry that is intersecting with the viewport
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          observer.unobserve(element); // Stop observing the element
          const targetValue = parseInt(value);
          let currentValue = 0;
          // Set an interval to increment the current value and update the element's innerHTML
          const interval = setInterval(() => {
            if (currentValue < targetValue) {
              currentValue++; // Increment the current value since not reached the target value yet
              element.innerHTML = currentValue.toString();
            } else {
              clearInterval(interval);
            }
          }, 1000 / targetValue); // The interval time is determined by the target value
        }
      });
    });
    // Start observing the element
    observer.observe(element);
  }
</script>

<div class="wrapper">
  <div class="icon">
    <Icon {icon} height="50" />
  </div>
  <h1 class="value" use:animateOnScroll>
    {value}
  </h1>
  <hr />
  <p>{title}</p>
</div>

<style lang="scss">
  .wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;

    min-width: 10rem;

    font-family: var(--font);
    color: var(--text);

    .icon {
      margin-bottom: -0.5rem;
    }

    h1 {
      font-size: 1.5rem;
      margin: 0;

      @media (max-width: 980px) {
        font-size: 1.2rem;
      }
    }

    hr {
      width: 2rem;
      margin: 0;
      margin-bottom: 0.5rem;
      color: var(--primary);

      @media (max-width: 980px) {
        width: 1.5rem;
      }
    }

    p {
      font-size: 0.9rem;
      margin: 0;

      @media (max-width: 980px) {
        font-size: 0.8rem;
        word-break: break-word;
      }
    }
  }
</style>

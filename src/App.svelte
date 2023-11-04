<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";
  import { onMount } from "svelte";
  import "chartist";
    import { LineChart } from "chartist";

  let chart;

  const data = {
    labels: ["Mon", "Tue", "Wed", "Thu", "Fri"],
    series: [[5, 7, 3, 2, 8]],
  };

  onMount(() => {
    const options = {
      fullWidth: true,
      showArea: true,
    };

    const chart = new LineChart(
      ".ct-chart",
      {
        labels: ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
        series: [
          [12, 9, 7, 8, 5],
          [2, 1, 3.5, 7, 3],
          [1, 3, 4, 5, 6],
        ],
      },
      {
        fullWidth: true,
        chartPadding: {
          right: 40,
        },
      }
    );
  });
</script>

<main>
  <div>
    <!-- <a href="https://vitejs.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo} class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1> -->

    <!-- <div class="card">
    <Counter />
  </div> -->

    <div>
      <div class="ct-chart" />

      <p>
        Check out <a
          href="https://github.com/sveltejs/kit#readme"
          target="_blank"
          rel="noreferrer">SvelteKit</a
        >, the official Svelte app framework powered by Vite!
      </p>

      <p class="read-the-docs">
        Click on the Vite and Svelte logos to learn more
      </p>
    </div>
  </div>
</main>

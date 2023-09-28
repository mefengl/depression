<script>
  const saying = "WHAT A wanderful WORLD";

  $: hearing = "";
  $: dance = "";
  $: lucky = "";
  $: whoami = "";

  setInterval(() => {
    const words = saying.split(" ");
    const index = Math.floor(Math.random() * words.length);
    hearing = words[index];

    dance = Math.random() > 0.5 ? "italic" : "";
    lucky = Math.random() > 0.5 ? "font-mono" : "font-serif";
  }, 2000);
</script>

<div class="w-screen h-screen grid place-items-center impression">
  <h1 class="text-9xl text-white font-bold select-none {dance} {lucky}">
    {hearing}
  </h1>
</div>

<style>
  .impression {
    margin: 0;
    padding: 0;
    background: linear-gradient(45deg, red, blue);
    animation: gradient 6s infinite linear;
  }

  @keyframes gradient {
    0% {
      background: linear-gradient(45deg, red, blue);
    }
    25% {
      background: linear-gradient(45deg, yellow, green);
    }
    50% {
      background: linear-gradient(45deg, orange, purple);
    }
    75% {
      background: linear-gradient(45deg, pink, cyan);
    }
    100% {
      background: linear-gradient(45deg, red, blue);
    }
  }
</style>

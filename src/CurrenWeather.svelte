<script>
  export let data;
</script>

{#if data && data.current}
  <div class="flex flex-col items-center gap-2 my-6">
    <div class="flex items-center ml-5">
      <h1 class="text-4xl">{data.location.name}</h1>
      <img
        src={data.current.condition.icon}
        alt={data.current.condition.text}
        class=" -translate-y-5 -translate-x-1 scale-110"
      />
    </div>
    <span class="text-7xl">{data.current.temp_c} &degC</span>
    <span class="text-lg">{data.current.condition.text}</span>
    <span class="text-xl"
      >Humidity: {data.current.humidity} g/m<sup>-3</sup></span
    >
  </div>
{/if}

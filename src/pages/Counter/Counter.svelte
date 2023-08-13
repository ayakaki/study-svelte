<script>
  export let name = 'world';
  let count = 0;
  const increment = () => {
    count += 1;
  };

  // 初回のみ実行される
  console.log('Render');

  // $: で始まる式は、式の値が変更されたときに再評価される
  $: doubleCount = count * 2;
  $: console.log('count', count);
  $: console.log('doubleCount', doubleCount);
</script>

<h2>カウンターコンポーネント{name}</h2>
<div>
  <button on:click={increment}>
    {count} 回クリックしました
  </button>
</div>
<p>doubleCount:{doubleCount}</p>
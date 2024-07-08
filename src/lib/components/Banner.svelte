<script lang="ts">
  import { onMount } from 'svelte';

  let banner: HTMLElement;

  const atOptions = {
    key: '88df67b9e92c28f13aabbe0fffb42ae1',
    format: 'iframe',
    height: 50,
    width: 320,
    params: {},
  };

  onMount(() => {
    if (!banner.firstChild) {
      const conf = document.createElement('script');
      const script = document.createElement('script');
      script.type = 'text/javascript';
      script.src = `//www.highperformancedformats.com/${atOptions.key}/invoke.js`;
      conf.innerHTML = `atOptions = ${JSON.stringify(atOptions)}`;

      if (banner) {
        banner.append(conf);
        banner.append(script);
      }
    }
  });
</script>

<div bind:this={banner}></div>


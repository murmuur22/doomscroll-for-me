<script lang="ts">
  import { onMount } from 'svelte';

  let banner: HTMLElement;

  const options: any = {
    key: '0b7a5c3cd5154b72a1b3a0556ca4dfd2',
  };

  onMount(() => {
    if (!banner.firstChild) {
      const script = document.createElement('script');
      const div = document.createElement('div');
      script.type = 'text/javascript';
      script.src = `//pl23729903.highrevenuenetwork.com/${options.key}/invoke.js`;
      div.id = `container-${options.key}`;

      if (banner) {
        banner.append(div);
        banner.append(script);
      }
    }
  });
</script>

<div bind:this={banner}></div>


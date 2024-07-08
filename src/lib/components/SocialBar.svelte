<script lang="ts">
  import { onMount } from 'svelte';

  let socialBar: HTMLElement;

  const atOptions = {
    key: '88df67b9e92c28f13aabbe0fffb42ae1',
    format: 'iframe',
    height: 50,
    width: 320,
    params: {},
  };

  onMount(() => {
    if (!socialBar.firstChild) {
      const script = document.createElement('script');
      script.type = 'text/javascript';
      script.src = `//pl23729877.highrevenuenetwork.com/4a/25/cd/4a25cd923a029f1c8e2f74209981af49.js`;

      if (socialBar) {
        document.body.append(script);
      }
    }
  });
</script>

<div bind:this={socialBar}></div>


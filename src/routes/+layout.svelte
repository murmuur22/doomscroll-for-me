<script>
  import "../app.css";
  import { onMount } from "svelte";

  onMount(()=> {
    const script = document.createElement("script");
    script.src = "https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-2496238868363436"
    script.async = true;
    document.body.append(script);
  })
</script>

<slot />

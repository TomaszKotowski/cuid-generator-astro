<script>
  export let id = "";

  const handleCopyToClipboard = async () => {
    return await navigator.clipboard.writeText(id);
  };
</script>

<button type="button" on:click={handleCopyToClipboard} value={id}>Copy</button>

<script>
  export let id = "";
  let tooltipVisible = false;

  const handleTooltipVisibility = () => {
    tooltipVisible = true;
    setTimeout(() => (tooltipVisible = false), 2000);
  };

  const handleCopyToClipboard = async () => {
    handleTooltipVisibility();
    return await navigator.clipboard.writeText(id);
  };
</script>

<button
  data-tooltip={tooltipVisible ? "Copied!" : null}
  type="button"
  on:click={handleCopyToClipboard}
  value={id}>Copy</button
>

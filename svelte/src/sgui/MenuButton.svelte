<script>
    export let fn = undefined;
</script>

<button on:click={fn}>
    <slot></slot>
</button>

<script>

    import SGMenu from "./Menu.svelte";
    import Icon from '@iconify/svelte';

    export let title = undefined;
    export let header = false;

    let count = 0;

	function svelteGuiMinFrame(aba) {
		count += 1;
        console.log(count + " " + aba);
	}
</script>

<div class="sgui-window">

    {#if header == true}

    <div class="sgui-frame">
        <div class="sgui-frame-header">
            <div class="sgui-frame-header-wrapper">

            </div>
            <div class="sgui-frame-header-wrapper title">
                <h5>{title}</h5>
            </div>
            <div class="sgui-frame-header-wrapper buttons">
                <button class="frame-min-button" name="frame-min-button" on:click={() => svelteGuiMinFrame(23)}>{count}</button>
                <button class="frame-max-button" name="frame-max-button"><Icon icon="fluent:arrow-maximize-16-filled" /></button>
                <button class="frame-close-button" name="frame-close-button"><Icon icon="entypo:cross" /></button>
            </div>
        </div>
        <slot name="menu"/>
        <slot name="content"/>
    </div>

    {:else}

        <slot name="menu"/>
        <slot name="content"/>

    {/if}
</div>

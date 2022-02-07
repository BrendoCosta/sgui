<script>
    import * as SGUI from "./sgui";

    function hello(text) {

        alert("hello " + text);

    }

</script>

<main>
    <SGUI.Frame title="Example app" header={true}>
        <SGUI.Menu slot="menu">
            <SGUI.MenuButton fn="{() => hello('world')}">Button 1</SGUI.MenuButton>
            <SGUI.MenuButton>Button 2</SGUI.MenuButton>
            <SGUI.MenuButton>Button 3</SGUI.MenuButton>
        </SGUI.Menu>
        <p slot="content">Some text</p>
    </SGUI.Frame>
</main>

<style>
</style>

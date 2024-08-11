<script>
    import "../app.css";
    import { ModeWatcher } from "mode-watcher";
    import Nav from "$lib/components/Nav.svelte";
    import ThemeSwitch from "$lib/components/ThemeSwitch.svelte";
</script>
<Nav/>
<ModeWatcher />
<slot></slot>

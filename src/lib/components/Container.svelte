<script lang="ts">
    import {cn} from "$lib/utils"

    let className:string="";

    export {className as class};
</script>

<div class={cn("max-w-screen-sm px-4 mx-auto py-16", className)}>
    <slot/>
</div>
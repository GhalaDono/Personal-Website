<script lang="ts">
    import Container from "$lib/components/Container.svelte";
    import { Textarea } from "$lib/components/ui/textarea";
    import { Label } from "$lib/components/ui/label";
    import { Input } from "$lib/components/ui/input";
    import { text } from "@sveltejs/kit";
    import { Button } from "$lib/components/ui/button/index.js";

</script>

<Container class="flex flex-col gap-10" >
<form class="p-8 bg-[#a3bffa] shadow-md shadow-bg  flex flex-col gap-10">
    <div>
        <Label for="name">Full Name</Label>
        <Input name="name" id="name" placeholder="write your name"/>
    </div>
    <div>
        <Label for="email">Email</Label>
        <Input name="email" id="email" placeholder="example@example.com"/>
    </div>
    <div>
        <Label for="subject">Subject</Label>
        <Input name="subject" id="subject" placeholder="subject of your message"/>
    </div>
    <div >
        <Label for="message">Message</Label>
        <Textarea name="message" id="message" placeholder="write your message here"/>
    </div>
    <Button type="submit" class="bg-popover rounded-3xl h-12 w-20">
        Submit
    </Button>
</form>
</Container>

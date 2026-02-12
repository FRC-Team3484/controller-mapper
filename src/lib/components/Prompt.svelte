<script lang="ts">
    import {Node, Anchor, type Direction} from 'svelvet'
    import TextInput from '$lib/components/TextInput.svelte'
    import ControllerPrompt from '$lib/components/TextInput.svelte'
    let {target, x, y, d= 'east'}: {target: ControllerPrompt, x: number, y: number, d: Direction} = $props();
    let connection = 'controller-' + target
    console.log(connection)
</script>

<Node id="c-{target}"  let:selected position={{x:x, y:y}}>
    <TextInput tgt={target}></TextInput>
    <Anchor bgColor="brown" connections={[connection]} invisible direction={d} />
</Node>
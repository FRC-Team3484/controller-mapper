<script lang="ts">
    import {Node, Anchor, type Direction} from 'svelvet'
    import TextInput from '$lib/components/TextInput.svelte'
    import ControllerPrompt from '$lib/components/TextInput.svelte'
    
    let {target, x, y, d = 'east', anchorx = 0, anchory = 0}: {target: ControllerPrompt, x: number, y: number, d: Direction, anchorx: number, anchory: number} = $props();
    let connection = 'controller-' + target
    console.log(connection)
</script>

<Node id="c-{target}"  let:selected position={{x:x, y:y}} editable={false} bgColor="lightgray">
    <TextInput tgt={target}></TextInput>
    <Anchor bgColor="brown" connections={[connection]} invisible direction={d} dynamic={true}/>
</Node>
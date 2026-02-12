<script lang="ts">
    import xbox_controller from '$lib/assets/xbox_controller.svg'
    import Controller from '$lib/components/Controller.svelte';
    import Prompt from '$lib/components/Prompt.svelte';
    import TextInput from '$lib/components/TextInput.svelte';
    import { onMount } from 'svelte';
    
    let happy = $state("happy")
    import { Anchor, Background, Node, Svelvet } from 'svelvet';
    
    onMount(() => {
        window.addEventListener("resize", () => {
            setTimeout(() => {location.reload()}, 1000)
        })
    })
</script> 
<style>
    :root[svelvet-theme='blue-lines'] {
        --node-color: hsl(225, 30%, 50%);
		--node-border-color: hsl(225, 20%, 40%);
		--node-selection-color: hsl(45, 90%, 60%);
		--text-color: hsl(0, 100%, 50%);

		--background-color: hsl(225, 20%, 27%);
		--dot-color: hsl(225, 10%, 50%);

		--accent-color: hsl(45, 90%, 60%);
		--primary-color: hsl(225, 30%, 66%);

		--edge-color: #008000;
		--target-edge-color: hsl(225, 20%, 40%);

		--anchor-color: hsl(45, 90%, 67%);
		--anchor-border-color: hsl(45, 90%, 87%);
		--anchor-connected: hsl(45, 90%, 100%);
		--anchor-connected-border: hsl(225, 20%, 20%);

		--anchor-connecting: hsl(225, 30%, 40%);
		--anchor-connecting-border: hsl(0, 0%, 100%);

		--anchor-hovering: hsl(225, 20%, 46%);
		--anchor-hovering-border: hsl(0, 0%, 0%);

		--minimap-background-color: hsl(225, 20%, 27%);

		--minimap-node-color: hsl(225, 30%, 20%);

		--controls-background-color: hsl(225, 20%, 27%);
		--controls-text-color: hsl(0, 0%, 100%);

		--theme-toggle-text-color: hsl(0, 0%, 100%);
		--theme-toggle-color: hsl(225, 20%, 27%);
    }
</style>

<!-- <div class="w-screen h-screen flex">
    <div class="flex flex-row">
        <div class="flex flex-col w-[33vw] justify-center">
            
        </div>
        <div class="flex flex-col w-[33vw] justify-center">
            <img id="xboxc" alt="xbox controller" src={xbox_controller} class="w-75 lg:w-200">
        </div>
        <div class="flex flex-col w-[33vw] justify-center">
        </div>
    </div>
</div> -->
<div class="w-screen h-screen flex">
    <Svelvet id="my-canvas" edgeStyle="step" theme="blue-lines" fitView>
        <!-- <Node id="frog" let:selected position={{x: 200, y:0}}>
            <p>frog</p>
            <Anchor invisible direction="west"/>
        </Node> -->
        
        <img alt="not a frog" src="{xbox_controller}" class="w-50">
        <Controller></Controller>

        <Prompt target="lb" x={-50} y={-90}></Prompt>
        <Prompt target="rb" x={150} y={-90}></Prompt>
        <Background bgColor="black" dotColor="black" slot="background"/>
    </Svelvet>


</div>    

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
        --node-color: hsl(0, 0%, 0%);
		--node-border-color: hsl(0, 0%, 0%);
		--node-selection-color: hsl(0, 0%, 0%);
		--text-color: hsl(0, 0%, 0%);

		--background-color: #ffffff;
		--dot-color: hsl(225, 10%, 50%);

		--accent-color: hsl(45, 90%, 60%);
		--primary-color: hsl(225, 30%, 66%);

		--edge-color: #000000;
		--target-edge-color: hsl(0, 0%, 0%);

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
        
        <img alt="not a frog (an xbox controller)" src="{xbox_controller}" class="w-50">
        <Controller></Controller>

        <Prompt target="lb" x={-50} y={-90} d="east"/>
        <Prompt target="rb" x={190} y={-90} d="west"/>
        <Prompt target="lt" x={-30} y={-150} d="east"/>
        <Prompt target="rt" x={160} y={-150} d="west"/>
        <Prompt target="view" x={60} y={-120} d="south"/>
        <Prompt target="menu" x={75} y={-70} d="south"/>
        <Prompt target="lstick" x={-100} y={-15} d="east"/>
        <Prompt target="dpadu" x={-120} y={48} d="east"/>
        <Prompt target="dpadd" x={20} y={160} d="north"/>
        <Prompt target="dpadl" x={-100} y={110} d="east"/>
        <Prompt target="dpadr" x={130} y={140} d="east"/>
        <Prompt target="rstick" x={230} y={110} d="east"/>
        <Prompt target="buttonx" x={240} y={-21} d="east"/>
        <Prompt target="buttony" x={322} y={-61} d="east"/>
        <Prompt target="buttona" x={302} y={30} d="east"/>
        <Prompt target="buttonb" x={402} y={5} d="east"/>
        

        <Background bgColor="white" dotColor="white" slot="background"/>
    </Svelvet>


</div>    

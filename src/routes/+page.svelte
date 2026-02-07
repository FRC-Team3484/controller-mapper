<script lang="ts">
    import xbox_controller from '$lib/assets/xbox_controller.svg'
    import TextInput from '$lib/components/TextInput.svelte';
    
    let happy = $state("happy")
    import { onMount } from 'svelte';
    onMount(createLine)

    function createLine() {
        
    }
</script> 


<div class="w-screen h-screen flex">
    <div class="flex flex-row">
        <div class="flex flex-col w-[33vw] justify-center">
            
        </div>
        <div class="flex flex-col w-[33vw] justify-center">
            <img id="xboxc" alt="xbox controller" src={xbox_controller} class="w-75 lg:w-200">
        </div>
        <div class="flex flex-col w-[33vw] justify-center">
            <TextInput tgt="rb"></TextInput>
            <TextInput tgt="rt"></TextInput>
            <TextInput tgt="buttona"></TextInput>
            <TextInput tgt="buttonb"></TextInput>
            <TextInput tgt="buttonx"></TextInput>
            <TextInput tgt="buttony"></TextInput>
            <TextInput tgt="menu"></TextInput>
            <TextInput tgt="rstick"></TextInput>
        </div>
    </div>
</div>

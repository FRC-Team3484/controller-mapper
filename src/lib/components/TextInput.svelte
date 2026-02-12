<script lang="ts">
    type ControllerPrompt = 
    "buttona" | "buttonb" | "buttonx" | "buttony"
    | "dpadd" | "dpadu" | "dpadl" | "dpadr"
    | "lstick" | "rstick"
    | "lb" | "lt" | "rb" | "rt"
    | "menu" | "share" | "view"
    

    let {tgt}: {tgt: ControllerPrompt} = $props();
    
</script>

<div class="">
    <enhanced:img class="w-5 h-5" alt="{tgt} image" about="{tgt} image" src={`/src/lib/assets/controllers/xbox/${tgt}.png`}/>
    <input class="ui_input">
</div>

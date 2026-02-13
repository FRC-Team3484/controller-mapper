<script lang="ts">
import {Anchor, Node} from 'svelvet'
import xbox_controller from '$lib/assets/xbox_controller.svg'

</script>

<Node id="controller-lb" let:selected position={{x:50, y:5}}>
    <Anchor invisible direction="north"></Anchor>
</Node>
<Node id="controller-rb" let:selected position={{x:150, y:5}}>
    <Anchor invisible direction="north"></Anchor>
</Node>

<Node id="controller-lt" let:selected position={{x:50, y:5}}>
    <Anchor invisible direction="north"></Anchor>
</Node>

<Node id="controller-rt" let:selected position={{x:150, y:5}}>
    <Anchor invisible direction="north"></Anchor>
</Node>

<Node id="controller-view" let:selected position={{x:86, y:38}}>
    <Anchor invisible direction="north"></Anchor>
</Node>

<Node id="controller-menu" let:selected position={{x:115, y:38}}>
    <Anchor invisible direction="north"></Anchor>
</Node>

<Node id="controller-lstick" let:selected position={{x:51.5, y:36}}>
    <Anchor invisible direction="west"></Anchor>
</Node>

<Node id="controller-dpadu" let:selected position={{x:71, y:64}}>
    <Anchor invisible direction="west"></Anchor>
</Node>

<Node id="controller-dpadd" let:selected position={{x:71, y:84}}>
    <Anchor invisible direction="south"></Anchor>
</Node>

<Node id="controller-dpadl" let:selected position={{x:61, y:74}}>
    <Anchor invisible direction="west"></Anchor>
</Node>

<Node id="controller-dpadr" let:selected position={{x:81, y:74}}>
    <Anchor invisible direction="south"></Anchor>
</Node>

<Node id="controller-rstick" let:selected position={{x:127.5, y:70}}>
    <Anchor invisible direction="east"></Anchor>
</Node>

<Node id="controller-buttonx" let:selected position={{x:137, y:41}}>
    <Anchor invisible direction="north"></Anchor>
</Node>
<Node id="controller-buttony" let:selected position={{x:151, y:28}}>
    <Anchor invisible direction="east"></Anchor>
</Node>
<Node id="controller-buttona" let:selected position={{x:151, y:55}}>
    <Anchor invisible direction="south"></Anchor>
</Node>
<Node id="controller-buttonb" let:selected position={{x:165, y:41}}>
    <Anchor invisible direction="east"></Anchor>
</Node>
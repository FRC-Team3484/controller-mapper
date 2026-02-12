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
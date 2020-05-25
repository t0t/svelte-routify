<script>
    export let type, id;
    import { params } from "@sveltech/routify";
    $: type = $params.type;
</script>

<h1>Seguro que quieres borrar {id} de {type}??</h1>
<button>Yes</button>
<button>No</button>
<script lang="ts">
    export let message: string;
    export let classes = '';
</script>

<div class:hidden={!message}>
    <p class="text-sm text-red-600 {classes}">
        {message}
    </p>
</div>

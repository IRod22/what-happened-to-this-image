<script lang="ts">
    let before = ''
    let after = ''
</script>

<h1>What Happened to This Image?</h1>

<table>
    <tr>
        <th>Before</th>
        <th></th>
        <th>After</th>
    </tr>
    <tr>
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <td><img src="{before}" alt="Original image"></td>
        <td>&rarr;</td>
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <td><img src="{after}" alt="Changed image"></td>
    </tr>
    <tr>
        <td><label>URL: <input type="text" bind:value={before}></label></td>
        <td></td>
        <td><label>URL: <input type="text" bind:value={after}></label></td>
    </tr>
</table>
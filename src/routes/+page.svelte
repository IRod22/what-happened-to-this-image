<script lang="ts">
    let before = ''
    let after = ''
    let blur = 0
    let brightness = 100
    let contrast = 100
    let grayscale = 0
    let hueRotate = 0
    let inversion = 0
    let sepia = 0
    $: css = `filter: blur(${blur? `${blur}px` : "0"}) brightness(${brightness}%) contrast(${contrast}%) grayscale(${grayscale}%) hue-rotate(${hueRotate}deg) invert(${inversion}%) sepia(${sepia}%) `
</script>

<table>
    <tr>
        <th>Original Image</th>
        <th></th>
        <th>Processed Image</th>
    </tr>
    <tr>
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <td><img style={css} src="{before}" alt="Original image"></td>
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

<fieldset>
    <legend>Image filters</legend>
    <p>
        <label>Blur: <input type="number" bind:value={blur} min="0" step="1">{blur? "px" : " (no change)"}</label>
    </p>
    <p>
        <label>Brightness: <input type="number" bind:value={brightness} min="0" step="1">% {brightness > 100? "(brighter)" : brightness < 100? "(darker)" : "(no change)"}</label>
    </p>
    <p>
        <label>Contrast: <input type="number" bind:value={contrast} min="0" step="1">% {contrast > 100? "(more contrast)" : contrast < 100? "(less contrast)" : "(no change)"}</label>
    </p>
    <p>
        <label>Grayscale: <input type="number" bind:value={grayscale} min="0" max="100" step="1">% {grayscale? '' : " (no change)"}</label>
    </p>
    <p>
        <label>Hue rotation: <input type="number" bind:value={hueRotate} min="0" max="359" step="1"> degrees {hueRotate? '' : " (no change)"}</label>
    </p>
    <p>
        <label>Inversion: <input type="number" bind:value={inversion} min="0" max="100" step="1">% {inversion? '' : " (no change)"}</label>
    </p>
    <p>
        <label>Sepia: <input type="number" bind:value={sepia} min="0" max="100" step="1">% {sepia? '' : " (no change)"}</label>
    </p>
</fieldset>
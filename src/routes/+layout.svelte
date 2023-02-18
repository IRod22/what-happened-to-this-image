<script lang="ts">
    import { base } from '$app/paths'
</script>

<h1>What Happened to This Image?</h1>

<nav>
    <a href={`${base}/`}>Home</a>
    <a href={`${base}/about`}>About</a>
</nav>

<slot></slot>

<section>
    <h3>How do I use this?</h3>
    <ol>
        <li>
            Paste the URL of the original image into the "URL" field under the "Original Image" area.
            You should see the image within a few seconds at most.
        </li>
        <li>
            Paste the URL of the original image into the "URL" field under the "Processed Image" area.
            You should see the image within a few seconds at most.
        </li>
        <li>
            Configure the image filters until the original image becomes the processed image.
            You should be able to use your arrow keys to get fine-grained results.
        </li>
        <li>
            See the immediate and fine-grained results.
            Adjust the filters until the original image looks identical to the processed image.
        </li>
    </ol>
</section>

<script>
    export let r;
    export let g;
    export let b;

    function valueToHex(c) {
        let hex = c.toString(16);
        return hex;
    }

    function rgbToHex(r, g, b) {
        return valueToHex(r) + valueToHex(g) + valueToHex(b);
    }
</script>

<h1>{rgbToHex(r, g, b)}</h1>

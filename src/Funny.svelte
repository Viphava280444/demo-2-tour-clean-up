<script>
    export let size = 100;
    setInterval(() => {
        if (size === 50) {
            size = 5;
        } else {
            size += 1;
        }
    }, 10);
</script>

<h2 style="font-size: {size}px;">No soap radio</h2>

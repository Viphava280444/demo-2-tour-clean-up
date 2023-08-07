<script>
    let redScore = 0;
    let blueScore = 0;

    function increaseRed() {
        if (redScore < 20) {
            redScore += 1;
        }
    }
    function decreaseRed() {
        if (redScore > 0) {
            redScore -= 1;
        }
    }
    function increaseBlue() {
        if (blueScore < 20) {
            blueScore += 1;
        }
    }
    function decreaseBlue() {
        if (blueScore > 0) {
            blueScore -= 1;
        }
    }
    function reset() {
        redScore = 0;
        blueScore = 0;
    }
</script>

<div class="container text-center">
    <div class="row">
        <div class="col c1">
            <h4>Team Red: {redScore}</h4>

            <div
                class="btn-group"
                role="group"
                aria-label="Basic mixed styles example"
                style="margin-bottom: 15px;"
            >
                <button
                    type="button"
                    class="btn btn-success"
                    on:click={increaseRed}><b>+</b></button
                >
                <button
                    type="button"
                    class="btn btn-danger"
                    on:click={decreaseRed}><b>-</b></button
                >
            </div>
        </div>
        <div class="col c2">
            <h4>Team Blue: {blueScore}</h4>

            <div
                class="btn-group"
                role="group"
                aria-label="Basic mixed styles example"
            >
                <button
                    type="button"
                    class="btn btn-success"
                    on:click={increaseBlue}><b>+</b></button
                >
                <button
                    type="button"
                    class="btn btn-danger"
                    on:click={decreaseBlue}><b>-</b></button
                >
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col">
            {#if redScore === 20}
                <h4 style="color: white; background-color: red">Red won!</h4>
            {:else if blueScore === 20}
                <h4 style="color: white; background-color: blue">Blue won!</h4>
            {/if}
        </div>
    </div>
    <div class="row">
        <div class="col">
            <div class="d-grid gap-2">
                <button class="btn btn-warning" type="button" on:click={reset}
                    ><b>Reset</b></button
                >
            </div>
        </div>
    </div>
</div>

<style>
    .container .row .c1 {
        border: solid red;
        color: red;
    }
    .container .row .c2 {
        border: solid blue;
        color: blue;
    }
</style>

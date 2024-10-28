<script>
    import {navigate} from "svelte-navigator";
</script>

<div class="hero bg-white min-h-screen">
    <div class="hero-content text-center">
        <div class="max-w-md">
            <h1 class="text-5xl font-bold text-black">Hello Nicholas</h1>


            <div class="stats bg-white">
                <div class="stat">
                    <div class="stat-figure text-secondary">
                        <div
                                class="radial-progress bg-primary text-primary-content border-primary border-4 text-xs"
                                style="--value:80; --thickness: 2px;"
                                role="progressbar">
                            80% <br> to redeem
                        </div>

                    </div>
                    <div class="stat-title text-black">Trash deposited</div>
                    <div class="stat-value text-black">69</div>
                    <div class="stat-desc text-black">From January 1st to February 1st</div>
                </div>
            </div>
            <p class="py-6 text-black">
                Have recyclable in hand?
            </p>
            <button class="btn btn-primary" on:click={() => navigate("/map")}>Find bin</button>
        </div>
    </div>
</div>
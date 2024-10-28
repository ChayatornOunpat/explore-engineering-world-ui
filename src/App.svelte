<script>
    import {Router, Route, navigate} from "svelte-navigator";
    import Home from "./lib/Home.svelte";
    import Map from "./lib/Map.svelte"
    import Redeem from "./lib/Redeem.svelte";
</script>

<div class="min-h-screen">
    <div class="drawer min-h-screen">
        <input id="my-drawer" type="checkbox" class="drawer-toggle"/>
        <div class="drawer-content min-h-screen">
            <div class="navbar bg-stone-800 w-screen sticky top-0 z-40">
                <div class="flex-none">
                    <label for="my-drawer" class="ml-2 btn btn-square btn-ghost drawer-button">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                             class="inline-block w-5 h-5 stroke-current">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                  d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </label>
                </div>
                <div class="flex-1">
                </div>
                <div class="avatar">
                    <div class="w-16 rounded-full">
                        <img src="https://media.istockphoto.com/id/1332100919/vector/man-icon-black-icon-person-symbol.jpg?s=612x612&w=0&k=20&c=AVVJkvxQQCuBhawHrUhDRTCeNQ3Jgt0K1tXjJsFy1eg="/>
                    </div>
                </div>
            </div>
            <Router>
                <Route path="/" component={Home}/>
                <Route path="/map" component={Map}/>
                <Route path="/redeem" component={Redeem}/>
            </Router>
        </div>
        <div class="drawer-side z-50">
            <label for="my-drawer" class="drawer-overlay"></label>
            <ul class="menu p-4 w-80 h-full bg-stone-800 text-base-content">
                <li><a on:click={() => navigate("/")}>home</a></li>
                <li><a on:click={() => navigate("/map")}>map</a></li>
                <li><a on:click={() => navigate("/redeem")}>redeem</a></li>
            </ul>
        </div>
    </div>
    <footer class="footer footer-center bg-stone-800 text-base-content p-4 sticky bottom-0">
        <p class="text-2xl mr-6 text-center text-white">TreasureTrash</p>
    </footer>
</div>

<style>

</style>

<div id="navbar">
    <div id="container">
        <div class="boxes-nav">
            <Link to="/">
                Home
            </Link>
        </div>

        <div class="boxes-nav">

        </div>

        <div class="boxes-nav">

        </div>

        <div class="boxes-nav">
        </div>
    </div>
</div>


<script>
    import { Link } from 'svelte-navigator'
</script>

<style lang="scss">
    #navbar {
        width: 100%;
        height: 65px;
        background-color: red;
        display: flex;
        justify-content: center;
    }
    #container {
        width: 80%;
        height: 100%;
        display: flex;
    }
    .boxes-nav{
        width: 20%;
        background-color: blue;
        height: 100%;
        margin: 0 5px 0 5px;
    }
</style>
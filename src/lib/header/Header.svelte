<script>
    import logo from '../INK-logo.svg'

    let isMenuOpen = false;

    function toggleMenu(){
        isMenuOpen = !isMenuOpen;
    }
</script>

<header>
    <a href="/">
        <img src={logo} alt="logo" />
    </a>
    <nav class:open={isMenuOpen}>
        <ul>
            <li><a href="/" class="current">Home</a></li>
            <li><a href="/about">About</a></li>
            <li><a href="/promise">Promise</a></li>
            <li class="sponsor-button"><a href="/becomeSponsor" class="sponsor-button-text">Become a sponsor</a></li>
        </ul>
    </nav>

    <button class="burger-menu" on:click={toggleMenu}>
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
    </button>

</header>

<style>

    header{
        padding: 1.5em;
        background-color: var(--charcoal);

        display: flex;
        justify-content: space-between;
        align-items: center;
        position: relative;

    }

    header img{
        width: clamp(25px, 8vw, 65px);
    }
    
    header img:hover{
        scale: 1.1;
    }

    header a{
        text-transform: uppercase;
    }

    /* Mobile slider nav */
    nav{
        display: none;
    }

    @keyframes slideIn {
    from {
        height: 0;
        opacity: 0;
    }
    to {
        height: 35vh; /* Replace with the actual height of the `.nav` element */
        opacity: 1;
    }
}

    nav.open{
        display: block;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100vw;
        height: 35vh;
        z-index: 1;
        overflow: visible;
        background-color: var(--candelLight);
        transition:  0.4s ease-out;
        animation: slideIn 0.4s ease-in-out forwards; /* Apply animation */
    }

    

    nav ul{
        display: flex;
        margin: 2vh 4vh;
        gap: 5vh;
        flex-direction: column;
        align-items: center;
    }

    nav a{
        color: var(--charcoal);
        font-size: 1.6em;
        font-family: 'Apercu';
        font-weight: 900;
        letter-spacing: 0.08rem;
        line-height: 100%;
    }

    .current{
        position: relative;
    }

    .current::after{
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: var(--justWhite);
    }

    nav li{
        margin-bottom: .5em;
    }

    nav li:hover{
        scale: 1.1;
    }


    .sponsor-button{
        border: none;
        border-radius: 3em;
        padding: .7em 1.2em;
        background-color: var(--pictonBlue);
    }

    .sponsor-button-text{
        font-size: .9em;
        color: var(--justWhite);
    }

    /* Hambuger menu */

    .burger-menu{
        height: 3em;
        aspect-ratio: 1;
        border: 2px solid var(--candelLight);
        background-color: var(--candelLight);
        border-radius: 50%;

        display: flex;
        justify-content: center;
        align-items: center;
    }

    .burger-menu > div{
        height: 2px;
        width: 14px;
        background-color: var(--charcoal);
        position: absolute;
    }

    .bar1{
        transform: translateY(-5px);
    }

    .bar3{
        transform: translateY(5px);
    }



</style>

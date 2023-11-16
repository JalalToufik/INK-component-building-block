<script>
    import logo from '../INK-logo.svg'
</script>

<header>
    <nav>
        <a href="/">
            <img src={logo} alt="logo" />
        </a>
        <ul>
            <li>
                <a href="/about" class="">About</a>
            </li>
            <li>
                <a href="/promise" class="">Promise</a>
            </li>
            <li>
                <a href="/becomeSponsor"class="">Become a sponsor</a>
            </li>
        </ul>
    </nav>

    <div class="burger-menu">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
    </div>

</header>

<style>

    header{
        padding: 2em;
        background-color: var(--jungleGreen);
    }

    nav{
        display: flex;
        justify-content: space-between;
    }

    nav img{
        width: clamp(25px, 8vw, 65px);
    }
    
    nav img:hover{
        scale: 1.1;
    }

    nav ul{
        display: flex;
        gap: 2em;
        align-items: center;
    }

    nav a{
        color: var(--justWhite);
    }
</style>

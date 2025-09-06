<script>
    import logo from '../assets/logo.png';
    let menuOpen = false;
    function toggleMenu() {
        menuOpen = !menuOpen;
    }
</script>

<div class="header-container">
    <div class="logo">
        <img src={logo} alt="">
    </div>
    <div class="transfers">
        <a href="">About</a>
        <a href="https://ideathon6-0.ecellnmit.in/">Events</a>
        <a href="https://www.ecellnmit.in/team/index.html">Team</a>
        <a href="https://www.ecellnmit.in/blogs/index.html">Blogs</a>
        <a href="">Contact</a>
    </div>
    <button>Join Us</button>
    <div class="menu-icon" on:click={toggleMenu}>
        <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect y="5" width="24" height="2" rx="1" fill="#00FFFF"/>
            <rect y="11" width="24" height="2" rx="1" fill="#00FFFF"/>
            <rect y="17" width="24" height="2" rx="1" fill="#00FFFF"/>
        </svg>
    </div>
    {#if menuOpen}
        <div class="dropdown-menu">
            <a href="">About</a>
            <a href="https://ideathon6-0.ecellnmit.in/">Events</a>
            <a href="https://www.ecellnmit.in/team/index.html">Team</a>
            <a href="https://www.ecellnmit.in/blogs/index.html">Blogs</a>
            <a href="">Contact</a>
        </div>
    {/if}
</div>

<style>
    .header-container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.3vh 1.5vw;
        position: relative;
    }
    .menu-icon {
        display: none;
        cursor: pointer;
        margin-left: 1vw;
    }
    .dropdown-menu {
        display: none;
        position: absolute;
        top: 100%;
        right: 0;
        background: #0E1A2B;
        box-shadow: 0 8px 24px rgba(0, 255, 255, 0.15);
        border-radius: 0.5rem;
        padding: 1rem 2rem;
        z-index: 100;
        flex-direction: column;
        gap: 1rem;
    }
    .dropdown-menu a {
        color: #00FFFF;
        text-decoration: none;
        font-family: 'Poppins', sans-serif;
        font-size: 1.1rem;
        font-weight: 500;
        transition: color 0.2s;
    }
    .dropdown-menu a:hover {
        color: #FFFFFF;
    }

    .logo img {
        height: 13vh;
        background:#0E1A2B ;
    }

    .transfers {
        display: flex;
        gap: 4vw;
    }
    .transfers a {
        text-decoration: none;
        font-family: 'Poppins', sans-serif;
        font-weight: 400;
        font-size: 1.2rem;
        transition: color 0.3s ease;
        color: #FFFFFF;
    }
    button {
        padding: 0.8vh 1.0vw;
        border-radius: 1rem;
        border: 2px solid #00FFFF;
        color: #00FFFF;
        font-family: 'Poppins', sans-serif;
        font-weight: 500;
        font-size: 1.1rem;
        cursor: pointer;
    } 
    @media (max-width: 768px) {
        .logo img {
            height: 8vh;
        }
        .transfers {
            display: none;
        }
        .menu-icon {
            display: block;
        }
        .dropdown-menu {
            display: flex;
        }
        button {
            padding: 0.6vh 0.8vw;
            font-size: 1rem;
        } 
    }
</style>
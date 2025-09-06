<script>
    import logo from '../assets/logo.png';    
</script>

<div>
    <div class="footer">
        <img src={logo} alt="">
        <p>Made By Abhishek Kumar
        © E-Cell NMIT (ENIGMA)</p>
        <p class="end"> A vibrant community of aspiring entrepreneurs</p>
    </div>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        gap: 1.5vh;
        padding: 1vh 0.6vw;
        background-color: #0b1522;
    }
    div:hover{
        cursor: default;
    }
    .footer{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        gap: 1.5vh;
        padding: 1vh 0.6vw;
    }
    .footer img {
        height: 10vh;
    }
    p {
        font-family: 'Poppins', sans-serif;
        font-weight: 400;
        font-size: 1.2rem;
        color: #FFFFFF;
        margin: 0.3vh;
        padding: 0.2vh;
    }
    .end {
        font-family: 'Poppins', sans-serif;
        font-weight: 300;
        font-size: 1rem;
        color: #AAAAAA;
        margin-top: 1vh;
        padding: 0.2vh;
    }
</style>
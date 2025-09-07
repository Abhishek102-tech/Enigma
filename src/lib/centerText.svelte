<script>

</script>

<div>
    <h1>Igniting Future Entrepreneurs</h1>
    <h2>THE ENTREPRENEURSHIP CELL OF NMIT</h2>
    <h2>Empowering innovations and leadership</h2>
    <button>Join Us</button>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        gap: 1.5vh;
        padding: 2vh 1vw;
    }
    div:hover{
        cursor: default;
    }
    h1 {
        font-family: 'Orbitron', sans-serif;
        font-weight: 700;
        font-size: 3.5rem;
        color: #00FFFF;
        text-transform:uppercase;
        margin: 0.5vh;
        padding: 0.2vh;
    }
    
    h2 {
        font-family: 'Poppins', sans-serif;
        font-weight: 400;
        font-size: 1.5rem;
        color: #FFFFFF;
        margin: 0.3vh;
        padding: 0.2vh;
    }
    
    button {
        padding: 1.5vh 1.7vw;
        border-radius: 1rem;
        border: 2px solid #00FFFF;
        color: #00FFFF;
        font-family: 'Poppins', sans-serif;
        font-weight: 500;
        font-size: 1.4rem;
        cursor: pointer;
    } 
    button:hover {
        background: #00FFFF;
        color: #0E1A2B;
        transition: background 0.2s, color 0.2s;
        animation: glow 1.5s infinite;
    }
    @keyframes glow {
        0% {
            box-shadow: 0 0 5px #00FFFF;
        }
        50% {
            box-shadow: 0 0 20px #00FFFF;
        }
        100% {
            box-shadow: 0 0 5px #00FFFF;
        }
    }
    @media (max-width: 768px) {
        h1 {
            font-size: 2.2rem;
        }
        h2 {
            font-size: 1.2rem;
        }
        button {
            font-size: 1.2rem;
            padding: 1vh 1.2vw;
        }
    }
</style>
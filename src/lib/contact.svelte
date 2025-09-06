<script>
 import linkedin from '../assets/linkedin.svg';
 import instagram from '../assets/instagram.svg';
 import facebook from '../assets/facebook.svg';
</script>

<div>
    <h1>Contact</h1>
    <div class="contacts">
        <p>Email: <a href="mailto:ecell@nmit.ac.in">ecell@nmit.ac.in </a></p>
        <a href="https://www.linkedin.com/company/enigma-e-cell-nmit/"><img src={linkedin} alt=""></a>
        <a href="https://www.instagram.com/ecellnmit/?hl=en"><img src={instagram} alt=""></a>
        <a href="https://www.facebook.com/ecellnmit/"><img src={facebook} alt=""></a>
    </div>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 1vh 0.6vw;
        gap: 1.5vh;
    }
    div:hover{
        cursor: default;
    }
    h1 {
        font-family: 'Orbitron', sans-serif;
        font-weight: 700;
        font-size: 3.0rem;
        color: #00FFFF;
        text-transform:uppercase;
        margin: 0.5vh;
        padding: 0.2vh;
    }
    .contacts {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        gap: 2vw;
    }
    .contacts p {
        font-family: 'Poppins', sans-serif;
        font-weight: 400;
        font-size: 1.2rem;
        color: #FFFFFF;
        margin: 0.3vh;
        padding: 0.2vh;
    }
    .contacts a img {
        height: 4vh;
        color: #00FFFF;
        transition: transform 0.3s ease, filter 0.3s ease;
    }
    .contacts a img:hover {
        transform: scale(1.1);
        filter: brightness(1.2);
        -webkit-filter: brightness(1.2);
    box-shadow: 0 0 16px 4px #00aaff;
        cursor: pointer;
    }
</style>
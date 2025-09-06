<script>
    import rocket from '../assets/rocket.png';
    let aboutText = [
        "The Entrepreneurship Cell (E-Cell) of NMIT is a student-driven organization dedicated to fostering innovation, entrepreneurship, and leadership among students. Established with the vision of creating a vibrant entrepreneurial ecosystem within the campus, E-Cell NMIT aims to empower students to transform their ideas into successful ventures.",
        "Our mission is to provide a platform for aspiring entrepreneurs to learn, collaborate, and grow. We organize various events, workshops, and competitions throughout the year to nurture entrepreneurial skills and mindset. Through these initiatives, we strive to create an environment that encourages creativity, critical thinking, and problem-solving.",
        "E-Cell NMIT collaborates with industry experts, successful entrepreneurs, and mentors to provide valuable insights and guidance to our members. We believe in the power of networking and community building, and we actively engage with local startups, incubators, and accelerators to create opportunities for our members.",
        "Join us on this exciting journey of innovation and entrepreneurship. Whether you have a groundbreaking idea or simply want to learn more about the startup ecosystem, E-Cell NMIT welcomes you to be a part of our dynamic community."
    ];
</script>

<div>
    <div class="about">
    <h1>About</h1>
    <div class="box">
    <p>{aboutText[0]}</p>
    </div>
    </div>
    <img src={rocket} alt="" class="rocket">
</div>

<style>
    div {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        align-items: center;
        justify-content: center;
        padding: 1vh 0.6vw;
    }
    .about{
        display: flex;
        flex-direction: column;
        gap: 1.5vh;
        padding: 1vh 0.6vw;
    }
    .about:hover{
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
    .box {
        border: 3px solid #004f75;
        text-align: center;
        max-width: 800px;
        border-radius: 10px;
        padding: 2.6vh 2.4vw;
        color: #00FFFF;
        box-shadow: 3px 2px 8px #00FFFF;
        width: 40vw;
    }
    .box:hover{
        cursor: default;
    }
    p {
        font-family: 'Poppins', sans-serif;
        font-weight: 400;
        font-size: 1.2rem;
        color: #FFFFFF;
        margin: 1vh 0;
        line-height: 1.6;
    }
    @media (max-width: 768px) {
        div {
        }
        .box {
            width: 40vw;
        }
        p{
            font-size: 0.7rem;
        }
        .rocket {
            height: 30vh;
        }
    }
</style>


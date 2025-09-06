<script>
    import rocket from '../assets/rocket.png';
    let aboutText = [
        "The Entrepreneurship Cell (E-Cell) of NMIT is a student-driven organization dedicated to fostering innovation, entrepreneurship, and leadership among students. Established with the vision of creating a vibrant entrepreneurial ecosystem within the campus, E-Cell NMIT aims to empower students to transform their ideas into successful ventures.",
        "Our mission is to provide a platform for aspiring entrepreneurs to learn, collaborate, and grow. We organize various events, workshops, and competitions throughout the year to nurture entrepreneurial skills and mindset. Through these initiatives, we strive to create an environment that encourages creativity, critical thinking, and problem-solving.",
        "E-Cell NMIT collaborates with industry experts, successful entrepreneurs, and mentors to provide valuable insights and guidance to our members. We believe in the power of networking and community building, and we actively engage with local startups, incubators, and accelerators to create opportunities for our members.",
        "Join us on this exciting journey of innovation and entrepreneurship. Whether you have a groundbreaking idea or simply want to learn more about the startup ecosystem, E-Cell NMIT welcomes you to be a part of our dynamic community."
    ];
    let current = 0;
    let isMobile = false;
    let startX = 0;
    let endX = 0;

    // Detect mobile
    if (typeof window !== 'undefined') {
        isMobile = window.matchMedia('(max-width: 768px)').matches;
        window.addEventListener('resize', () => {
            isMobile = window.matchMedia('(max-width: 768px)').matches;
        });
    }

    function prev() {
        current = (current - 1 + aboutText.length) % aboutText.length;
    }
    function next() {
        current = (current + 1) % aboutText.length;
    }
    function handleTouchStart(e) {
        startX = e.touches[0].clientX;
    }
    function handleTouchEnd(e) {
        endX = e.changedTouches[0].clientX;
        if (startX - endX > 50) {
            next();
        } else if (endX - startX > 50) {
            prev();
        }
    }
</script>

<div>
    <div class="about">
        <h1>About</h1>
        <div class="box"
            on:touchstart={isMobile ? handleTouchStart : undefined}
            on:touchend={isMobile ? handleTouchEnd : undefined}
        >
            <p>{aboutText[current]}</p>
            {#if !isMobile}
                <div class="slider-buttons">
                    <button class="slider-btn left" on:click={prev}>&lt;</button>
                    <button class="slider-btn right" on:click={next}>&gt;</button>
                </div>
            {/if}
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
    .slider-buttons {
        display: flex;
        justify-content: center;
        gap: 2vw;
        margin-top: 1vh;
    }
    .slider-btn {
        background: #0E1A2B;
        color: #00FFFF;
        border: 2px solid #00FFFF;
        border-radius: 50%;
        width: 2.5rem;
        height: 2.5rem;
        font-size: 1.5rem;
        cursor: pointer;
        transition: background 0.2s, color 0.2s;
    }
    .slider-btn:hover {
        background: #00FFFF;
        color: #0E1A2B;
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
        display: flex;
        flex-direction: column;
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


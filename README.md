# HTML-PROJECT
// Initialize Swiper
        const swiper = new Swiper('.swiper', {
            effect: 'coverflow',
            grabCursor: true,
            centeredSlides: true,
            slidesPerView: 'auto',
            loop: true,
            autoplay: {
                delay: 3000,
                disableOnInteraction: false,
            },
            coverflowEffect: {
                rotate: 50,
                stretch: 0,
                depth: 100,
                modifier: 1,
                slideShadows: true,
            },
            pagination: {
                el: '.swiper-pagination',
            },
        });

        // Simulated live score updates
        function updateScores() {
            const scores = [
                { teams: "IND vs AUS", score: "325/4 (45.2)" },
                { teams: "Man U vs Chelsea", score: "2 - 1" },
                { teams: "India vs Malaysia (Badminton)", score: "21-18, 19-21, 21-16" },
                { teams: "Telugu Titans vs UP Yodhas (Kabaddi)", score: "33-28" },
                { teams: "Lakers vs Warriors (Basketball)", score: "108-102" }
            ];

            const scoreBoard = document.getElementById('scoreBoard');
            scoreBoard.innerHTML = scores.map(score => `
                <div class="score-card">
                    <h3>${score.teams}</h3>
                    <p>${score.score}</p>
                    <a href="https://www.flashscore.in" target="_blank">View more scores on FlashScore</a>
                </div>
            `).join('');
        }
        // Create footer with contact information and display horizontally
        const footer = document.createElement('footer');
        footer.innerHTML = `
            <div class="contact-info" style="display: flex; justify-content: space-around; flex-wrap: wrap; font-family: 'Times New Roman', Times, serif;">
                <div class="contact-card" style="flex: 1; min-width: 250px; text-align: center; padding: 10px;">
                    <h4>Boda Dhanesh</h4>
                    <p>Sports Director</p>
                    <p>Email: bodadhanesh12@gmail.com</p>
                    <p>Phone: +91 9398469736</p>
                </div>
                <div class="contact-card" style="flex: 1; min-width: 250px; text-align: center; padding: 10px;">
                    <h4>Maremalla Rajaram</h4>
                    <p>Marketing Manager</p>
                    <p>Email: rajaramrls2006@gmail.com.com</p>
                    <p>Phone: +91 7981137616</p>
                </div>
                <div class="contact-card" style="flex: 1; min-width: 250px; text-align: center; padding: 10px;">
                    <h4>Yenduru Naga Satwik Sai Ganesh</h4>
                    <p>Technical Support</p>
                    <p>Email: sathyayenduru@gmail.com</p>
                    <p>Phone: +91 9977991626</p>
                </div>
                <div class="contact-card" style="flex: 1; min-width: 250px; text-align: center; padding: 10px;">
                    <h4>Aryan Singh</h4>
                    <p>Customer Relations</p>
                    <p>Email: aryansingh@gmail.com</p>
                    <p>Phone: +91 9023353948</p>
                </div>
            </div>
        `;
        document.body.appendChild(footer);

        setInterval(updateScores, 5000);
        updateScores();

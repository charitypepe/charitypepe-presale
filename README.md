<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Charity PEPE (CPEPE) Presale</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            min-height: 100vh;
            margin: 0;
            background: linear-gradient(45deg, #28a745, #218838);
            animation: backgroundAnimation 5s infinite alternate;
            overflow-x: hidden;
            position: relative;
            text-align: center;
        }
        @keyframes backgroundAnimation {
            from { background: linear-gradient(45deg, #28a745, #218838); }
            to { background: linear-gradient(45deg, #218838, #28a745); }
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 900px;
            position: relative;
            z-index: 10;
            opacity: 0;
            animation: fadeIn 1s forwards;
        }
        @keyframes fadeIn {
            to { opacity: 1; }
        }
        .timeline {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 50px 0;
            padding: 30px;
            background: #fff;
            border-radius: 15px;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }
        .timeline-item {
            text-align: center;
            width: 22%;
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-in-out;
        }
        .timeline-item span {
            display: block;
            width: 100px;
            height: 100px;
            background: #f9f9f9;
            border-radius: 50%;
            border: 5px solid #007bff;
            margin: auto;
            line-height: 100px;
            font-size: 40px;
            color: #007bff;
            cursor: pointer;
        }
        .countdown {
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
            color: #007bff;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
        }
        .faq, .how-to-buy, .subscribe, .progress-bar, .wallet, .socials {
            margin-top: 40px;
            text-align: left;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        .money {
            position: absolute;
            width: 50px;
            height: auto;
            opacity: 0.9;
            animation: fallingMoney 4s linear forwards;
        }
        @keyframes fallingMoney {
            from { transform: translateY(-50px) rotate(0deg); opacity: 1; }
            to { transform: translateY(500px) rotate(360deg); opacity: 0; }
        }
        .subscribe input {
            padding: 10px;
            margin-right: 10px;
            border: 1px solid #007bff;
            border-radius: 5px;
        }
        .subscribe button, .wallet button {
            padding: 10px 20px;
            background: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .subscribe button:hover, .wallet button:hover {
            background: #0056b3;
        }
        .progress-bar .bar {
            width: 100%;
            height: 20px;
            background: #f0f0f0;
            border-radius: 10px;
            overflow: hidden;
        }
        .progress-bar .fill {
            height: 100%;
            background: #007bff;
            width: 60%;
            transition: width 1s ease-in-out;
        }
        .socials a {
            margin: 0 10px;
            color: #007bff;
            text-decoration: none;
            font-size: 18px;
        }
        .socials a:hover {
            color: #0056b3;
        }
        @media (max-width: 768px) {
            .timeline {
                flex-direction: column;
                padding: 15px;
            }
            .timeline-item {
                width: 100%;
                margin-bottom: 20px;
                opacity: 1;
                transform: none;
            }
            .timeline-item span {
                width: 80px;
                height: 80px;
                line-height: 80px;
                font-size: 30px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Charity PEPE (CPEPE) Presale</h1>
        <div class="countdown" id="countdown">Loading...</div>
        <div class="progress-bar">
            <h2>Presale Progress</h2>
            <div class="bar">
                <div class="fill"></div>
            </div>
            <p>60% of tokens sold (12,000 / 20,000 CPEPE)</p>
        </div>
        <div class="timeline">
            <div class="timeline-item" id="presale">
                <span onclick="playSound()">📅</span>
                <p>Presale</p>
            </div>
            <div class="timeline-item" id="liquidity">
                <span onclick="playSound()">💰</span>
                <p>Liquidity Pool</p>
            </div>
            <div class="timeline-item" id="transfers">
                <span onclick="playSound()">🔓</span>
                <p>Transfer Unlock</p>
            </div>
            <div class="timeline-item" id="voting">
                <span onclick="playSound()">🗳️</span>
                <p>Voting for Donations</p>
            </div>
        </div>
        <div class="how-to-buy">
            <h2>How to Buy CPEPE</h2>
            <ol>
                <li>Connect your wallet (MetaMask, TrustWallet, etc.).</li>
                <li>Choose the amount of CPEPE tokens.</li>
                <li>Confirm the transaction.</li>
                <li>Wait for the transaction to complete.</li>
            </ol>
        </div>
        <div class="wallet">
            <h2>Presale Wallet Address</h2>
            <p id="walletAddress">0x1234...5678</p>
            <button onclick="copyAddress()">Copy Address</button>
        </div>
        <div class="faq">
            <h2>Frequently Asked Questions</h2>
            <p><strong>When will the presale end?</strong> - December 31, 2025</p>
            <p><strong>How do I stake my CPEPE?</strong> - Staking will be available after the presale.</p>
        </div>
        <div class="subscribe">
            <h2>Subscribe for Updates</h2>
            <form id="subscribeForm">
                <input type="email" placeholder="Enter your email" required>
                <button type="submit">Subscribe</button>
            </form>
            <p id="subscribeMessage" style="display: none;">Thank you for subscribing!</p>
        </div>
        <div class="socials">
            <h2>Join Our Community</h2>
            <a href="https://www.charitypepe.com/" target="_blank">Website</a>
            <a href="https://x.com/CharityPePE" target="_blank">X.com</a>
            <a href="https://t.me/CharityPP" target="_blank">Telegram</a>
        </div>
    </div>
    <script>
        function playSound() {
            const audio = new Audio('https://www.soundjay.com/button/beep-07.wav');
            audio.play().catch(error => console.log("Error playing sound:", error));
        }

        function startCountdown() {
            const endDate = new Date("December 31, 2025 23:59:59").getTime();
            const countdownElement = document.getElementById("countdown");
            if (!countdownElement) {
                console.log("Countdown element not found!");
                return;
            }
            const interval = setInterval(() => {
                const now = new Date().getTime();
                const timeLeft = endDate - now;
                if (timeLeft <= 0) {
                    countdownElement.innerHTML = "Presale has ended!";
                    clearInterval(interval);
                    return;
                }
                const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
                const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
                countdownElement.innerHTML = `Time left: ${days}d ${hours}h ${minutes}m ${seconds}s`;
            }, 1000);
        }

        function createMoney() {
            if (document.querySelectorAll('.money').length >= 10) return;
            const money = document.createElement("img");
            money.classList.add("money");
            money.src = "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f6/Euro_banknotes.png/320px-Euro_banknotes.png";
            money.style.left = `${Math.random() * (window.innerWidth - 50)}px`;
            money.style.animationDuration = `${Math.random() * 3 + 2}s`;
            document.body.appendChild(money);
            money.addEventListener('animationend', () => money.remove());
        }

        function copyAddress() {
            const address = document.getElementById("walletAddress").innerText;
            navigator.clipboard.writeText(address).then(() => {
                alert("Address copied to clipboard!");
            });
        }

        window.onload = function() {
            startCountdown();
            const timelineItems = document.querySelectorAll('.timeline-item');
            timelineItems.forEach((item, index) => {
                setTimeout(() => {
                    item.style.opacity = '1';
                    item.style.transform = 'translateY(0)';
                }, index * 300);
            });
            setInterval(createMoney, 2000);

            // Interactive timeline
            document.querySelectorAll('.timeline-item span').forEach(item => {
                item.addEventListener('click', function() {
                    playSound();
                    const info = {
                        presale: "Presale starts now and ends on Dec 31, 2025.",
                        liquidity: "Liquidity pool will be locked after presale.",
                        transfers: "Transfers unlock after liquidity is added.",
                        voting: "Vote for charities starting Jan 2026."
                    };
                    const id = this.parentElement.id;
                    alert(info[id]);
                });
            });

            // Subscribe form
            document.getElementById("subscribeForm").addEventListener("submit", function(e) {
                e.preventDefault();
                document.getElementById("subscribeMessage").style.display = "block";
                this.reset();
                setTimeout(() => {
                    document.getElementById("subscribeMessage").style.display = "none";
                }, 3000);
            });
        };
    </script>
</body>
</html>

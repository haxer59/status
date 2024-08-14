<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: #000000;
            color: #e0e0e0;
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            font-size: 14px;
            align-items: center;
        }

        .container {
            padding: 30px;
            width: 80%;
            margin: 0 auto;
            background-color: #040b14;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            animation: fadeIn 1s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .content {
            padding: 20px;
            align-items: center;
            justify-content: center;
        }

        .header-container {
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .button-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

      .button {
    background-color: #275ABF;
    border: 1px solid #1C4B82;
    color: white;
    padding: 12px 25px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 18px;
    margin-top: 20px;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    border-radius: 5px;
    transition: background-color 0.3s ease, transform 0.3s ease;
}
    .button:hover {
    background-color: #1E468F;
    transform: translateY(-2px);
}
      .sort-container label {
    color: #bbb;
    font-size: 16px;
    margin-right: 10px;
}

        .header-Image {
            height: 250px;
            margin: auto;
        }

        h1 {
            font-size: 24px;
            color: #2196F3;
            margin-bottom: 20px;
            text-align: center;
        }

        .status-card {
            background: #02070e;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-left: 5px solid #76ff03;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s ease, transform 0.3s ease;
            position: relative;
            text-decoration: none;
        }

        .status-card:hover {
            background-color: rgba(255, 255, 255, 0.1);
            transform: translateY(-5px);
        }

        .status-card:hover .go-back-button {
            display: block;
        }

        .go-back-button {
            display: none;
            position: absolute;
            top: 10px;
            right: 10px;
            background: linear-gradient(to bottom, #3498db, #2980b9);
            border: none;
            color: white;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }

        .status-card.updating {
            border-left-color: #E07501;
        }

        .status-card.under-development {
            border-left-color: #E0CC01;
        }

        .status-card.undetected {
            border-left-color: #01E11F;
        }

        .status-card.offline {
            border-left-color: #E11901;
        }

        .status-card p {
            margin: 0;
            padding: 0;
            color: #bbb;
        }

        .status-card .image-container img {
            width: 64px;
            height: 64px;
            margin-right: 10px;
        }

        .status-card .title {
            font-weight: bold;
            color: #fff;
        }

        .status-card .fas {
            margin-right: 10px;
        }

        .status-card .status {
            font-weight: bold;
            text-transform: uppercase;
        }

        .status-card .status.undetected {
            color: #01E11F;
        }

        .status-card .status.under-development {
            color: #E0CC01;
        }

        .status-card .status.updating {
            color: #E07501;
        }

        .status-card .status.offline {
            color: #E11901;
        }
        
        .sort-select {
    padding: 10px;
    font-size: 16px;
    border-radius: 5px;
    border: 1px solid #275ABF;
    background-color: #1e1e1e;
    color: #fff;
    transition: border-color 0.3s ease, background-color 0.3s ease;
}
    .sort-select:hover, .sort-select:focus {
    border-color: #1E468F;
    outline: none;
    background-color: #2C2C2C;
}
    </style>
</head>

<body>

    <div class="container">
        <!-- Go Back Button -->
        <div style="text-align: center; margin-bottom: 20px;">
            <button class="button" onclick="window.location.href='https://www.moddingassociation.net/store/'">Go Back</button>
        </div>
        <div class="sort-container" style="margin-bottom: 20px; text-align: center;">
            <label for="sort-status">Sort by Status: </label>
            <select id="sort-status" class="sort-select" onchange="sortCards()">
                <option value="none">None</option>
                <option value="undetected">Undetected</option>
                <option value="updating">Updating</option>
            </select>
        </div>
        <div class="status-cards">
            <!-- TEMP SPOOFER -->
            <a href="https://www.moddingassociation.net/store/category/53-temporary-spoofer/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/QkHn4W5/hwidspoofer.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">EAC / BE TEMP SPOOFER</p>
                    <p>A HWID Spoofer For EasyAntiCheat & Battleye & Ricochet Games</p>
                    <p>Released on 28/04/2024</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- EAC/BE PERM SPOOFER -->
            <a href="https://www.moddingassociation.net/store/product/968-permanent-eacbe-spoofer-onetime/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/QkHn4W5/hwidspoofer.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">EAC/BE PERMANENT SPOOFER</p>
                    <p>A Permanent HWID Spoofer for All Games</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- VAL PERM SPOOFER -->
            <a href="https://www.moddingassociation.net/store/product/177-permanent-valorant-spoofer-onetime/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/QkHn4W5/hwidspoofer.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">VALORANT PERMANENT SPOOFER</p>
                    <p>A Permanent HWID Spoofer for All Games</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- VALORANT FULL -->
            <a href="https://www.moddingassociation.net/store/category/106-ma-valorant-cheat-full-cheat/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/tqD0KNP/valorant-logo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">VALORANT FULL</p>
                    <p>Full Cheat for Valorant</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- VALORANT ICONS -->
            <a href="https://www.moddingassociation.net/store/category/171-ma-valorant-icon-esp-only/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/tqD0KNP/valorant-logo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">VALORANT ICONS</p>
                    <p>ESP Only Cheat for Valorant</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- VALORANT SKINCHANGER -->
            <a href="https://www.moddingassociation.net/store/category/180-ma-valorant-skinchanger/" class="status-card updating">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/tqD0KNP/valorant-logo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">VALORANT SKINCHANGER</p>
                    <p>ESP Only Cheat for Valorant</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status updating">updating</p>
                </div>
            </a>

            <!-- VALORANT PRIVATE -->
            <a href="https://www.moddingassociation.net/store/product/913-ma-valorant-private-month/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/tqD0KNP/valorant-logo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">VALORANT PRIVATE</p>
                    <p>Valornat Private Cheat</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- XDefiant -->
            <a href="https://www.moddingassociation.net/store/category/275-xdefiant-cheatshacks/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/TgQDR9v/xdefiant.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">XDefiant</p>
                    <p>Cheat for XDefiant Game!</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- EFT -->
            <a href="https://www.moddingassociation.net/store/category/12-eft-cheatshacks/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/NS6zt76/1111.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">Escape From Tarkov</p>
                    <p>ESP Only cheat for EFT</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- RUST FULL -->
            <a href="https://www.moddingassociation.net/store/category/19-ma-rust-full/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/gTp4s6d/rustimg.jpg" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">RUST FULL</p>
                    <p>Full Cheat for Rust</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- FORTNITE -->
            <a href="https://www.moddingassociation.net/store/category/92-fortnite-internal/" class="status-card updating">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/Km9XzRk/fortnite-logo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">FORTNITE</p>
                    <p>Full Tourney Cheat for Fortnite</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status updating">updating</p>
                </div>
            </a>

            <!-- FORTNITE EXTERNAL -->
            <a href="https://www.moddingassociation.net/store/product/930-ma-fortnite-external-day/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/Km9XzRk/fortnite-logo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">FORTNITE EXTERNAL</p>
                    <p>External Fortnite Cheat</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- APEX BRAVO -->
            <a href="https://www.moddingassociation.net/store/category/173-ma-apex-bravo/" class="status-card updating">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/PWQQT80/apexlogo.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">APEX BRAVO</p>
                    <p>Full Cheat for Apex Legends</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status updating">updating</p>
                </div>
            </a>

            <!-- DAYZ -->
            <a href="https://www.moddingassociation.net/store/category/34-dayz-cheatshacks/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/GtXnXJ7/dayz-1640044421966.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">DAYZ</p>
                    <p>Full Cheat for DAYZ</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- R6 LITE -->
            <a href="https://www.moddingassociation.net/store/category/84-ma-r6-lite/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/MRj3hWy/r6-siege-button-02jpg-b778df.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">R6 Lite Cheat</p>
                    <p>Lite Cheat for Rainbow6Siege</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- R6 FULL -->
            <a href="https://www.moddingassociation.net/store/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/MRj3hWy/r6-siege-button-02jpg-b778df.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">R6 FULL</p>
                    <p>Full Cheat for Rainbow6Siege</p>
                    <p>Just Got Released!</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- ARMA 3 -->
            <a href="https://www.moddingassociation.net/store/category/281-arma-3-cheatshacks/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/h9cMYHf/Arm-A-3-Logo-Black-Transparent-SVG-svg.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">ARMA 3</p>
                    <p>ARMA 3 Cheat</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- HUNT -->
            <a href="https://www.moddingassociation.net/store/category/86-ma-huntshowdown/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/5vbD8DQ/ab67706c0000da84572b29ec265ba12eac1da2ef.jpg" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">HUNT SHOWDOWN</p>
                    <p>Full Cheat for HUNT SHOWDOWN</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- MW3 -->
            <a href="https://www.moddingassociation.net/store/category/40-ma-modern-warfare-3/" class="status-card updating">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/y04LhGw/codmw3-1691430628998.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">Modern Warfare 3</p>
                    <p>Full Cheat for MW3</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status updating">updating</p>
                </div>
            </a>

            <!-- COD AIO -->
            <a href="https://www.moddingassociation.net/store/category/42-ma-mw3-unlocker/" class="status-card updating">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/y04LhGw/codmw3-1691430628998.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">COD UNLOCKER</p>
                    <p>Unlock All for MW3</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status updating">updating</p>
                </div>
            </a>

            <!-- RL AI -->
            <a href="https://www.moddingassociation.net/store/category/90-rocket-league-bot-ai/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/yV6Y2B1/RLBadge-Logo-Large.png" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">RocketLeague AI</p>
                    <p>AI Cheat for Rocketleague</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- OVERWATCH 2 -->
            <a href="https://www.moddingassociation.net/store/category/96-overwatch-2-outline/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/0KB0Xrz/overwatch2-1681945442681.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">OVERWATCH 2 Outlines</p>
                    <p>ESP Only Cheat for Overwatch 2</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- OVERWATCH 2 Full -->
            <a href="https://www.moddingassociation.net/store/category/179-overwatch-2-full/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/0KB0Xrz/overwatch2-1681945442681.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">OVERWATCH 2 Full</p>
                    <p>Full Cheat for Overwatch 2</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- DBD LITE -->
            <a href="https://www.moddingassociation.net/store/category/169-ma-dbd-lite/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/Mk7cPJt/dead-by-daylight-button-replacement-1715713276872.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">DBD LITE</p>
                    <p>Lite Cheat for DeadbyDaylight</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- DBD FULL -->
            <a href="https://www.moddingassociation.net/store/category/170-ma-dbd-full/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/Mk7cPJt/dead-by-daylight-button-replacement-1715713276872.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">DBD FULL</p>
                    <p>Full Cheat for DeadbyDaylight</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>

            <!-- WAR THUNDER -->
            <a href="https://www.moddingassociation.net/store/category/37-warthunder-cheatshacks/" class="status-card updating">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/yq2dRDZ/warthunder-1640044666858.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">WAR THUNDER</p>
                    <p>Full Cheat for War Thunder</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status updating">updating</p>
                </div>
            </a>

            <!-- INSURGENCY SANDSTORM -->
            <a href="https://www.moddingassociation.net/store/category/56-insurgency-sandstorm-cheatshacks/" class="status-card undetected">
                <div>
                    <div class="image-container">
                        <img src="https://i.ibb.co/JFjFb03/insurgency-sandstorm-button-fin-1632454496057.webp" alt="ignore me">
                    </div>
                    <p style="font-size: 20px" class="title">INSURGENCY SANDSTORM</p>
                    <p>Full Cheat for Insurgency Sandstorm</p>
                    <p>--</p>
                </div>
                <div>
                    <p style="font-size: 25px" class="status undetected">undetected</p>
                </div>
            </a>
        </div>
    </div>

    <script>
        function sortCards() {
            const sortValue = document.getElementById("sort-status").value;
            const cardsContainer = document.querySelector('.status-cards');
            const cards = Array.from(cardsContainer.querySelectorAll('.status-card'));

            let sortedCards;
            if (sortValue === "undetected") {
                sortedCards = cards.sort((a, b) => a.classList.contains('undetected') ? -1 : 1);
            } else if (sortValue === "updating") {
                sortedCards = cards.sort((a, b) => a.classList.contains('updating') ? -1 : 1);
            } else {
                location.reload(); // Refresh the page
            }

            cardsContainer.innerHTML = '';
            sortedCards.forEach(card => cardsContainer.appendChild(card));
        }
    </script>
</body>

</html>

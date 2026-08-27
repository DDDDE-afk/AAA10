```
    body {
        margin: 0;
        padding: 0;
        background-color: var(--bg);
        color: var(--text);
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        height: 100vh;
        overflow: hidden;
        user-select: none;
    }

    .game-container {
        display: grid;
        grid-template-columns: 1fr 1.2fr;
        grid-template-rows: 1fr;
        width: 95vw;
        max-width: 1050px;
        height: 92vh;
        max-height: 720px;
        background: var(--panel);
        border: 1px solid var(--border);
        border-radius: 16px;
        box-shadow: 0 12px 32px rgba(0, 0, 0, 0.05);
        overflow: hidden;
    }

    .click-section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        padding: 30px 20px;
        border-right: 1px solid var(--border);
        background: #fff;
        position: relative;
        box-sizing: border-box;
    }

    .score-box {
        text-align: center;
        margin-bottom: 15px;
        height: 110px;
    }

    .balance {
        font-size: 32px;
        font-weight: 700;
        color: var(--primary);
        letter-spacing: -1px;
        word-break: break-all;
    }

    .stats-summary {
        font-size: 13px;
        color: var(--text-muted);
        margin-top: 8px;
        line-height: 1.5;
    }

    .click-btn-container {
        margin: 10px 0;
        height: 210px;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
    }

    .click-btn {
        width: 190px;
        height: 190px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 48px;
        font-weight: bold;
        cursor: pointer;
        transition: transform 0.08s ease, box-shadow 0.2s ease, background 0.3s ease;
        position: relative;
        outline: none;
        box-sizing: border-box;
        text-shadow: 0 2px 8px rgba(0,0,0,0.3);
    }
    .click-btn:active {
        transform: scale(0.90) !important;
    }

    /* 고퀄리티 그래픽 스킨 스타일 */
    .skin-style-default { border: 3px solid var(--primary); color: var(--primary); background: #ffffff; box-shadow: 0 8px 20px rgba(0,0,0,0.06); text-shadow: none; }
    .skin-style-neon { border: 3px solid #00ffcc; color: #00ffcc; background: radial-gradient(circle, #0f2b26 0%, #050d0b 100%); box-shadow: 0 0 20px #00ffcc, inset 0 0 15px rgba(0,255,204,0.3); animation: neonPulse 2s infinite alternate; }
    @keyframes neonPulse { 0% { box-shadow: 0 0 15px #00ffcc, inset 0 0 10px rgba(0,255,204,0.3); } 100% { box-shadow: 0 0 30px #00ffcc, inset 0 0 25px rgba(0,255,204,0.6); } }
    .skin-style-gold { border: 3px solid #ffe066; color: #fff; background: linear-gradient(135deg, #fcc419 0%, #fab005 50%, #e67700 100%); box-shadow: 0 10px 25px rgba(252, 196, 25, 0.4); }
    .skin-style-crystal { border: 3px solid #eebefa; color: #ffffff; background: linear-gradient(135deg, #e599f7 0%, #b197fc 50%, #63e6be 100%); box-shadow: 0 10px 25px rgba(177, 151, 252, 0.4); }
    .skin-style-pixel { border: 6px dashed #212529; border-radius: 50%; color: #212529; background: #ffec99; box-shadow: inset -6px -6px 0px #fcc419, 0 0 0 4px #212529; font-family: monospace; font-weight: bold; text-shadow: none; }
    .skin-style-abyss { border: 3px solid transparent; color: #ffffff; background: linear-gradient(#1f1442, #1f1442) padding-box, linear-gradient(135deg, #7048e8, #f783ac, #4263eb) border-box; box-shadow: 0 0 30px rgba(112, 72, 232, 0.6); }
    .skin-style-supernova { border: 3px solid #ff6b6b; color: #fff; background: radial-gradient(circle, #ff8787 0%, #c92a2a 70%, #360505 100%); box-shadow: 0 0 35px #ff6b6b; }
    .skin-style-singularity { border: 3px solid #da77f2; color: #00ffff; background: radial-gradient(circle, #0b021a 10%, #3bc9db 60%, #862e9c 100%); box-shadow: 0 0 40px #da77f2; }
    .skin-style-godhand { border: 4px solid #fff3bf; color: #fff; background: linear-gradient(135deg, #ffd43b 0%, #fcc419 40%, #ffffff 70%, #fab005 100%); box-shadow: 0 0 50px rgba(255, 212, 59, 0.9); }
    .skin-style-infinity { border: 4px solid #ffffff; color: #ffffff; background: linear-gradient(45deg, #ff007f, #7f00ff, #00f0ff, #ff007f); background-size: 300% 300%; box-shadow: 0 0 60px #00f0ff; animation: infinityShift 3s ease infinite; }
    @keyframes infinityShift { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
    .skin-style-darkmatter { border: 3px solid #343a40; color: #e9ecef; background: radial-gradient(circle, #212529 0%, #000000 100%); box-shadow: 0 0 40px #000000, inset 0 0 20px #495057; }
    .skin-style-bigbang { border: 4px solid #ffec99; color: #fff; background: radial-gradient(circle, #fff 0%, #ff922b 30%, #f783ac 60%, #5c7cfa 100%); box-shadow: 0 0 70px #ff922b; animation: bigbangPulse 1s infinite alternate; }
    @keyframes bigbangPulse { 0% { box-shadow: 0 0 40px #ff922b; } 100% { box-shadow: 0 0 80px #f783ac, 0 0 20px #fff; } }

    .skin-style-shrek { border: 4px solid #82c91e; color: #ffffff; background: radial-gradient(circle, #5c940d 0%, #2b8a3e 70%, #123b18 100%); box-shadow: 0 0 50px #82c91e; }
    .skin-style-egg { border: 4px solid #fff3bf; border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%; color: #d9480f; background: radial-gradient(circle, #ffffff 40%, #ffec99 100%); box-shadow: 0 0 40px #ffe066; text-shadow: none; }
    
    /* 브레인롯 럭키박스 디자인 (네온 그라데이션 + 네온 아웃라인) */
    .skin-style-luckybox { border: 5px solid #00ffff; border-radius: 28px; background: linear-gradient(135deg, #ff007f 0%, #7f00ff 50%, #00f0ff 100%); box-shadow: 0 0 30px #ff007f, inset 0 0 20px rgba(255,255,255,0.4); animation: brainrotBounce 1.2s infinite ease-in-out alternate; }
    @keyframes brainrotBounce { 0% { transform: translateY(0) scale(1); } 100% { transform: translateY(-6px) scale(1.02); } }

    /* 스마일 코어 디자인 */
    .skin-style-smile { border: 4px solid #ffd43b; color: #212529; background: radial-gradient(circle, #ffe066 0%, #fcc419 100%); box-shadow: 0 0 40px #ffd43b; text-shadow: none; }

    .skin-section {
        width: 100%;
        margin-top: auto;
        border-top: 1px solid var(--border);
        padding-top: 15px;
    }
    .skin-title { font-size: 14px; font-weight: bold; color: var(--accent); margin-bottom: 10px; }
    .skin-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 8px; width: 100%; max-height: 140px; overflow-y: auto; padding-right: 2px; }
    .skin-card { border: 1px solid var(--border); border-radius: 8px; padding: 8px; cursor: pointer; font-size: 11px; background: var(--bg); text-align: left; transition: all 0.15s ease; }
    .skin-card:hover { border-color: var(--accent); }
    .skin-card.active { border-color: #2f9e44; background: #ebfbee; font-weight: bold; }
    .skin-stat-tag { font-size: 9px; color: #868e96; display: block; margin-top: 2px; }

    .shop-section { padding: 20px 25px; background: var(--bg); display: flex; flex-direction: column; height: 100%; box-sizing: border-box; overflow: hidden; }
    .shop-title { font-size: 16px; font-weight: 600; margin-bottom: 10px; color: var(--primary); padding-bottom: 4px; border-bottom: 1px solid var(--border); }
    .shop-sticky-top { flex-shrink: 0; margin-bottom: 5px; }
    .rebirth-wrapper { margin-bottom: 12px; }

    .event-status-box { background: #1a1a24; color: #fff; padding: 12px 18px; border-radius: 8px; text-align: center; font-weight: bold; font-size: 13px; margin-bottom: 6px; border: 1px solid #2d2d3a; }
    .event-status-box.event-active { background: var(--event-color); border-color: var(--event-color); }
    .event-wrapper { margin-bottom: 6px; }
    .event-upgrade-wrapper { margin-bottom: 15px; }

    .shop-scroll-area { flex-grow: 1; overflow-y: auto; padding-right: 6px; display: flex; flex-direction: column; gap: 8px; }
    .shop-scroll-area::-webkit-scrollbar, .skin-grid::-webkit-scrollbar { width: 6px; }
    .shop-scroll-area::-webkit-scrollbar-track, .skin-grid::-webkit-scrollbar-track { background: transparent; }
    .shop-scroll-area::-webkit-scrollbar-thumb, .skin-grid::-webkit-scrollbar-thumb { background: #ced4da; border-radius: 3px; }

    .shop-item { display: flex; justify-content: space-between; align-items: center; background: var(--panel); padding: 12px 16px; border-radius: 8px; border: 1px solid var(--border); cursor: pointer; transition: border-color 0.15s; }
    .shop-item.disabled { opacity: 0.5; cursor: not-allowed; }
    .shop-item.maxed { border-color: var(--maxed-border); background: var(--maxed-bg); cursor: not-allowed; }
    .shop-item.lock-item { background: var(--locked); border-color: var(--border); cursor: not-allowed; color: var(--text-muted); }
    .shop-item.rebirth-item { border-color: var(--rebirth); background: #f3f0ff; }
    .shop-item.event-upgrade-item { border-color: var(--event-upgrade); background: #fff9db; }
    .shop-item.secret-egg-item { border-color: #ffe066; background: #fffde7; }

    .item-info { display: flex; flex-direction: column; }
    .item-name { font-size: 13px; font-weight: 600; display: flex; align-items: center; gap: 6px; }
    .synergy-badge { font-size: 10px; background: var(--maxed-border); color: #fff; padding: 1px 4px; border-radius: 3px; }
    .discount-badge { font-size: 10px; background: #e67e22; color: #fff; padding: 1px 4px; border-radius: 3px; }
    .item-details { font-size: 11px; color: var(--text-muted); margin-top: 2px; }
    .item-cost { font-size: 11px; font-weight: 600; color: #c92a2a; margin-top: 3px; }
    .item-level { font-size: 13px; font-weight: 700; color: #adb5bd; min-width: 75px; text-align: right; }

    .floating-text { position: absolute; font-size: 20px; font-weight: 600; color: var(--primary); pointer-events: none; animation: floatUp 0.6s ease-out forwards; }
    @keyframes floatUp { 0% { transform: translateY(0); opacity: 1; } 100% { transform: translateY(-70px); opacity: 0; } }
</style>

```

```
<div class="game-container">
    <div class="click-section" id="clickSection">
        <div class="score-box">
            <div class="balance" id="balanceDisplay">0</div>
            <div class="stats-summary">
                초당 자동 증가 GPS: <span id="gpsDisplay">0</span><br>
                클릭당 증가량 DPC: <span id="dpcDisplay">1</span><br>
                환생 횟수: <span id="rebirthDisplay">0</span> <span id="bonusDisplay">0</span>% 버프
            </div>
        </div>
        
        <div class="click-btn-container">
            <div class="click-btn skin-style-default" id="clickBtn">＋</div>
        </div>

        <div class="skin-section">
            <div class="skin-title">버튼 인터페이스 스킨</div>
            <div class="skin-grid" id="skinGrid"></div>
        </div>
    </div>

    <div class="shop-section">
        <div class="shop-sticky-top">
            <div class="shop-title">환생 아키텍처</div>
            <div class="rebirth-wrapper" id="rebirthContainer"></div>

            <div class="shop-title">실시간 이벤트 프로토콜</div>
            <div class="event-wrapper" id="eventContainer">
                <div class="event-status-box" id="eventBar">로드 중...</div>
            </div>
            <div class="event-upgrade-wrapper" id="eventUpgradeContainer"></div>
        </div>

        <div class="shop-title">업그레이드 프로토콜</div>
        <div class="shop-scroll-area" id="shopContainer"></div>
    </div>
</div>

<script>
    const MAX_LEVEL = 100;
    const TOTAL_TIERS = 143;
    const SAVE_KEY = 'minimal_clicker_v10_save';
    
    let game = {
        balance: 0,
        totalGps: 0,
        clickPower: 1,
        rebirths: 0,
        eventLevel: 0,
        currentSkin: 'default',
        ownedSkins: ['default'],
        eggClicks: 0
    };

    let eventTimer = 180; 
    let eventActiveTime = 0;
    let isEventActive = false;
    let currentEventType = 0;
    let lastTickTime = Date.now();

    const eventTypes = [
        { name: "피버 타임", desc: "클릭 폭증", mult: 1 },
        { name: "골드 러시", desc: "자동 생산 폭발", mult: 2.5 },
        { name: "하이퍼 드라이브", desc: "클릭 및 자동 가속", mult: 2 },
        { name: "퀀텀 붐", desc: "초월 에너지 극대화", mult: 4 }
    ];

    const skins = [
        { id: 'default', name: '미니멀 링', stat: '기본', cost: 0, gpsB: 1.0, cpcB: 1.0, class: 'skin-style-default' },
        { id: 'neon', name: '사이버 네온', stat: '클릭 x1.5', cost: 50000, gpsB: 1.0, cpcB: 1.5, class: 'skin-style-neon' },
        { id: 'gold', name: '골드 리치', stat: '자동 x1.5', cost: 5000000, gpsB: 1.5, cpcB: 1.0, class: 'skin-style-gold' },
        { id: 'crystal', name: '크리스탈', stat: '전체 x1.3', cost: 50000000, gpsB: 1.3, cpcB: 1.3, class: 'skin-style-crystal' },
        { id: 'pixel', name: '레트로 픽셀', stat: '클릭 x1.8', cost: 200000000, gpsB: 1.0, cpcB: 1.8, class: 'skin-style-pixel' },
        { id: 'abyss', name: '오메가 코어', stat: '전체 x2', cost: 500000000, gpsB: 2.0, cpcB: 2.0, class: 'skin-style-abyss' },
        { id: 'supernova', name: '초신성 코어', stat: '전체 x3', cost: 10000000000, gpsB: 3.0, cpcB: 3.0, class: 'skin-style-supernova' },
        { id: 'singularity', name: '차원 균열', stat: '전체 x5', cost: 500000000000, gpsB: 5.0, cpcB: 5.0, class: 'skin-style-singularity' },
        { id: 'godhand', name: '신성한 도미니온', stat: '전체 x10', cost: 100000000000000, gpsB: 10.0, cpcB: 10.0, class: 'skin-style-godhand' },
        { id: 'infinity', name: '엔드게임 인피니티', stat: '전체 x20', cost: 50000000000000000, gpsB: 20.0, cpcB: 20.0, class: 'skin-style-infinity' },
        { id: 'darkmatter', name: '다크 매터', stat: '전체 x50', cost: 1000000000000000000, gpsB: 50.0, cpcB: 50.0, class: 'skin-style-darkmatter' },
        { id: 'bigbang', name: '빅뱅 코어', stat: '전체 x100', cost: 100000000000000000000, gpsB: 100.0, cpcB: 100.0, class: 'skin-style-bigbang' },
        { id: 'shrek', name: '슈렉 코어', stat: '전체 x200', cost: 1e26, gpsB: 200.0, cpcB: 200.0, class: 'skin-style-shrek' },
        { id: 'egg', name: '이스터 에그', stat: '전체 x20', cost: 0, gpsB: 20.0, cpcB: 20.0, class: 'skin-style-egg', isSecret: true },
        { id: 'luckybox', name: '럭키박스', stat: 'x1~x1850 랜덤', cost: 0, gpsB: 1.0, cpcB: 1.0, class: 'skin-style-luckybox', isSecret: true, isRandom: true },
        { id: 'smile', name: '스마일 코어', stat: '전체 x125', cost: 0, gpsB: 125.0, cpcB: 125.0, class: 'skin-style-smile', isSecret: true }
    ];

    const items = [];
    for (let i = 1; i <= TOTAL_TIERS; i++) {
        let cost = 10 * Math.pow(2.7, i - 1);
        let gpsVal = 0.1 * Math.pow(2.5, i - 1);
        let cpcVal = 1 * Math.pow(2.4, i - 1);
        
        let reqRebirth = 0;
        if (i > 5) reqRebirth = Math.floor((i - 5) / 1.3) + 1;

        items.push({
            id: `tier${i}`,
            name: `티어 ${i}`,
            baseCost: cost,
            gps: gpsVal,
            cpc: cpcVal,
            count: 0,
            requiredRebirth: reqRebirth
        });
    }

    function getRandomLuckyMult() { return 1 + Math.random() * 1849; }
    function getRebirthCost() { return 50000 * Math.pow(5, game.rebirths); }
    function getEventUpgradeCost() { return 5000 * Math.pow(2.8, game.eventLevel); }
    function getEventMultiplier() { return (2 + game.eventLevel * 0.5) * eventTypes[currentEventType].mult; }
    function getEventDuration() { return 45 + game.eventLevel * 2; }

    const balanceDisplay = document.getElementById('balanceDisplay');
    const gpsDisplay = document.getElementById('gpsDisplay');
    const dpcDisplay = document.getElementById('dpcDisplay');
    const rebirthDisplay = document.getElementById('rebirthDisplay');
    const bonusDisplay = document.getElementById('bonusDisplay');
    const clickBtn = document.getElementById('clickBtn');
    const clickSection = document.getElementById('clickSection');
    const shopContainer = document.getElementById('shopContainer');
    const rebirthContainer = document.getElementById('rebirthContainer');
    const eventUpgradeContainer = document.getElementById('eventUpgradeContainer');
    const skinGrid = document.getElementById('skinGrid');
    const eventBar = document.getElementById('eventBar');

    function checkSkinUnlocks() {
        let unlockedAny = false;
        if (game.eventLevel >= 100 && !game.ownedSkins.includes('luckybox')) {
            game.ownedSkins.push('luckybox');
            unlockedAny = true;
        }
        if (game.rebirths >= 25 && !game.ownedSkins.includes('smile')) {
            game.ownedSkins.push('smile');
            unlockedAny = true;
        }
        if (unlockedAny) {
            initSkins();
        }
    }

    function getCost(index) {
        const item = items[index];
        let currentCost = item.baseCost * Math.pow(1.18, item.count);
        if (index > 0 && items[index - 1].count >= MAX_LEVEL) {
            currentCost *= 0.7;
        }
        return currentCost;
    }

    function formatNum(num) {
        if (num < 1) return Math.floor(num).toString();
        const units = ["", "만", "억", "조", "경", "해", "자", "양", "구", "간", "정", "재", "극", "항하사", "아승기", "나유타", "불가사의", "무량대수"];
        let exp = Math.floor(Math.log10(num));
        let unitIdx = Math.floor(exp / 4);
        if (unitIdx === 0) return Math.floor(num).toLocaleString();
        if (unitIdx >= units.length) return num.toExponential(2);
        let value = num / Math.pow(10, unitIdx * 4);
        return (Math.floor(value * 100) / 100).toLocaleString() + units[unitIdx];
    }

    let holdTimer = null;
    let holdInterval = null;
    let isScrolling = false;

    function initShop() {
        shopContainer.innerHTML = '';
        rebirthContainer.innerHTML = '';
        eventUpgradeContainer.innerHTML = '';
        
        const rebirthEl = document.createElement('div');
        rebirthEl.className = 'shop-item rebirth-item';
        rebirthEl.id = 'rebirth-btn';
        rebirthEl.onclick = triggerRebirth;
        rebirthEl.innerHTML = `
            <div class="item-info">
                <div class="item-name">환생 프로토콜 진입</div>
                <div class="item-details">레벨 리셋, 전체 기본 증폭량 +100% 누적 (25회 시 스마일 스킨)</div>
                <div class="item-cost" id="rebirth-cost">-</div>
            </div>
            <div class="item-level" id="rebirth-count">0 회</div>
        `;
        rebirthContainer.appendChild(rebirthEl);

        const eventUpEl = document.createElement('div');
        eventUpEl.className = 'shop-item event-upgrade-item';
        eventUpEl.id = 'event-upgrade-btn';

        const startEventUp = (e) => {
            e.preventDefault();
            buyEventUpgrade();
            holdTimer = setTimeout(() => { holdInterval = setInterval(() => buyEventUpgrade(), 60); }, 300);
        };
        const stopEventUp = () => { clearTimeout(holdTimer); clearInterval(holdInterval); };

        eventUpEl.addEventListener('mousedown', (e) => { if (e.button === 0) startEventUp(e); });
        eventUpEl.addEventListener('mouseup', stopEventUp);
        eventUpEl.addEventListener('mouseleave', stopEventUp);
        eventUpEl.addEventListener('touchstart', () => {
            isScrolling = false;
            holdTimer = setTimeout(() => { if (!isScrolling) holdInterval = setInterval(() => buyEventUpgrade(), 60); }, 300);
        }, { passive: true });
        eventUpEl.addEventListener('touchmove', () => { isScrolling = true; stopEventUp(); }, { passive: true });
        eventUpEl.addEventListener('touchend', () => { stopEventUp(); if (!isScrolling) buyEventUpgrade(); });

        eventUpEl.innerHTML = `
            <div class="item-info">
                <div class="item-name">이벤트 효율 극대화</div>
                <div class="item-details" id="event-upgrade-details">지속시간 및 배율 강화 (100렙 시 럭키박스 스킨)</div>
                <div class="item-cost" id="event-upgrade-cost">-</div>
            </div>
            <div class="item-level" id="event-upgrade-count">0 / ${MAX_LEVEL}</div>
        `;
        eventUpgradeContainer.appendChild(eventUpEl);

        items.forEach((item, index) => {
            const itemEl = document.createElement('div');
            itemEl.className = 'shop-item';
            itemEl.id = `item-${item.id}`;
            
            const startAction = (e) => {
                e.preventDefault();
                buyItem(index);
                holdTimer = setTimeout(() => { holdInterval = setInterval(() => buyItem(index), 60); }, 300);
            };
            const stopAction = () => { clearTimeout(holdTimer); clearInterval(holdInterval); };

            itemEl.addEventListener('mousedown', (e) => { if (e.button === 0) startAction(e); });
            itemEl.addEventListener('mouseup', stopAction);
            itemEl.addEventListener('mouseleave', stopAction);
            itemEl.addEventListener('touchstart', () => {
                isScrolling = false;
                holdTimer = setTimeout(() => { if (!isScrolling) holdInterval = setInterval(() => buyItem(index), 60); }, 300);
            }, { passive: true });
            itemEl.addEventListener('touchmove', () => { isScrolling = true; stopAction(); }, { passive: true });
            itemEl.addEventListener('touchend', () => { stopAction(); if (!isScrolling) buyItem(index); });

            itemEl.innerHTML = `
                <div class="item-info">
                    <div class="item-name" id="name-${item.id}">${item.name} <span id="badge-container-${item.id}"></span></div>
                    <div class="item-details" id="details-${item.id}">초당 +${formatNum(item.gps)} / 클릭 +${formatNum(item.cpc)}</div>
                    <div class="item-cost" id="cost-${item.id}">-</div>
                </div>
                <div class="item-level" id="count-${item.id}">0 / ${MAX_LEVEL}</div>
            `;
            shopContainer.appendChild(itemEl);
        });

        const eggEl = document.createElement('div');
        eggEl.className = 'shop-item secret-egg-item';
        eggEl.id = 'secret-egg-btn';
        eggEl.onclick = clickSecretEgg;
        eggEl.innerHTML = `
            <div class="item-info">
                <div class="item-name">비밀 달걀 프로토콜</div>
                <div class="item-details">1000번 터치하여 히든 스킨 해금</div>
                <div class="item-cost" style="color:#d9480f;">터치 시 카운트 증가</div>
            </div>
            <div class="item-level" id="egg-click-count">0 / 1000</div>
        `;
        shopContainer.appendChild(eggEl);
    }

    function clickSecretEgg() {
        if (game.ownedSkins.includes('egg')) return;
        game.eggClicks++;
        if (game.eggClicks >= 1000) {
            game.ownedSkins.push('egg');
            game.currentSkin = 'egg';
            recalculateStats();
            initSkins();
        }
        updateUI();
        saveGame();
    }

    function initSkins() {
        skinGrid.innerHTML = '';
        skins.forEach(skin => {
            if (skin.isSecret && !game.ownedSkins.includes(skin.id)) return;

            const card = document.createElement('div');
            card.className = `skin-card ${game.currentSkin === skin.id ? 'active' : ''}`;
            card.id = `skin-${skin.id}`;
            card.onclick = () => selectSkin(skin.id);
            
            let priceText = game.ownedSkins.includes(skin.id) ? "보유 중" : `${formatNum(skin.cost)}`;
            card.innerHTML = `
                <strong>${skin.name}</strong>
                <span class="skin-stat-tag">${skin.stat}</span>
                <span style="color:var(--text-muted); font-size:10px;">${priceText}</span>
            `;
            skinGrid.appendChild(card);
        });
        
        const activeSkinObj = skins.find(s => s.id === game.currentSkin) || skins[0];
        clickBtn.className = `click-btn ${activeSkinObj.class}`;

        // 스킨 그래픽 연출 (SVG 라인 드로잉 사용)
        if (game.currentSkin === 'smile') {
            clickBtn.innerHTML = `
                <svg id="smileSvg" width="120" height="120" viewBox="0 0 100 100">
                    <circle cx="35" cy="38" r="7" fill="#212529" />
                    <circle cx="65" cy="38" r="7" fill="#212529" />
                    <!-- 평소에는 우울한 입 모양 (아래쪽 굴곡 ∩) -->
                    <path id="smileMouth" d="M 30 72 Q 50 52 70 72" stroke="#212529" stroke-width="7" stroke-linecap="round" fill="none" />
                </svg>
            `;
        } else if (game.currentSkin === 'luckybox') {
            clickBtn.innerHTML = ''; 
        } else {
            clickBtn.textContent = '＋';
        }
    }

    function selectSkin(skinId) {
        const skin = skins.find(s => s.id === skinId);
        if (game.ownedSkins.includes(skinId)) {
            game.currentSkin = skinId;
        } else {
            if (game.balance >= skin.cost) {
                game.balance -= skin.cost;
                game.ownedSkins.push(skinId);
                game.currentSkin = skinId;
            } else {
                return;
            }
        }
        recalculateStats();
        initSkins();
        updateUI();
        saveGame();
    }

    function updateUI() {
        balanceDisplay.textContent = formatNum(game.balance);
        gpsDisplay.textContent = game.currentSkin === 'luckybox' ? "랜덤 (1~1850배)" : formatNum(game.totalGps);
        dpcDisplay.textContent = game.currentSkin === 'luckybox' ? "랜덤 (1~1850배)" : formatNum(game.clickPower);
        rebirthDisplay.textContent = game.rebirths;
        bonusDisplay.textContent = game.rebirths * 100;

        const eggCountEl = document.getElementById('egg-click-count');
        const eggBtn = document.getElementById('secret-egg-btn');
        if (eggCountEl && eggBtn) {
            if (game.ownedSkins.includes('egg')) {
                eggCountEl.textContent = "해금 완료";
                eggBtn.className = 'shop-item maxed';
            } else {
                eggCountEl.textContent = `${game.eggClicks} / 1000`;
            }
        }

        const eventUpBtn = document.getElementById('event-upgrade-btn');
        const eventUpCostEl = document.getElementById('event-upgrade-cost');
        const eventUpCountEl = document.getElementById('event-upgrade-count');
        const eventUpDetailsEl = document.getElementById('event-upgrade-details');
        
        if (eventUpBtn) {
            eventUpDetailsEl.textContent = `지속시간: ${getEventDuration()}초 / 이벤트 효과 배율 지속 증가`;
            if (game.eventLevel >= MAX_LEVEL) {
                eventUpBtn.className = 'shop-item event-upgrade-item maxed';
                eventUpCostEl.textContent = 'MAX LEVEL';
                eventUpCountEl.textContent = `${MAX_LEVEL} / ${MAX_LEVEL}`;
            } else {
                eventUpBtn.className = 'shop-item event-upgrade-item';
                const evCost = getEventUpgradeCost();
                eventUpCostEl.textContent = `${formatNum(evCost)}`;
                eventUpCountEl.textContent = `${game.eventLevel} / ${MAX_LEVEL}`;
                if (game.balance >= evCost) eventUpBtn.classList.remove('disabled');
                else eventUpBtn.classList.add('disabled');
            }
        }

        items.forEach((item, index) => {
            const itemEl = document.getElementById(`item-${item.id}`);
            if (!itemEl) return;
            const costEl = document.getElementById(`cost-${item.id}`);
            const countEl = document.getElementById(`count-${item.id}`);
            const badgeContainer = document.getElementById(`badge-container-${item.id}`);
            
            if (game.rebirths < item.requiredRebirth) {
                itemEl.className = 'shop-item lock-item';
                costEl.textContent = `환생 ${item.requiredRebirth}회 필요`;
                countEl.textContent = `잠김`;
                badgeContainer.innerHTML = '';
                return;
            }

            const currentCost = getCost(index);
            let badgesHtml = '';
            if (index > 0 && items[index - 1].count >= MAX_LEVEL) {
                badgesHtml += `<span class="discount-badge">30% 할인</span>`;
            }

            if (item.count >= MAX_LEVEL) {
                itemEl.className = 'shop-item maxed';
                costEl.textContent = 'MAX LEVEL';
                countEl.textContent = `${MAX_LEVEL} / ${MAX_LEVEL}`;
                badgesHtml += `<span class="synergy-badge">2배 보너스</span>`;
            } else {
                itemEl.className = 'shop-item';
                countEl.textContent = `${item.count} / ${MAX_LEVEL}`;
                costEl.textContent = `${formatNum(currentCost)}`;

                if (game.balance >= currentCost) itemEl.classList.remove('disabled');
                else itemEl.classList.add('disabled');
            }
            badgeContainer.innerHTML = badgesHtml;
        });

        const rBtn = document.getElementById('rebirth-btn');
        const rCostEl = document.getElementById('rebirth-cost');
        const rCountEl = document.getElementById('rebirth-count');
        if (rBtn) {
            const rCost = getRebirthCost();
            rCostEl.textContent = `${formatNum(rCost)}`;
            rCountEl.textContent = `${game.rebirths} 회`;
            if (game.balance >= rCost) rBtn.classList.remove('disabled');
            else rBtn.classList.add('disabled');
        }
    }

    // 스마일 코어 누를 때 입 모양 전환 애니메이션 연출 (∩ -> ∪)
    clickBtn.addEventListener('mousedown', (e) => {
        let actualClickPower = game.clickPower;

        if (game.currentSkin === 'smile') {
            const mouth = document.getElementById('smileMouth');
            if (mouth) mouth.setAttribute('d', 'M 30 58 Q 50 78 70 58'); // 웃는 입 모양 (∪)
        }

        if (game.currentSkin === 'luckybox') {
            const randMult = getRandomLuckyMult();
            actualClickPower = game.clickPower * randMult;
        }

        if (isEventActive) actualClickPower *= getEventMultiplier();
        game.balance += actualClickPower;
        createFloatingText(e.clientX, e.clientY, `+${formatNum(actualClickPower)}`);
        updateUI();
    });

    // 떼었을 때 다시 우울한 입으로 복구 (∪ -> ∩)
    const resetMouth = () => {
        if (game.currentSkin === 'smile') {
            const mouth = document.getElementById('smileMouth');
            if (mouth) mouth.setAttribute('d', 'M 30 72 Q 50 52 70 72');
        }
    };
    clickBtn.addEventListener('mouseup', resetMouth);
    clickBtn.addEventListener('mouseleave', resetMouth);

    function createFloatingText(x, y, text) {
        const rect = clickSection.getBoundingClientRect();
        const relativeX = x - rect.left;
        const relativeY = y - rect.top;

        const textEl = document.createElement('div');
        textEl.className = 'floating-text';
        textEl.style.left = `${relativeX}px`;
        textEl.style.top = `${relativeY}px`;
        textEl.textContent = text;
        if(isEventActive) textEl.style.color = 'var(--event-color)';

        clickSection.appendChild(textEl);
        setTimeout(() => textEl.remove(), 600);
    }

    function buyItem(index) {
        const item = items[index];
        if (game.rebirths < item.requiredRebirth) return;

        const currentCost = getCost(index);
        if (item.count < MAX_LEVEL && game.balance >= currentCost) {
            game.balance -= currentCost;
            item.count++;
            recalculateStats();
            updateUI();
            saveGame();
        }
    }

    function buyEventUpgrade() {
        if (game.eventLevel >= MAX_LEVEL) return;
        const currentCost = getEventUpgradeCost();
        if (game.balance >= currentCost) {
            game.balance -= currentCost;
            game.eventLevel++;
            checkSkinUnlocks();
            updateUI();
            saveGame();
        }
    }

    function recalculateStats() {
        const rebirthMult = 1 + game.rebirths;
        const activeSkin = skins.find(s => s.id === game.currentSkin) || skins[0];

        let baseGps = 0;
        let baseCpc = 0;

        items.forEach((item) => {
            let itemGps = item.count * item.gps;
            let itemCpc = item.count * item.cpc;
            if (item.count >= MAX_LEVEL) {
                itemGps *= 2;
                itemCpc *= 2;
            }
            baseGps += itemGps;
            baseCpc += itemCpc;
        });

        game.totalGps = baseGps * rebirthMult * activeSkin.gpsB;
        game.clickPower = (1 + baseCpc) * rebirthMult * activeSkin.cpcB;
    }

    function triggerRebirth() {
        const rCost = getRebirthCost();
        if (game.balance >= rCost) {
            if (confirm("환생하시겠습니까? 이벤트 상태도 초기화됩니다.")) {
                game.rebirths++;
                game.balance = 0;
                game.eventLevel = 0;
                eventTimer = 180;
                eventActiveTime = 0;
                isEventActive = false;
                items.forEach(item => item.count = 0);
                checkSkinUnlocks();
                recalculateStats();
                saveGame();
                updateUI();
            }
        }
    }

    function handleEventSystemDT(dt) {
        if (isEventActive) {
            eventActiveTime -= dt;
            eventBar.className = "event-status-box event-active";
            let evInfo = eventTypes[currentEventType];
            eventBar.textContent = `${evInfo.name} 발동 중! [${evInfo.desc} & ${getEventMultiplier().toFixed(1)}배] ${Math.ceil(eventActiveTime)}초 남음`;
            if (eventActiveTime <= 0) {
                isEventActive = false;
                eventTimer = 180;
                eventActiveTime = 0;
            }
        } else {
            eventTimer -= dt;
            eventBar.className = "event-status-box";
            let displayTimer = Math.max(0, eventTimer);
            let min = Math.floor(displayTimer / 60);
            let sec = Math.floor(displayTimer % 60);
            eventBar.textContent = `다음 프로토콜까지: ${min}분 ${sec}초 대기 중`;
            if (eventTimer <= 0) {
                isEventActive = true;
                currentEventType = Math.floor(Math.random() * eventTypes.length);
                eventActiveTime = getEventDuration();
                eventTimer = 0;
            }
        }
    }

    function saveGame() {
        const saveData = {
            balance: game.balance,
            rebirths: game.rebirths,
            eventLevel: game.eventLevel,
            currentSkin: game.currentSkin,
            ownedSkins: game.ownedSkins,
            eggClicks: game.eggClicks,
            counts: items.map(item => item.count),
            eventTimer: eventTimer,
            eventActiveTime: eventActiveTime,
            isEventActive: isEventActive,
            currentEventType: currentEventType,
            lastSavedAt: Date.now()
        };
        localStorage.setItem(SAVE_KEY, JSON.stringify(saveData));
    }

    function loadGame() {
        const saved = localStorage.getItem(SAVE_KEY);
        if (saved) {
            try {
                const data = JSON.parse(saved);
                game.balance = data.balance || 0;
                game.rebirths = data.rebirths || 0;
                game.eventLevel = data.eventLevel || 0;
                game.currentSkin = data.currentSkin || 'default';
                game.ownedSkins = data.ownedSkins || ['default'];
                game.eggClicks = data.eggClicks || 0;
                if (data.counts && Array.isArray(data.counts)) {
                    items.forEach((item, idx) => {
                        if (data.counts[idx] !== undefined) {
                            item.count = Math.min(data.counts[idx], MAX_LEVEL);
                        }
                    });
                }
                if (data.eventTimer !== undefined) eventTimer = data.eventTimer;
                if (data.eventActiveTime !== undefined) eventActiveTime = data.eventActiveTime;
                if (data.isEventActive !== undefined) isEventActive = data.isEventActive;
                if (data.currentEventType !== undefined) currentEventType = data.currentEventType;

                checkSkinUnlocks();
                recalculateStats();
            } catch (e) {
                console.error("저장 데이터 로드 실패", e);
            }
        }
        lastTickTime = Date.now();
    }

    window.addEventListener('beforeunload', saveGame);
    window.addEventListener('pagehide', saveGame);

    setInterval(() => {
        let now = Date.now();
        let dt = (now - lastTickTime) / 1000;
        lastTickTime = now;

        if (dt > 0) {
            let currentGps = game.totalGps;
            if (game.currentSkin === 'luckybox') {
                currentGps = game.totalGps * getRandomLuckyMult();
            }
            
            if (currentGps > 0) game.balance += currentGps * dt;
            if (isEventActive) {
                let actualClickPower = game.clickPower * getEventMultiplier();
                if (game.currentSkin === 'luckybox') actualClickPower *= getRandomLuckyMult();
                game.balance += actualClickPower * dt;
            }
            handleEventSystemDT(dt);
        }
        updateUI();
    }, 100);

    setInterval(saveGame, 3000);

    initShop();
    loadGame();
    initSkins();
    updateUI();
</script>

```

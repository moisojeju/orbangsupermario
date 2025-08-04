<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>슈퍼 오르방 - 플랫폼 어드벤처</title>
    <link rel="stylesheet" href="mario-orbang.css">
</head>
<body>
    <div class="game-container">
        <div class="header">
            <div class="game-title">
                <h1>🍄 슈퍼 오르방 🍄</h1>
                <div class="subtitle">Super Orbang Platform Adventure</div>
            </div>
            <div class="game-stats">
                <div class="stat-group">
                    <div class="stat-item">
                        <span class="stat-label">점수</span>
                        <span id="score" class="stat-value">000000</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-label">코인</span>
                        <span id="coins" class="stat-value">×00</span>
                    </div>
                </div>
                <div class="stat-group">
                    <div class="stat-item">
                        <span class="stat-label">생명</span>
                        <span id="lives" class="stat-value">×03</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-label">시간</span>
                        <span id="time" class="stat-value">400</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="game-world">
            <canvas id="gameCanvas" width="1000" height="600"></canvas>
            <div id="character-intro" class="character-intro">
                <div class="intro-content">
                    <h2>오르방이 모험을 떠납니다!</h2>
                    <div class="character-showcase">
                        <div class="orbang-display"></div>
                        <div class="character-info">
                            <h3>ORBANG</h3>
                            <p>용감한 건설 영웅</p>
                            <div class="abilities">
                                <div class="ability">🏃‍♂️ 빠른 이동</div>
                                <div class="ability">🦘 높은 점프</div>
                                <div class="ability">💪 강력한 파워</div>
                            </div>
                        </div>
                    </div>
                    <div class="difficulty-select">
                        <h3>난이도 선택</h3>
                        <div class="difficulty-options">
                            <div class="difficulty-option selected" data-difficulty="easy">
                                <span class="difficulty-icon">😊</span>
                                <span>EASY</span>
                            </div>
                            <div class="difficulty-option" data-difficulty="normal">
                                <span class="difficulty-icon">😐</span>
                                <span>NORMAL</span>
                            </div>
                            <div class="difficulty-option" data-difficulty="hard">
                                <span class="difficulty-icon">😤</span>
                                <span>HARD</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="controls">
            <button id="startBtn" class="btn-start">게임 시작</button>
            <button id="pauseBtn" class="btn-pause" disabled>일시정지</button>
            <button id="restartBtn" class="btn-restart">재시작</button>
        </div>

        <div class="instructions">
            <div class="instruction-section">
                <h3>🎮 게임 조작법</h3>
                <div class="controls-grid">
                    <div class="control-item">
                        <span class="key">A 또는 ←</span>
                        <span class="action">왼쪽 이동</span>
                    </div>
                    <div class="control-item">
                        <span class="key">D 또는 →</span>
                        <span class="action">오른쪽 이동</span>
                    </div>
                    <div class="control-item">
                        <span class="key">W 또는 ↑</span>
                        <span class="action">점프</span>
                    </div>
                    <div class="control-item">
                        <span class="key">스페이스</span>
                        <span class="action">달리기/파워업</span>
                    </div>
                </div>
            </div>
            <div class="instruction-section">
                <h3>🎯 오르방의 미션</h3>
                <ul class="objectives">
                    <li>🪙 건설 자재(코인)을 수집하세요</li>
                    <li>🍄 파워 툴로 오르방을 강화하세요</li>
                    <li>🤖 작업을 방해하는 로봇들을 처치하세요</li>
                    <li>🚧 건설 현장의 모든 구역을 완성하세요</li>
                    <li>🏁 안전하게 목표 지점에 도달하세요</li>
                    <li>⭐ 숨겨진 보너스 아이템을 찾아보세요</li>
                </ul>
            </div>
        </div>

        <div id="gameOverScreen" class="game-over-screen hidden">
            <div class="game-over-content">
                <h2 id="gameOverTitle">🎮 작업 완료! 🎮</h2>
                <div class="final-stats">
                    <p>최종 점수: <span id="finalScore">0</span></p>
                    <p>수집한 자재: <span id="finalCoins">0</span></p>
                    <p>완성한 구역: <span id="finalLevel">1-1</span></p>
                    <p>작업 시간: <span id="finalTime">0:00</span></p>
                </div>
                <div class="performance-rating">
                    <div id="rating" class="rating">⭐⭐⭐</div>
                    <div id="ratingText" class="rating-text">훌륭한 작업입니다!</div>
                </div>
                <div class="game-over-buttons">
                    <button id="playAgainBtn" class="btn-start">다시 작업하기</button>
                    <button id="newGameBtn" class="btn-pause">새 프로젝트</button>
                </div>
            </div>
        </div>
    </div>

    <script src="mario-orbang.js"></script>
</body>
</html>

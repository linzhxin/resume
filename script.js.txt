// Interactive sample game code (HTML5 Canvas - Click to Score)
let score = 0;
const canvas = document.getElementById('gameCanvas');
if (canvas) {
    const ctx = canvas.getContext('2d');
    function drawScore() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        ctx.font = '20px Arial';
        ctx.fillText('Score: ' + score, 10, 30);
    }
    canvas.addEventListener('click', () => {
        score++;
        drawScore();
    });
    drawScore();
}
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<title>AI Vẽ Hình - Demo Toán Lớp 5</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
    body{
        font-family: Arial, sans-serif;
        background:#f4f7fb;
        margin:0; padding:0;
        color:#222;

        display:flex;
        justify-content:center;
        align-items:center;
        min-height:100vh;
    }
    h1{color:#234b8a; margin-bottom:10px; text-align:center;}

    .box{
        background:#fff; padding:16px; border-radius:12px;
        box-shadow:0 4px 14px rgba(0,0,0,0.08);
        max-width:650px; width:90%;
    }
    input{
        width:100%; padding:10px; margin:10px 0;
        border-radius:8px; border:1px solid #ccc;
    }
    button{
        background:#234b8a; color:white; padding:10px 18px;
        border:none; border-radius:8px; cursor:pointer;
    }
    canvas{
        border:1px solid #ddd; background:white;
        margin-top:16px; width:100%; height:380px;
    }
</style>
</head>
<body>
<div class="box">
    <h1>🧠 AI VẼ HÌNH – TOÁN LỚP 5</h1>
    <label><strong>Nhập yêu cầu vẽ hình:</strong></label>
    <input id="cmd" placeholder="Ví dụ: vẽ hình vuông cạnh 20 cm" />
    <button onclick="run()">Vẽ hình</button>
    <button style="background:#666; margin-left:8px;" onclick="clearCanvas()">Xóa</button>
    <canvas id="board"></canvas>
</div>

<script>
const canvas = document.getElementById("board");
const ctx = canvas.getContext("2d");

function fitCanvas(){
    const rect = canvas.getBoundingClientRect();
    canvas.width = rect.width;
    canvas.height = rect.height;
}
fitCanvas();
window.onresize = fitCanvas;

function clearCanvas(){
    ctx.clearRect(0, 0, canvas.width, canvas.height);
}

/* Chuyển cm sang px, có giới hạn max kích thước */
function cmToPx(cm){
    const pxPerCm = 37.8; // 1cm ≈ 37.8px
    let px = cm * pxPerCm;
    const maxPx = 250;  // Giới hạn kích thước tối đa để vẽ vừa canvas
    if(px > maxPx){
        const scale = maxPx / px;
        px = px * scale;
    }
    return px;
}

/* Vẽ chữ */
function drawText(txt, x, y){
    ctx.font = "14px Arial";
    ctx.fillStyle = "red";
    ctx.fillText(txt, x, y);
}

function run(){
    clearCanvas();
    const text = document.getElementById("cmd").value.toLowerCase().trim();
    if(!text) return;

    /* HÌNH VUÔNG */
    if(text.includes("hình vuông")){
        const m = text.match(/\d+/);
        const cm = m ? +m[0] : 10;
        const a = cmToPx(cm);

        ctx.strokeRect(50, 50, a, a);

        // Nhãn ở trung điểm các cạnh, điều chỉnh khoảng cách trái/phải
        drawText(cm + " cm", 50 + a/2 - 10, 50 - 5);      // cạnh trên
        drawText(cm + " cm", 50 + a + 10, 50 + a/2);     // cạnh phải (đưa vào gần cạnh hơn)
        drawText(cm + " cm", 50 + a/2 - 10, 50 + a + 15); // cạnh dưới
        drawText(cm + " cm", 50 - 50, 50 + a/2);          // cạnh trái (đưa ra xa cạnh hơn)

        return;
    }

    /* HÌNH CHỮ NHẬT */
    if(text.includes("hình chữ nhật")){
        const nums = text.match(/\d+/g);
        let wcm = 10, hcm = 5;
        if(nums?.length >= 2){
            wcm = +nums[0];
            hcm = +nums[1];
        }

        const w = cmToPx(wcm);
        const h = cmToPx(hcm);

        ctx.strokeRect(50, 50, w, h);

        drawText(wcm + " cm", 50 + w/2 - 10, 50 - 5);    // cạnh trên
        drawText(wcm + " cm", 50 + w/2 - 10, 50 + h + 15); // cạnh dưới
        drawText(hcm + " cm", 50 - 50, 50 + h/2);        // cạnh trái (đưa ra xa cạnh hơn)
        drawText(hcm + " cm", 50 + w + 10, 50 + h/2);    // cạnh phải (đưa vào gần cạnh hơn)

        return;
    }

    /* TAM GIÁC ĐỀU */
    if(text.includes("tam giác đều")){
        const m = text.match(/\d+/);
        const cm = m ? +m[0] : 10;
        const a = cmToPx(cm);

        const x = canvas.width/2;
        const y = 100;
        const h = a * Math.sqrt(3) / 2;

        const Ax = x, Ay = y;
        const Bx = x - a/2, By = y + h;
        const Cx = x + a/2, Cy = y + h;

        ctx.beginPath();
        ctx.moveTo(Ax, Ay);
        ctx.lineTo(Bx, By);
        ctx.lineTo(Cx, Cy);
        ctx.closePath();
        ctx.stroke();

        // Nhãn trung điểm các cạnh
        drawText(cm + " cm", (Ax + Bx)/2 - 10, (Ay + By)/2); // AB
        drawText(cm + " cm", (Bx + Cx)/2 - 10, (By + Cy)/2 + 5); // BC
        drawText(cm + " cm", (Cx + Ax)/2 + 5, (Cy + Ay)/2 - 5); // CA

        return;
    }

    /* TAM GIÁC THƯỜNG (3 cạnh) */
    if(text.includes("tam giác")){
        const nums = text.match(/\d+/g);

        if(nums && nums.length === 3){
            const acm = +nums[0];
            const bcm = +nums[1];
            const ccm = +nums[2];

            const a = cmToPx(acm);
            const b = cmToPx(bcm);
            const c = cmToPx(ccm);

            const Ax = 80, Ay = 300;
            const Bx = Ax + c, By = Ay;

            const cosA = (b*b + c*c - a*a) / (2 * b * c);
            const h = Math.sqrt(Math.max(0, b*b - (c*cosA)**2));

            const Cx = Ax + c*cosA;
            const Cy = Ay - h;

            ctx.beginPath();
            ctx.moveTo(Ax, Ay);
            ctx.lineTo(Bx, By);
            ctx.lineTo(Cx, Cy);
            ctx.closePath();
            ctx.stroke();

            // Nhãn trung điểm các cạnh
            drawText(ccm + " cm", (Ax + Bx)/2 - 10, (Ay + By)/2 + 5); 
            drawText(acm + " cm", (Bx + Cx)/2, (By + Cy)/2 - 5);     
            drawText(bcm + " cm", (Cx + Ax)/2 - 10, (Cy + Ay)/2 - 5); 

            return;
        }
    }

    alert("⚠️ Không hiểu yêu cầu. VD: 'hình vuông 10 cm', 'chữ nhật 20 10 cm', 'tam giác đều 12 cm', 'tam giác 100 120 130'");
}
</script>
</body>
</html>

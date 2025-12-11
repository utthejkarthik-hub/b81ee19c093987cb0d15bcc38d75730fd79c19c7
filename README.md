<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vitamin Deficiency Food Suggestion</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
    body {
        margin: 0;
        font-family: 'Poppins', sans-serif;
        background: linear-gradient(135deg, #1c1f26, #2e323d);
        color: #fff;
    }

    .container {
        max-width: 650px;
        margin: 80px auto;
        background: rgba(255, 255, 255, 0.06);
        padding: 40px;
        border-radius: 18px;
        box-shadow: 0 0 25px rgba(0,0,0,0.4);
        backdrop-filter: blur(10px);
    }

    h1 {
        text-align: center;
        font-size: 28px;
        font-weight: 600;
        letter-spacing: 1px;
        color: #ffcc66;
    }

    label {
        font-size: 16px;
        display: block;
        margin-bottom: 10px;
        margin-top: 25px;
    }

    select {
        width: 100%;
        padding: 12px;
        border-radius: 10px;
        border: none;
        font-size: 16px;
        background: #2c3038;
        color: white;
    }

    button {
        width: 100%;
        margin-top: 25px;
        padding: 14px;
        font-size: 18px;
        border: none;
        border-radius: 10px;
        background: #ffcc66;
        color: #1a1a1a;
        font-weight: 600;
        cursor: pointer;
        transition: 0.3s;
    }
    button:hover {
        background: #ffb833;
        transform: scale(1.02);
    }

    .result-box {
        margin-top: 30px;
        padding: 20px;
        border-radius: 12px;
        background: rgba(255, 255, 255, 0.08);
        box-shadow: 0 0 15px rgba(0,0,0,0.2);
    }

    .foods {
        color: #ffdd99;
        font-size: 18px;
        margin-top: 8px;
    }
</style>
</head>

<body>

<div class="container">
    <h1>Vitamin Deficiency Food Suggestion</h1>

    <label>Select Vitamin Deficiency:</label>
    <select id="vitamin">
        <option value="">-- Select --</option>
        <option value="A">Vitamin A</option>
        <option value="B12">Vitamin B12</option>
        <option value="C">Vitamin C</option>
        <option value="D">Vitamin D</option>
        <option value="E">Vitamin E</option>
        <option value="K">Vitamin K</option>
    </select>

    <button onclick="showFood()">Suggest Food</button>

    <div id="result" class="result-box" style="display:none;">
        <h2 id="title"></h2>
        <p class="foods" id="foods"></p>
    </div>

</div>

<script>
    const vitaminFoods = {
        "A": "Carrots, Sweet Potatoes, Spinach, Mango, Eggs",
        "B12": "Milk, Cheese, Fish, Chicken, Eggs",
        "C": "Oranges, Lemon, Guava, Strawberries, Broccoli",
        "D": "Sunlight, Dairy Products, Eggs, Fish, Fortified Milk",
        "E": "Almonds, Sunflower Seeds, Avocado, Olive Oil",
        "K": "Green Leafy Vegetables, Kale, Broccoli, Spinach"
    };

    function showFood() {
        let v = document.getElementById('vitamin').value;

        if (v === "") {
            alert("Please select a vitamin deficiency!");
            return;
        }

        document.getElementById('title').innerText = "Best Foods for Vitamin " + v;
        document.getElementById('foods').innerText = vitaminFoods[v];
        document.getElementById('result').style.display = "block";
    }
</script>

</body>
</html>

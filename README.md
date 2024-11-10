<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notes & Practical Skills</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Unlock Your Success with Quality Notes & Practicals</h1>
        <p>Providing you with resources to excel in your studies and skills.</p>
        <a href="packages.html" class="btn-red">Get Started</a>
    </header>
    
    <section id="highlights">
        <div class="card">
            <h2>Notes</h2>
            <p>Detailed notes on various topics to enhance your understanding.</p>
        </div>
        <div class="card">
            <h2>Past Papers</h2>
            <p>Practice with past papers to boost your confidence.</p>
        </div>
        <div class="card">
            <h2>Practical Skills</h2>
            <p>Hands-on practical skills to apply knowledge effectively.</p>
        </div>
    </section>

    <section id="how-it-works">
        <h2>How It Works</h2>
        <ol>
            <li>Choose your package</li>
            <li>Pay securely via M-Pesa</li>
            <li>Access your resources instantly</li>
        </ol>
    </section>

    <footer>
        <p>Contact: info@example.com | Phone: 0703486797</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Choose Your Package</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Choose Your Package</h1>
        <p>Select the package that suits your needs.</p>
    </header>

    <section id="packages">
        <div class="package-card">
            <h2>Basic Package</h2>
            <p>Access to Notes</p>
            <p><strong>KES 100</strong></p>
            <button class="btn-orange" onclick="startPayment('Basic')">Subscribe Now</button>
        </div>
        <div class="package-card">
            <h2>Standard Package</h2>
            <p>Access to Notes & Past Papers</p>
            <p><strong>KES 200</strong></p>
            <button class="btn-orange" onclick="startPayment('Standard')">Subscribe Now</button>
        </div>
        <div class="package-card">
            <h2>Premium Package</h2>
            <p>Access to all resources</p>
            <p><strong>KES 300</strong></p>
            <button class="btn-orange" onclick="startPayment('Premium')">Subscribe Now</button>
        </div>
    </section>
</body>
</html>
function startPayment(packageName) {
    let amount;
    switch(packageName) {
        case 'Basic':
            amount = 100;
            break;
        case 'Standard':
            amount = 200;
            break;
        case 'Premium':
            amount = 300;
            break;
    }

    // Simulate M-Pesa PIN prompt
    const pin = prompt(`Enter your M-Pesa PIN to pay KES ${amount} for ${packageName} package:`);
    if(pin) {
        alert(`Payment of KES ${amount} for ${packageName} package successful! Redirecting...`);
        window.location.href = "dashboard.html";  // Redirect to dashboard after payment
    }
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Dashboard</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to Your Dashboard</h1>
    </header>

    <section id="dashboard">
        <div class="dashboard-menu">
            <a href="#" class="btn-blue">My Notes</a>
            <a href="#" class="btn-blue">Past Papers</a>
            <a href="#" class="btn-blue">Practical Skills</a>
        </div>
    </section>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f8fb;
}

header {
    background-color: #007bff;
    color: white;
    text-align: center;
    padding: 2rem 1rem;
}

header h1 {
    margin: 0;
}

.btn-red {
    background-color: #ff4d4d;
    color: white;
    padding: 0.5rem 1rem;
    text-decoration: none;
    border-radius: 5px;
}

#highlights, #packages {
    display: flex;
    gap: 1rem;
    padding: 2rem;
}

.card, .package-card {
    background-color: #fff;
    border: 2px solid #007bff;
    padding: 1rem;
    border-radius: 10px;
    flex: 1;
    text-align: center;
}

.package-card {
    border-color: #ffa500;
}

.btn-orange {
    background-color: #ffa500;
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    cursor: pointer;
    border-radius: 5px;
}

#how-it-works {
    background-color: #e0f7fa;
    padding: 2rem;
    text-align: center;
}

footer {
    background-color: #007bff;
    color: white;
    text-align: center;
    padding: 1rem;
    margin-top: 2rem;
}

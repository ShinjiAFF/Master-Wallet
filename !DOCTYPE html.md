<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>WALLET - Build Your Empire</title>  
  <script src="https://cdn.tailwindcss.com"></script>  
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">  
  <style>  
    body { font-family: system-ui, sans-serif; }  
    .hero-bg {   
      background: linear-gradient(rgba(0,0,0,0.85), rgba(0,0,0,0.9)),   
                  url('https://picsum.photos/id/1015/2000/1200');  
      background-size: cover;  
    }  
  </style>  
</head>  
<body class="bg-zinc-950 text-white">  
  
  <nav class="bg-black/90 fixed w-full z-50">  
    <div class="max-w-6xl mx-auto px-6 py-5 flex justify-between items-center">  
      <div class="text-4xl font-bold text-yellow-400">💰 WALLET</div>  
      <div class="space-x-8">  
        <a href="#how" class="hover:text-yellow-400">How to Play</a>  
        <a href="#wallet" class="hover:text-yellow-400">Wallet</a>  
        <a href="#preorder" class="hover:text-yellow-400">Pre-order</a>  
      </div>  
    </div>  
  </nav>  
  
  <section class="hero-bg h-screen flex items-center justify-center text-center">  
    <div class="max-w-3xl px-6">  
      <h1 class="text-7xl font-black mb-6">BUILD YOUR FINANCIAL EMPIRE</h1>  
      <p class="text-3xl text-yellow-300">Master money. Make deals. Dominate the game.</p>  
    </div>  
  </section>  
  
  <section id="how" class="py-24 bg-zinc-900">  
    <div class="max-w-5xl mx-auto px-6 text-center">  
      <h2 class="text-5xl font-bold mb-12">How to Play</h2>  
      <div class="grid md:grid-cols-4 gap-6">  
        <div class="bg-zinc-800 p-8 rounded-3xl">🎲 Roll & Move</div>  
        <div class="bg-zinc-800 p-8 rounded-3xl">💼 Acquire Assets</div>  
        <div class="bg-zinc-800 p-8 rounded-3xl">🤝 Trade & Negotiate</div>  
        <div class="bg-zinc-800 p-8 rounded-3xl">🏆 Dominate</div>  
      </div>  
    </div>  
  </section>  
  
  <section id="wallet" class="py-24 bg-black">  
    <div class="max-w-4xl mx-auto px-6">  
      <h2 class="text-5xl font-bold text-center mb-8">Live Wallet Demo</h2>  
      <div class="bg-zinc-900 rounded-3xl p-10 text-center">  
        <p class="text-zinc-400">Current Balance</p>  
        <p id="balance" class="text-6xl font-bold text-green-400 my-4">$12,450.75</p>  
        <div class="grid grid-cols-2 gap-6 max-w-xs mx-auto">  
          <button onclick="deposit()" class="bg-green-600 py-6 rounded-2xl font-bold">DEPOSIT</button>  
          <button onclick="withdraw()" class="bg-red-600 py-6 rounded-2xl font-bold">WITHDRAW</button>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <section id="preorder" class="py-24 text-center bg-gradient-to-b from-black to-yellow-900/20">  
    <div class="max-w-md mx-auto">  
      <h2 class="text-5xl font-bold mb-6">$59</h2>  
      <button onclick="alert('Pre-order coming soon!')" class="bg-yellow-400 text-black px-16 py-6 rounded-2xl text-2xl font-bold">  
        PRE-ORDER NOW  
      </button>  
    </div>  
  </section>  
  
  <script>  
    let balance = 12450.75;  
    function update() { document.getElementById('balance').textContent = '$' + balance.toFixed(2); }  
    function deposit() {  
      let amt = prompt("Deposit amount?", "500");  
      if (amt) { balance += Number(amt); update(); }  
    }  
    function withdraw() {  
      let amt = prompt("Withdraw amount?", "200");  
      if (amt && Number(amt) <= balance) { balance -= Number(amt); update(); }  
    }  
    update();  
  </script>  
</body>  
</html>  

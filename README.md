<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gorilla Tag League (GTL) - Competitive Ranked Play</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Rubik:wght@300;400;600;700;900&display=swap');
        
        body {
            font-family: 'Rubik', sans-serif;
            background-color: #0c0f1d;
            color: #e0e0e0;
            min-height: 100vh;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #1a1b2d 0%, #0c0f1d 100%);
        }
        
        .rank-icon {
            width: 80px;
            height: 80px;
            transition: all 0.3s ease;
        }
        
        .rank-icon:hover {
            transform: scale(1.1);
            filter: drop-shadow(0 0 8px rgba(255, 255, 255, 0.3));
        }
        
        .player-card {
            transition: all 0.3s ease;
            background: rgba(20, 22, 40, 0.7);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .player-card:hover {
            background: rgba(30, 33, 60, 0.8);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .progress-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #4f46e5 0%, #7c3aed 100%);
        }
        
        .ape-animation {
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        .glow-text {
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }
    </style>
</head>
<body class="gradient-bg">
    <!-- Header with Logo and Navigation -->
    <header class="py-6 px-4 sm:px-6 lg:px-8 border-b border-gray-800">
        <div class="max-w-7xl mx-auto flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="ape-animation">
                    <img src="C:\Users\mason\Downloads\wa.png" alt="GTL League Official Logo" class="w-12 h-12 rounded-full">
                </div>
                <h1 class="text-2xl font-bold text-white">Gorilla Tag League</h1>
            </div>
            <nav class="hidden md:flex space-x-8">
                <a href="#" class="text-white hover:text-purple-400 transition">Home</a>
                <a href="#rankings" class="text-white hover:text-purple-400 transition">Rankings</a>
                <a href="#mmr-system" class="text-white hover:text-purple-400 transition">MMR System</a>
                <a href="#events" class="text-white hover:text-purple-400 transition">Events</a>
                <a href="#faq" class="text-white hover:text-purple-400 transition">FAQ</a>
            </nav>
            <button class="md:hidden text-white">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto flex flex-col lg:flex-row items-center gap-12">
            <div class="lg:w-1/2">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-6">
                    <span class="text-purple-400 glow-text">Competitive</span> Gorilla Tag at its Finest
                </h2>
                <p class="text-lg text-gray-300 mb-8">
                    Join thousands of players in GTL's official ranking system. Test your skills, climb the leaderboards, 
                    and prove you're the best gorilla in the jungle. Our sophisticated MMR system ensures fair matches 
                    with players of similar skill levels.
                </p>
                <div class="flex space-x-4">
                    <button class="bg-purple-600 hover:bg-purple-700 text-white px-6 py-3 rounded-lg font-medium transition">
                        Register Now
                    </button>
                    <button class="bg-gray-700 hover:bg-gray-600 text-white px-6 py-3 rounded-lg font-medium transition">
                        Watch Trailer
                    </button>
                </div>
            </div>
            <div class="lg:w-1/2 relative">
                <div class="relative">
                    <div class="w-full h-96 bg-gray-800 rounded-xl overflow-hidden">
                        <img src="C:\Users\mason\OneDrive\Pictures\2.png" alt="Upcoming GTL Tournament Banner" class="w-full h-full object-cover">
                    </div>
                    <div class="absolute -bottom-4 -right-4 bg-purple-600/90 backdrop-blur-md rounded-lg px-4 py-2 shadow-lg">
                        <span class="font-bold text-white animate-pulse">LIVE TOURNAMENT IN 2 DAYS</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Rank System Overview -->
    <section id="mmr-system" class="py-16 px-4 sm:px-6 lg:px-8 bg-gray-900/50">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white mb-4">Our MMR-Based <span class="text-purple-400">Ranking System</span></h2>
                <p class="text-lg text-gray-300 max-w-3xl mx-auto">
                    GTL uses an advanced matchmaking rating (MMR) system to determine your skill level and rank.
                    Win matches to gain MMR, lose matches to drop MMR. The better players you beat, the more MMR you earn!
                </p>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8 mb-12">
                <!-- Bronze Rank -->
                <div class="text-center">
                    <div class="mb-4 flex justify-center">
                        <img src="bronze-badge.png" alt="Bronze Rank Badge" class="rank-icon">
                    </div>
                    <h3 class="text-xl font-semibold text-white mb-2">Bronze</h3>
                    <p class="text-gray-400">0 - 999 MMR</p>
                    <div class="mt-2 w-full progress-bar rounded-full">
                        <div class="progress-fill rounded-full" style="width: 25%"></div>
                    </div>
                </div>
                
                <!-- Silver Rank -->
                <div class="text-center">
                    <div class="mb-4 flex justify-center">
                        <img src="silver-badge.png" alt="Silver Rank Badge" class="rank-icon">
                    </div>
                    <h3 class="text-xl font-semibold text-white mb-2">Silver</h3>
                    <p class="text-gray-400">1000 - 1999 MMR</p>
                    <div class="mt-2 w-full progress-bar rounded-full">
                        <div class="progress-fill rounded-full" style="width: 50%"></div>
                    </div>
                </div>
                
                <!-- Gold Rank -->
                <div class="text-center">
                    <div class="mb-4 flex justify-center">
                        <img src="gold-badge.png" alt="Gold Rank Badge" class="rank-icon">
                    </div>
                    <h3 class="text-xl font-semibold text-white mb-2">Gold</h3>
                    <p class="text-gray-400">2000 - 2999 MMR</p>
                    <div class="mt-2 w-full progress-bar rounded-full">
                        <div class="progress-fill rounded-full" style="width: 75%"></div>
                    </div>
                </div>
                
                <!-- Platinum Rank -->
                <div class="text-center">
                    <div class="mb-4 flex justify-center">
                        <img src="platinum-badge.png" alt="Platinum Rank Badge" class="rank-icon">
                    </div>
                    <h3 class="text-xl font-semibold text-white mb-2">Platinum</h3>
                    <p class="text-gray-400">3000 - 3999 MMR</p>
                    <div class="mt-2 w-full progress-bar rounded-full">
                        <div class="progress-fill rounded-full" style="width: 100%"></div>
                    </div>
                </div>
                
                <!-- Diamond Rank -->
                <div class="text-center">
                    <div class="mb-4 flex justify-center">
                        <img src="diamond-badge.png" alt="Diamond Rank Badge" class="rank-icon">
                    </div>
                    <h3 class="text-xl font-semibold text-white mb-2">Diamond</h3>
                    <p class="text-gray-400">4000+ MMR</p>
                    <div class="mt-2 w-full progress-bar rounded-full">
                        <div class="progress-fill rounded-full" style="width: 100%"></div>
                    </div>
                </div>
            </div>
            
            <div class="bg-gray-800/50 rounded-xl p-6 max-w-4xl mx-auto">
                <h3 class="text-xl font-semibold text-white mb-4">How MMR Works</h3>
                <ul class="space-y-4">
                    <li class="flex items-start">
                        <div class="flex-shrink-0 h-6 w-6 text-purple-400 flex items-center justify-center">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <p class="ml-3 text-gray-300">
                            <strong>Rating Adjustments:</strong> The amount of MMR you gain or lose depends on the difference between your MMR and your opponent's MMR.
                        </p>
                    </li>
                    <li class="flex items-start">
                        <div class="flex-shrink-0 h-6 w-6 text-purple-400 flex items-center justify-center">
                            <i class="fas fa-trophy"></i>
                        </div>
                        <p class="ml-3 text-gray-300">
                            <strong>Win Streaks:</strong> Players on winning streaks will gain bonus MMR to help them reach their true skill level faster.
                        </p>
                    </li>
                    <li class="flex items-start">
                        <div class="flex-shrink-0 h-6 w-6 text-purple-400 flex items-center justify-center">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <p class="ml-3 text-gray-300">
                            <strong>Decay Protection:</strong> Players below Diamond rank don't experience MMR decay, while Diamond players must play regularly to maintain their rank.
                        </p>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Leaderboard Section -->
    <section id="rankings" class="py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white mb-4">Current <span class="text-purple-400">Leaderboard</span></h2>
                <p class="text-lg text-gray-300 max-w-3xl mx-auto">
                    Top 10 players in the Gorilla Tag League. Can you make it to the top?
                </p>
            </div>
            
            <div class="bg-gray-900/50 rounded-xl overflow-hidden">
                <div class="grid grid-cols-12 bg-gray-800 px-6 py-4 font-semibold text-gray-300">
                    <div class="col-span-1">#</div>
                    <div class="col-span-3">PLAYER</div>
                    <div class="col-span-2">RANK</div>
                    <div class="col-span-2">MMR</div>
                    <div class="col-span-2">WINS</div>
                    <div class="col-span-2">WIN RATE</div>
                </div>
                
                <div id="leaderboard-entries" class="divide-y divide-gray-800">
                    <!-- This will be populated by JavaScript -->
                </div>
                
                <div class="px-6 py-4 bg-gray-800 flex justify-center">
                    <button class="text-purple-400 hover:text-purple-300 font-medium">
                        View Full Leaderboard →
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Tournaments Section -->
    <section id="events" class="py-16 px-4 sm:px-6 lg:px-8 bg-gray-900/50">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white mb-4">Upcoming <span class="text-purple-400">Tournaments</span></h2>
                <p class="text-lg text-gray-300 max-w-3xl mx-auto">
                    Compete in official GTL tournaments with cash prizes, exclusive cosmetics, and bragging rights!
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Tournament Card 1 -->
                <div class="player-card rounded-xl overflow-hidden">
                    <div class="relative">
                        <img src="summer-championship-banner.jpg" alt="GTL Summer Championship Banner" class="w-full h-48 object-cover">
                        <div class="absolute top-4 right-4 bg-purple-600 rounded-md px-3 py-1 text-sm font-semibold text-white">
                            <span>REGISTER OPEN</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h3 class="text-xl font-bold text-white">GTL Summer Championships</h3>
                            <span class="bg-gray-700 text-white text-xs px-2 py-1 rounded">$5,000 PRIZE</span>
                        </div>
                        <div class="flex items-center text-sm text-gray-400 mb-4">
                            <i class="far fa-calendar mr-2"></i>
                            <span>July 15-17, 2024</span>
                        </div>
                        <p class="text-gray-300 mb-4">
                            The biggest Gorilla Tag tournament of the summer! Open to all players Gold rank and above.
                        </p>
                        <button class="w-full bg-purple-600 hover:bg-purple-700 text-white py-2 rounded-md font-medium transition">
                            Register Now
                        </button>
                    </div>
                </div>
                
                <!-- Tournament Card 2 -->
                <div class="player-card rounded-xl overflow-hidden">
                    <div class="relative">
                        <img src="newcomers-challenge-banner.jpg" alt="GTL Newcomers Challenge Banner" class="w-full h-48 object-cover">
                        <div class="absolute top-4 right-4 bg-yellow-500 rounded-md px-3 py-1 text-sm font-semibold text-gray-900">
                            <span>BEGINNER ONLY</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h3 class="text-xl font-bold text-white">Newcomers Challenge</h3>
                            <span class="bg-gray-700 text-white text-xs px-2 py-1 rounded">$1,000 PRIZE</span>
                        </div>
                        <div class="flex items-center text-sm text-gray-400 mb-4">
                            <i class="far fa-calendar mr-2"></i>
                            <span>June 28, 2024</span>
                        </div>
                        <p class="text-gray-300 mb-4">
                            Exclusive tournament for Bronze and Silver players only. Top 3 win special cosmetics!
                        </p>
                        <button class="w-full bg-purple-600 hover:bg-purple-700 text-white py-2 rounded-md font-medium transition">
                            Register Now
                        </button>
                    </div>
                </div>
                
                <!-- Tournament Card 3 -->
                <div class="player-card rounded-xl overflow-hidden">
                    <div class="relative">
                        <img src="monthly-grind-banner.jpg" alt="GTL Monthly Grind Banner" class="w-full h-48 object-cover">
                        <div class="absolute top-4 right-4 bg-gray-600 rounded-md px-3 py-1 text-sm font-semibold text-white">
                            <span>FREE ENTRY</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-4">
                            <h3 class="text-xl font-bold text-white">Monthly GTL Grind</h3>
                            <span class="bg-gray-700 text-white text-xs px-2 py-1 rounded">RANK POINTS</span>
                        </div>
                        <div class="flex items-center text-sm text-gray-400 mb-4">
                            <i class="far fa-calendar mr-2"></i>
                            <span>Every Saturday</span>
                        </div>
                        <p class="text-gray-300 mb-4">
                            Weekly competitive series where players can earn bonus MMR and special rewards.
                        </p>
                        <button class="w-full bg-purple-600 hover:bg-purple-700 text-white py-2 rounded-md font-medium transition">
                            View Schedule
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white mb-4">Frequently <span class="text-purple-400">Asked Questions</span></h2>
                <p class="text-lg text-gray-300 max-w-3xl mx-auto">
                    Got questions? We've got answers about the Gorilla Tag League and our competitive system.
                </p>
            </div>
            
            <div class="max-w-4xl mx-auto">
                <div class="space-y-4">
                    <!-- FAQ Item 1 -->
                    <div class="player-card rounded-lg overflow-hidden">
                        <button onclick="toggleFAQ(1)" class="w-full flex justify-between items-center p-6 text-left">
                            <h3 class="text-lg font-semibold text-white">How does MMR calculation work in GTL?</h3>
                            <i class="fas fa-chevron-down text-purple-400 transition-transform" id="faq-1-chevron"></i>
                        </button>
                        <div id="faq-1-content" class="px-6 pb-6 hidden">
                            <p class="text-gray-300">
                                Our MMR system compares your rating to your opponents' ratings. Beating higher-rated opponents gives you more MMR, while losing to lower-rated opponents costs more MMR. The exact formula takes into account match performance and variance calculations to ensure fair progression.
                            </p>
                        </div>
                    </div>
                    
                    <!-- FAQ Item 2 -->
                    <div class="player-card rounded-lg overflow-hidden">
                        <button onclick="toggleFAQ(2)" class="w-full flex justify-between items-center p-6 text-left">
                            <h3 class="text-lg font-semibold text-white">Is there a minimum MMR requirement for tournaments?</h3>
                            <i class="fas fa-chevron-down text-purple-400 transition-transform" id="faq-2-chevron"></i>
                        </button>
                        <div id="faq-2-content" class="px-6 pb-6 hidden">
                            <p class="text-gray-300">
                                Most tournaments have MMR requirements that correspond to ranks. For example, our Summer Championships require Gold rank or higher (2000+ MMR). However, we also host beginner tournaments specifically for Bronze and Silver players.
                            </p>
                        </div>
                    </div>
                    
                    <!-- FAQ Item 3 -->
                    <div class="player-card rounded-lg overflow-hidden">
                        <button onclick="toggleFAQ(3)" class="w-full flex justify-between items-center p-6 text-left">
                            <h3 class="text-lg font-semibold text-white">How often is MMR updated?</h3>
                            <i class="fas fa-chevron-down text-purple-400 transition-transform" id="faq-3-chevron"></i>
                        </button>
                        <div id="faq-3-content" class="px-6 pb-6 hidden">
                            <p class="text-gray-300">
                                MMR updates immediately after each ranked match. However, rank promotions (Bronze to Silver, etc.) only occur at the end of each competitive season unless you reach the full MMR threshold for promotion earlier.
                            </p>
                        </div>
                    </div>
                    
                    <!-- FAQ Item 4 -->
                    <div class="player-card rounded-lg overflow-hidden">
                        <button onclick="toggleFAQ(4)" class="w-full flex justify-between items-center p-6 text-left">
                            <h3 class="text-lg font-semibold text-white">Can I check my match history and stats?</h3>
                            <i class="fas fa-chevron-down text-purple-400 transition-transform" id="faq-4-chevron"></i>
                        </button>
                        <div id="faq-4-content" class="px-6 pb-6 hidden">
                            <p class="text-gray-300">
                                Yes! Once you register for GTL, you'll get access to your personal dashboard with detailed statistics including win/loss records, match history, performance trends, and more. You can even review heatmaps of your movement patterns!
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="py-16 px-4 sm:px-6 lg:px-8 bg-gradient-to-r from-purple-900/50 to-blue-900/50">
        <div class="max-w-5xl mx-auto text-center">
            <h2 class="text-3xl font-bold text-white mb-6">Join the GTL Community</h2>
            <p class="text-lg text-gray-300 mb-8 max-w-3xl mx-auto">
                Stay updated on the latest tournaments, rank adjustments, and community events. Subscribe to our newsletter!
            </p>
            <div class="flex flex-col sm:flex-row gap-4 max-w-md mx-auto">
                <input type="email" placeholder="Your email address" class="flex-grow px-4 py-3 rounded-md bg-gray-800 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-purple-500">
                <button class="bg-purple-600 hover:bg-purple-700 text-white px-6 py-3 rounded-md font-medium transition whitespace-nowrap">
                    Subscribe
                </button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-12 px-4 sm:px-6 lg:px-8 border-t border-gray-800">
        <div class="max-w-7xl mx-auto">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-lg font-semibold text-white mb-4">GTL</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">About</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Leaderboard</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Tournaments</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Blog</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-4">Competitive</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Rank System</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Rules</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Schedule</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Rewards</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-4">Support</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">FAQs</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Contact</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Discord</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Feedback</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-4">Legal</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Terms</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Privacy</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Cookies</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Guidelines</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="mt-12 pt-8 border-t border-gray-800 flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center space-x-4 mb-4 md:mb-0">
                    <img src="C:\Users\mason\Downloads\wa.png" alt="GTL Mini Logo" class="w-10 h-10 rounded-full">
                    <span class="text-gray-300">© 2024 Gorilla Tag League. All rights reserved.</span>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-twitter text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-discord text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-twitch text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-youtube text-xl"></i>
                    </a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Leaderboard data
        const leaderboardData = [
            { position: 1, name: "MonkeyKing", tag: "#GTL1", rank: "Diamond", mmr: 4873, wins: 342, winRate: "78%" },
            { position: 2, name: "GorillaGlue", tag: "#GTL2", rank: "Diamond", mmr: 4621, wins: 289, winRate: "75%" },
            { position: 3, name: "BananaSplit", tag: "#GTL3", rank: "Diamond", mmr: 4415, wins: 312, winRate: "72%" },
            { position: 4, name: "JungleJump", tag: "#GTL4", rank: "Diamond", mmr: 4298, wins: 276, winRate: "69%" },
            { position: 5, name: "SwingMaster", tag: "#GTL5", rank: "Platinum", mmr: 3987, wins: 231, winRate: "67%" },
            { position: 6, name: "ApeEscapes", tag: "#GTL6", rank: "Platinum", mmr: 3876, wins: 198, winRate: "65%" },
            { position: 7, name: "KongStrong", tag: "#GTL7", rank: "Platinum", mmr: 3712, wins: 187, winRate: "63%" },
            { position: 8, name: "TarzanPro", tag: "#GTL8", rank: "Platinum", mmr: 3645, wins: 176, winRate: "62%" },
            { position: 9, name: "MountainMover", tag: "#GTL9", rank: "Platinum", mmr: 3529, wins: 165, winRate: "61%" },
            { position: 10, name: "JungleFever", tag: "#GTL10", rank: "Gold", mmr: 2987, wins: 143, winRate: "58%" },
        ];

        // Populate leaderboard
        const leaderboardContainer = document.getElementById('leaderboard-entries');
        
        leaderboardData.forEach(player => {
            const entry = document.createElement('div');
            entry.className = 'grid grid-cols-12 items-center px-6 py-4 hover:bg-gray-800/50 transition';
            
            // Rank color based on position
            let rankColor = 'text-gray-300';
            if (player.position <= 3) {
                rankColor = 'text-yellow-400';
            } else if (player.position <= 5) {
                rankColor = 'text-purple-400';
            }
            
            entry.innerHTML = `
                <div class="col-span-1 font-bold ${rankColor}">${player.position}</div>
                <div class="col-span-3 font-medium text-white flex items-center">
                    <div class="w-8 h-8 rounded-full bg-gray-700 mr-3 overflow-hidden">
                        <img src="player-avatar-placeholder.jpg" alt="${player.name}'s avatar" class="w-full h-full object-cover">
                    </div>
                    ${player.name}<span class="text-gray-400 ml-1">${player.tag}</span>
                </div>
                <div class="col-span-2">
                    <span class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium bg-${player.rank === 'Diamond' ? 'blue-700' : (player.rank === 'Platinum' ? 'gray-700' : 'yellow-600')} text-white">
                        ${player.rank}
                    </span>
                </div>
                <div class="col-span-2 text-white">${player.mmr}</div>
                <div class="col-span-2 text-white">${player.wins}</div>
                <div class="col-span-2">
                    <div class="w-full bg-gray-700 rounded-full h-2.5">
                        <div class="bg-green-500 h-2.5 rounded-full" style="width: ${player.winRate}"></div>
                    </div>
                    <div class="text-xs text-gray-400 mt-1">${player.winRate}</div>
                </div>
            `;
            
            leaderboardContainer.appendChild(entry);
        });

        // Toggle FAQ items
        function toggleFAQ(num) {
            const content = document.getElementById(`faq-${num}-content`);
            const chevron = document.getElementById(`faq-${num}-chevron`);
            
            if (content.classList.contains('hidden')) {
                content.classList.remove('hidden');
                chevron.classList.add('rotate-180');
            } else {
                content.classList.add('hidden');
                chevron.classList.remove('rotate-180');
            }
        }

        // Mobile menu toggle (placeholder functionality)
        document.querySelector('header button').addEventListener('click', function() {
            alert('Mobile menu would open here in a full implementation');
        });
    </script>
</body>
</html>

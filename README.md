<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Multi-Feature App</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
<style>
  /* Global Styles */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: Arial, sans-serif;
    background: #fff;
    color: white;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  
  
  
  
  
  
  /* Preloader Container */
.preloader {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}
  
  /* First Preloader Styles */
.first-preloader-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  animation: fadeIn 1.5s ease-in-out infinite;
}

.logo {
  width: 80px;
  height: auto;
  margin-bottom: 10px;
}

.app-name {
  font-size: 28px;
  font-weight: bold;
  color: #000;
  padding: 9px;
}

/* Fade In Animation */
@keyframes fadeIn {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}

/* Second Preloader (Spinner) */
.spinner {
  width: 50px;
  height: 50px;
  border: 5px solid rgba(255, 255, 255, 0.1);
  border-top: 5px solid #ffff00;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
  
  
  
  
  
  

  /* Header */
  #header {
    background-color: #fff;
    color: white;
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 1px 5px rgba(85, 85, 85, 0.1);
    position: sticky;
    top: 0;
    z-index: 1000;
  }

  #logo {
    font-size: 20px;
    font-weight: bold;
    flex-grow: 1;
    margin-left: 7px;
    color: #000;
  }

  .icon {
    font-size: 17px;
    cursor: pointer;
    transition: color 0.3s ease;
    margin-left: 15px;
    color: #000;
  }

  .icon:hover {
    color: #cccccc;
  }

  /* Content */
  #content {
    flex-grow: 1;
    padding: 2px;
    overflow-y: auto;
  }
  
  
  
  /* Content Grid */
.content {
    padding: 50px;
}
  
  
  
  
  .sliding-page {
  position: fixed;
  top: 0;
  left: 100%;
  width: 100%;
  height: 100%;
  background: #1a1a1a;
  color: white;
  overflow-y: auto;
  z-index: 1000;
  transition: left 0.5s ease;
}

.sliding-page.active {
  left: 0;
}

.header {
  display: flex;
  align-items: center;
  padding: 10px;
}

.circle-arrow-btn {
  background: #333;
  border-radius: 50%;
  padding: 10px;
  cursor: pointer;
}

.home-section {
  text-align: center;
  margin: 5px 0;
}

.home-image {
  position: relative;
}

.circle-play-btn {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: rgba(0, 0, 0, 0.6);
  border: none;
  border-radius: 50%;
  padding: 15px;
  cursor: pointer;
  color: white;
  font-size: 20px;
}

.info-section {
  display: flex;
  padding: 10px;
  gap: 10px;
}

.info-image img {
  width: 80px;
  height: 120px;
  border-radius: 5px;
}

.info-text h2 {
  margin: 0;
  font-size: 24px;
}

.ratings-section {
  display: flex;
  gap: 10px;
  margin: 10px 0;
}

.tag-buttons {
  display: flex;
  gap: 10px;
  font-size: 14px;
}

.tag-btn {
  background: #444;
  padding: 5px 10px;
  border-radius: 5px;
}

.buttons-section {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 20px 0;
}

.circle-icon {
  background: #333;
  border-radius: 50%;
  padding: 10px;
  cursor: pointer;
}

.play-download-section {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 20px 0;
}

.play-btn, .download-btn {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
}

.cast-crew-section {
  margin: 20px;
}

.cast-slider {
  display: flex;
  gap: 10px;
  overflow-x: auto;
}

.cast-slider img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
  
  
  
  
  
  .feature-page {
    display: none;
    padding: 20px;
  }

  .feature-page.active {
    display: block;
  }

  
  
  

  .feature-page {
    display: none;
    width: 100%;
  }

  .feature-page.active {
    display: block;
  }

  /* Games Section */
    .games-container {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    
    
    
    
    
    
    
    
    
    
    
    
    
    /* Back-to-Top Button Styling */
#backToTopBtn {
    position: fixed;
    bottom: 60px; /* Distance from bottom */
    right: 20px; /* Distance from right */
    font-size: 50px; /* Adjust icon size */
    color: #ff4e50; /* Icon color */
    background: none;
    border: none;
    cursor: pointer;
    display: none; /* Initially hidden */
    opacity: 0;
    transition: opacity 0.4s, transform 0.3s;
}

/* Show button when scrolling */
#backToTopBtn.show {
    display: block;
    opacity: 1;
    transform: scale(1);
}

/* Hover effect */
#backToTopBtn:hover {
    color: #fc913a; /* Change color on hover */
    transform: scale(1.1);
}
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    /* Categories Container */
.categories-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2px;
}

/* Category Titles */
.category-title {
    font-size: 24px;
    margin-bottom: 15px;
    color: #ffcc00;
}

/* Games Grid */
.games-grid {
    display: flex;
    justify-content: center;
    gap: 25px;
    flex-wrap: wrap;
    max-width: 900px;
    margin: 0 auto;
}

/* Game Cards */
.game-card {
    width: 180px;
    height: 220px;
    background: linear-gradient(135deg, #fff 0%, #222 100%);
    padding: 40px;
    border-radius: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    transition: transform 0.3s, box-shadow 0.3s;
    cursor: pointer;
    box-shadow: 0 5px 15px rgba(255, 255, 255, 0.1);
}

/* Hover Effect */
.game-card:hover {
    transform: scale(1.15);
    box-shadow: 0 10px 25px rgba(255, 255, 255, 0.3);
}

/* Icons */
.icon-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.icon-container i {
    font-size: 32px;
    margin-bottom: 15px;
    color: #fff;
}

.icon-container span {
    font-size: 16px;
    font-weight: bold;
}
    
    
    
    
    
    
    
    
    
    

    .games-row {
      display: flex;
      gap: 10px;
    }

    .game-card {
      flex: 1;
      height: 169px;
      background-color: #f3f3f3;
      border-radius: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.3s ease;
      
      
    }

    .game-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .game-card:hover {
      transform: scale(1.05);
    }

  /* Footer */
  .footer {
    background-color: #fff;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px 0;
    box-shadow: 0 -1px 5px rgba(85, 85, 85, 0.1);
    position: sticky;
    bottom: 0;
    z-index: 1000;
  }

  .footer-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
    color: #000;
    transition: color 0.3s ease;
  }

  .footer-item:hover,
  .footer-item.active {
    color: #cccccc;
  }

  .footer-item i {
    font-size: 22px;
  }

  .footer-item span {
    font-size: 12px;
    margin-top: 5px;
  }
</style>
</head>
<body>







<!-- First Preloader -->
  <div id="first-preloader" class="preloader">
    <div class="first-preloader-content">
      <img src="https://cdn-icons-png.flaticon.com/512/12165/12165084.png" alt="App Logo" class="logo">
      <div class="app-name">Pokii</div>
    </div>
  </div>

  <!-- Second Preloader -->
  <div id="second-preloader" class="preloader" style="display: none;">
  <p></p>
    <div class="spinner"></div>
  </div>









<!-- Header -->
<div id="header">
  <div>
    <img src="https://cdn-icons-png.flaticon.com/512/12165/12165084.png" width="25px" height="25px" alt="">
  </div>
  <div id="logo">Pokii</div>
  <i id="setting" class="fas fa-bell icon" onclick="showFeature('settings')"></i>
  <i class="fas fa-ellipsis-v icon"></i>
</div>

<!-- Content -->
<div id="content">
  <!-- Games Page -->
  <div id="games-page" class="feature-page active">
    
    <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/guess-their-answer_1x1/20241122084004/guess-their-answer_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1" onclick="openSlidingPage()">
          
     </div>
     
     
     <!-- Independent Sliding Page -->
<div class="sliding-page" id="slidingPage">
  <div class="header">
    <div class="circle-arrow-btn" onclick="closeSlidingPage()">
      <i class="fas fa-arrow-left"></i>
    </div>
  </div>

  <!-- Home Section -->
  <div class="home-section">
    <div class="home-image">
      <img src="https://imgs.crazygames.com/guess-their-answer_1x1/20241122084004/guess-their-answer_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Movie Poster">
      <button class="circle-play-btn"><i class="fas fa-play"></i></button>
    </div>
  </div>

  <!-- Info Section -->
  <div class="info-section">
    <div class="info-image">
      <img src="https://imgs.crazygames.com/guess-their-answer_1x1/20241122084004/guess-their-answer_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Movie Thumbnail">
    </div>
    <div class="info-text">
      <h2>The Last Exit</h2>
      <div class="ratings-section">
        <div class="rating">
          <img src="https://via.placeholder.com/20" alt="Rating">
          <div>95%</div>
        </div>
        <div class="rating">
          <img src="https://via.placeholder.com/20" alt="Rating">
          <div>88%</div>
        </div>
      </div>
      <div class="tag-buttons">
        <span class="tag-btn">4K UHD</span>
        <span class="tag-btn">PG-13</span>
        <span>1h 43m</span>
      </div>
    </div>
  </div>

  <!-- Action Buttons -->
  <div class="buttons-section">
    <div class="circle-icon"><i class="fas fa-thumbs-up"></i></div>
    <div class="circle-icon"><i class="fas fa-thumbs-down"></i></div>
  </div>

  <!-- Play & Download Buttons -->
  <div class="play-download-section">
    <button class="play-btn">Play</button>
    <button class="download-btn">Download</button>
  </div>
  
</div>
          
          
          
     
     
     
     
     
        
        <div class="game-card">
          <img src="https://imgs.crazygames.com/slice-master_1x1/20240731033229/slice-master_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2" onclick="openSlidingPage()">
          
         </div>
         
         
         
         
         
         
         
         <!-- Independent Sliding Page -->
<div class="sliding-page" id="slidingPage">
  <div class="header">
    <div class="circle-arrow-btn" onclick="closeSlidingPage()">
      <i class="fas fa-arrow-left"></i>
    </div>
  </div>

  <!-- Home Section -->
  <div class="home-section">
    <div class="home-image">
      <img src="https://imgs.crazygames.com/slice-master_1x1/20240731033229/slice-master_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Movie Poster">
      <button class="circle-play-btn"><i class="fas fa-play"></i></button>
    </div>
  </div>

  <!-- Info Section -->
  <div class="info-section">
    <div class="info-image">
      <img src="https://imgs.crazygames.com/slice-master_1x1/20240731033229/slice-master_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Movie Thumbnail">
    </div>
    <div class="info-text">
      <h2>The Last Exit</h2>
      <div class="ratings-section">
        <div class="rating">
          <img src="https://via.placeholder.com/20" alt="Rating">
          <div>95%</div>
        </div>
        <div class="rating">
          <img src="https://via.placeholder.com/20" alt="Rating">
          <div>88%</div>
        </div>
      </div>
      <div class="tag-buttons">
        <span class="tag-btn">4K UHD</span>
        <span class="tag-btn">PG-13</span>
        <span>1h 43m</span>
      </div>
    </div>
  </div>

  <!-- Action Buttons -->
  <div class="buttons-section">
    <div class="circle-icon"><i class="fas fa-thumbs-up"></i></div>
    <div class="circle-icon"><i class="fas fa-thumbs-down"></i></div>
  </div>

  <!-- Play & Download Buttons -->
  <div class="play-download-section">
    <button class="play-btn">Play</button>
    <button class="download-btn">Download</button>
  </div>

  <!-- Cast & Crew Section -->
  <div class="cast-crew-section">
    <h3>Cast & Crew</h3>
    <div class="cast-slider">
      <img src="https://via.placeholder.com/80" alt="Cast 1">
      <img src="https://via.placeholder.com/80" alt="Cast 2">
      <img src="https://via.placeholder.com/80" alt="Cast 3">
    </div>
  </div>
</div>
         
         
         
      
      </div>
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/games/mahjongg-solitaire/cover_1x1-1707829451340.png?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1"  onclick="openSlidingPage()">
        </div>
        <div class="game-card">
          <img src="https://imgs.crazygames.com/games/arkadium-s-bubble-shooter/cover_1x1-1722870856788.png?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/hexa-sort_1x1/20241120035137/hexa-sort_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://imgs.crazygames.com/skillwarz_1x1/20241119085229/skillwarz_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/wood-block-journey_1x1/20230907100853/wood-block-journey_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://imgs.crazygames.com/color-match-amg_1x1/20241223043903/color-match-amg_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/bubble-blast-pwd_1x1/20240927035025/bubble-blast-pwd_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://imgs.crazygames.com/thief-puzzle_1x1/20240919050737/thief-puzzle_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/games/block-champ/cover_1x1-1707829050219.png?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://imgs.crazygames.com/racing-limits_1x1/20231106035425/racing-limits_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://imgs.crazygames.com/games/onet-connect-classic/cover_1x1-1709113771990.png?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://imgs.crazygames.com/mergest-kingdom_1x1/20241211151323/mergest-kingdom_1x1-cover?auto=format%2Ccompress&q=80&cs=strip&h=175&dpr=1" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/e07f42e340447222129467619dc0e7e4.jpeg" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/f7f310827933ab4fe647a980cddec50a.png" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/972a0e3dabb998d2fb8fce785e2c1fa4.jfif" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=204,height=204,fit=cover,f=auto/8fe1b52b0dce26510d0ebf4cbb484aaf.png" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/05594391d018e94c37744742c566e225.png" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/2196eaa2d7e18946421260cc8147060b.png" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/505695b9-1b21-47fd-a8e1-93345afb57de.png" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://img.poki-cdn.com/cdn-cgi/image/quality=78,width=94,height=94,fit=cover,f=auto/8e60d250151c33ed4f8e5a3e77b64c68.png" alt="Game 2">
        </div>
      </div>
      
      
      
      
      
      
      
      
      
      
      
      <div class="games-container">
      <div class="games-row">
        <div class="game-card">
          <img src="https://tcf.admeen.org/game/17000/16767/200x123/3d-bowling.webp" alt="Game 1">
        </div>
        <div class="game-card">
          <img src="https://tcf.admeen.org/game/18000/17614/200x123/mergest-kingdom.webp" alt="Game 2">
        </div>
      </div>
    </div>
  </div>
      
      
      
      
      
      
      
      
      
      
    </div>
  </div>
      
      
      
      
      
      
      
      
      
    </div>
  </div>
      
      
      
      
      
      
      
      
      
    </div>
  </div>
      
      
      
    </div>
  </div>
      
      
      
      
      
    </div>
  </div>
      
      
      
      
    </div>
  </div>
      
      
    </div>
  </div>
      
      
      
      
    </div>
  </div>
      
      
      
      
      
    </div>
  </div>
      
      
    </div>
  </div>
    
    
    
    
    
    
    
    
    
    
    
    
  </div>
</div>




<!-- Settings Page -->
  <div id="settings" class="feature-page">
    
    
    
    <div class="categories-container">
        
        <!-- Puzzle Games Category -->
        <div class="category">
            <h2 class="category-title"></h2>
            <div class="games-grid">
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-puzzle-piece"></i>
                        <span>Action & Adventure</span>
                    </div>
                </div>
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-gamepad"></i>
                        <span>Arcade</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Adventure Games Category -->
        <div class="category">
            <h2 class="category-title"></h2>
            <div class="games-grid">
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-dice"></i>
                        <span>Board</span>
                    </div>
                </div>
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-mountain"></i>
                        <span>Cards & Casino</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Action Games Category -->
        <div class="category">
            <h2 class="category-title"></h2>
            <div class="games-grid">
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-gem"></i>
                        <span>Casual</span>
                    </div>
                </div>
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-music"></i>
                        <span>Music & Educational</span>
                    </div>
                </div>
                
                
                
                
                
                
                
                <!-- Action Games Category -->
        <div class="category">
            <h2 class="category-title"></h2>
            <div class="games-grid">
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-puzzle-piece"></i>
                    <span>Puzzle</span>
                    </div>
                </div>
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-basketball-ball"></i>
             <span>Racing & Sports</span>
                    </div>
                </div>
                
                
                
                
                
                
                
                
                
                <!-- Action Games Category -->
        <div class="category">
            <h2 class="category-title"></h2>
            <div class="games-grid">
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-shield-alt"></i>
                    <span>Role Playing</span>
                    </div>
                </div>
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-vr-cardboard"></i>
             <span>Simulation</span>
                    </div>
                </div>
                
                
                
                
                
                
                
                
                
                
                <!-- Action Games Category -->
        <div class="category">
            <h2 class="category-title"></h2>
            <div class="games-grid">
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-chess-knight"></i>
                    <span>Strategy</span>
                    </div>
                </div>
                <div class="game-card">
                    <div class="icon-container">
                        <i class="fas fa-question-circle"></i>
             <span>Trivia & Word</span>
                    </div>
                </div>
            </div>
        </div>
                
                
                
                
                
                
                
                
                
                
                
            </div>
        </div>
                
                
                
                
                
                
                
                
                
                
            </div>
        </div>
                
                
                
                
                
                
            </div>
        </div>

    </div>
    
    
    
    
    
  </div>

  <!-- Header Content -->
  <div id="header-content" class="feature-page">
    <h2>Notifications</h2>
    <p>View your recent notifications here.</p>
  </div>
</div>



<!-- Footer -->
<div class="footer">
  <div class="footer-item" onclick="showFeature('games-page')">
    <img src="https://cdn-icons-png.flaticon.com/512/91/91014.png" width="23px" height="23px" alt="">
    <span>Games</span>
  </div>
  <div class="footer-item" onclick="showFeature('settings')">
    <img src="https://www.svgrepo.com/show/512465/menu-navigation-grid-1528.svg" width="23px" height="23px" alt="">
    <span>Categories</span>
  </div>
</div>

<script>
  function showFeature(featureId) {
    const pages = document.querySelectorAll(".feature-page");
    pages.forEach((page) => page.classList.remove("active"));

    const activePage = document.getElementById(featureId);
    if (activePage) {
      activePage.classList.add("active");
    }

    const items = document.querySelectorAll(".footer-item");
    items.forEach((item) => item.classList.remove("active"));
    document.querySelector(`.footer-item[onclick="showFeature('${featureId}')"]`).classList.add("active");
  }
</script>






<script>
    document.addEventListener("DOMContentLoaded", () => {
  const firstPreloader = document.getElementById("first-preloader");
  const secondPreloader = document.getElementById("second-preloader");
  const mainContent = document.getElementById("main-content");

  // Show first preloader for 3 seconds
  setTimeout(() => {
    firstPreloader.style.display = "none";
    secondPreloader.style.display = "flex";

    // Show second preloader for another 3 seconds
    setTimeout(() => {
      secondPreloader.style.display = "none";
      mainContent.style.display = "block";
    }, 3000);
  }, 3000);
});
</script>



<script>
    function openSlidingPage() {
  document.getElementById("slidingPage").classList.add("active");
}

function closeSlidingPage() {
  document.getElementById("slidingPage").classList.remove("active");
}
  </script>










<script>
      // Get the button
const backToTopBtn = document.getElementById("backToTopBtn");

// Show button when user scrolls down
window.addEventListener("scroll", function () {
    if (window.scrollY > 300) {
        backToTopBtn.classList.add("show");
    } else {
        backToTopBtn.classList.remove("show");
    }
});

// Smooth Scroll to Top
function scrollToTop() {
    let scrollToTopInterval = window.requestAnimationFrame(scrollToTop);
    if (document.documentElement.scrollTop > 0 || document.body.scrollTop > 0) {
        window.scrollBy(0, -50);
    } else {
        cancelAnimationFrame(scrollToTopInterval);
    }
}
    </script>








</body>
</html>

<!DOCTYPE html><html lang="sw">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  <title>BONGO FLAVA FOREVER</title>  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #080808;
      color: white;
      padding-bottom: 100px;
    }

    header {
      background: #000;
      padding: 18px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 2px solid gold;
      position: sticky;
      top: 0;
      z-index: 500;
    }

    .logo {
      color: gold;
      font-size: 24px;
      font-weight: bold;
    }

    nav {
      display: flex;
      align-items: center;
      gap: 15px;
    }

    nav a {
      color: white;
      text-decoration: none;
    }

    nav a:hover {
      color: gold;
    }

    .admin-nav-btn {
      background: gold;
      color: black;
      padding: 9px 15px;
      border-radius: 20px;
      font-weight: bold;
    }

    .hero {
      padding: 70px 8%;
      text-align: center;
      background: linear-gradient(135deg, #000, #1a1a1a);
    }

    .hero h1 {
      color: gold;
      font-size: 40px;
    }

    .hero p {
      margin-top: 15px;
      color: #ccc;
    }

    .listen-btn {
      margin-top: 20px;
      padding: 12px 25px;
      border: none;
      border-radius: 30px;
      background: gold;
      color: black;
      font-weight: bold;
      cursor: pointer;
    }

    section {
      padding: 50px 8%;
    }

    h2 {
      color: gold;
      margin-bottom: 25px;
    }

    /* SONGS */

    .chart {
      display: grid;
      gap: 12px;
    }

    .song {
      background: #151515;
      padding: 15px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      border-left: 4px solid gold;
      gap: 15px;
    }

    .rank {
      color: gold;
      font-size: 20px;
      font-weight: bold;
      width: 45px;
    }

    .song-cover {
      width: 60px;
      height: 60px;
      border-radius: 8px;
      overflow: hidden;
      background: #333;
      flex-shrink: 0;
    }

    .song-cover img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .song-info {
      flex: 1;
    }

    .song-info p {
      color: #aaa;
      margin-top: 5px;
    }

    .play {
      background: gold;
      border: none;
      padding: 10px 15px;
      border-radius: 20px;
      cursor: pointer;
      font-size: 16px;
    }

    /* NEW SONGS */

    .new-songs {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
    }

    .card {
      background: #151515;
      padding: 15px;
      border-radius: 10px;
    }

    .card-cover {
      height: 180px;
      border-radius: 10px;
      overflow: hidden;
      background: #333;
      margin-bottom: 15px;
    }

    .card-cover img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .card p {
      color: #aaa;
      margin-top: 5px;
    }

    /* ADMIN LOGIN */

    .admin-login {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.9);
      z-index: 3000;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .login-box {
      background: #151515;
      border: 2px solid gold;
      width: 100%;
      max-width: 400px;
      padding: 30px;
      border-radius: 15px;
    }

    .login-box h2 {
      text-align: center;
    }

    input {
      width: 100%;
      padding: 13px;
      margin-top: 12px;
      border-radius: 8px;
      border: 1px solid #555;
      background: #222;
      color: white;
    }

    .close-btn {
      background: #333;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 10px;
    }

    /* ADMIN DASHBOARD */

    .admin-dashboard {
      display: none;
      min-height: 100vh;
      background: #080808;
      padding-bottom: 100px;
    }

    .admin-header {
      background: #000;
      border-bottom: 2px solid gold;
      padding: 18px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .admin-container {
      padding: 30px 8%;
    }

    .admin-stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
      margin-bottom: 30px;
    }

    .stat {
      background: #151515;
      border: 1px solid #333;
      border-radius: 12px;
      padding: 25px;
      text-align: center;
    }

    .stat h3 {
      color: gold;
      font-size: 30px;
    }

    .stat p {
      color: #aaa;
      margin-top: 8px;
    }

    .add-song-box {
      background: #151515;
      padding: 25px;
      border-radius: 15px;
      margin-bottom: 30px;
      border: 1px solid #333;
    }

    .add-song-box label {
      display: block;
      margin-top: 15px;
      color: gold;
    }

    .admin-song-list {
      display: grid;
      gap: 12px;
    }

    .admin-song {
      background: #151515;
      padding: 15px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      gap: 15px;
    }

    .admin-cover {
      width: 65px;
      height: 65px;
      border-radius: 8px;
      overflow: hidden;
      background: #333;
      flex-shrink: 0;
    }

    .admin-cover img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .admin-info {
      flex: 1;
    }

    .admin-info p {
      color: #aaa;
      margin-top: 5px;
    }

    .edit-btn {
      background: gold;
      color: black;
      border: none;
      padding: 10px;
      border-radius: 8px;
      cursor: pointer;
    }

    .delete-btn {
      background: crimson;
      color: white;
      border: none;
      padding: 10px;
      border-radius: 8px;
      cursor: pointer;
    }

    /* MUSIC PLAYER */

    .music-player {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      background: #111;
      border-top: 2px solid gold;
      padding: 12px 8%;
      display: flex;
      align-items: center;
      gap: 15px;
      z-index: 1000;
    }

    .player-info {
      flex: 1;
    }

    .player-info strong {
      color: gold;
    }

    audio {
      width: 45%;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: #000;
      color: #888;
      border-top: 1px solid #333;
    }

    @media (max-width: 600px) {

      header {
        flex-direction: column;
        gap: 15px;
      }

      nav {
        flex-wrap: wrap;
        justify-content: center;
      }

      .hero h1 {
        font-size: 28px;
      }

      .music-player {
        padding: 10px;
        flex-wrap: wrap;
      }

      audio {
        width: 100%;
      }

      .admin-song {
        flex-wrap: wrap;
      }

      .admin-header {
        gap: 15px;
      }
    }
  </style></head><body>  <!-- MAIN WEBSITE -->  <div id="mainWebsite"><header>

  <div class="logo">🎧 BONGO FLAVA FOREVER</div>

  <nav>
    <a href="#home">Home</a>
    <a href="#chart">Chart</a>
    <a href="#new">Nyimbo Mpya</a>

    <a href="#" class="admin-nav-btn" onclick="openLogin(); return false;">
      🔐 Admin
    </a>
  </nav>

</header>


<section class="hero" id="home">

  <h1>🔥 BONGO FLAVA FOREVER 🔥</h1>

  <p>
    Nyumbani kwa Bongoflava. Sikiliza nyimbo
    na uone nyimbo zinazotawala chart.
  </p>

  <button class="listen-btn" onclick="playFirstSong()">
    🎵 SIKILIZA SASA
  </button>

</section>


<section id="chart">

  <h2>🏆 BONGO FLAVA CHART</h2>

  <div class="chart" id="chartSongs"></div>

</section>


<section id="new">

  <h2>🔥 NYIMBO MPYA</h2>

  <div class="new-songs" id="newSongs"></div>

</section>


<footer>

  <p>© 2026 BONGO FLAVA FOREVER 🎵</p>

  <p>Real Music • Real Talent • Forever</p>

</footer>

  </div>  <!-- ADMIN LOGIN -->  <div class="admin-login" id="loginPage"><div class="login-box">

  <h2>🔐 ADMIN LOGIN</h2>

  <input
    type="text"
    id="adminUsername"
    placeholder="Username"
  >

  <input
    type="password"
    id="adminPassword"
    placeholder="Password"
  >

  <button class="listen-btn" onclick="loginAdmin()">
    LOGIN
  </button>

  <br>

  <button class="close-btn" onclick="closeLogin()">
    Funga
  </button>

</div>

  </div>  <!-- ADMIN DASHBOARD -->  <div class="admin-dashboard" id="adminDashboard"><div class="admin-header">

  <div class="logo">
    🎧 BONGO FLAVA FOREVER ADMIN
  </div>

  <button class="close-btn" onclick="logoutAdmin()">
    🚪 Logout
  </button>

</div>


<div class="admin-container">

  <h2>📊 ADMIN DASHBOARD</h2>


  <div class="admin-stats">

    <div class="stat">

      <h3 id="totalSongs">0</h3>

      <p>🎵 Jumla ya Nyimbo</p>

    </div>


    <div class="stat">

      <h3 id="totalChart">0</h3>

      <p>🏆 Chart Songs</p>

    </div>


    <div class="stat">

      <h3>ADMIN</h3>

      <p>👤 Status</p>

    </div>

  </div>


  <!-- ADD SONG -->

  <div class="add-song-box">

    <h2>➕ ONGEZA WIMBO</h2>


    <label>Jina la Wimbo</label>

    <input
      type="text"
      id="songTitle"
      placeholder="Mfano: Nipe Upendo"
    >


    <label>Jina la Msanii</label>

    <input
      type="text"
      id="songArtist"
      placeholder="Mfano: Reo"
    >


    <label>Chagua MP3</label>

    <input
      type="file"
      id="songFile"
      accept="audio/*"
    >


    <label>Chagua Cover Image</label>

    <input
      type="file"
      id="coverFile"
      accept="image/*"
    >


    <button class="listen-btn" onclick="addSong()">
      ➕ ONGEZA WIMBO
    </button>

  </div>


  <!-- MANAGE SONGS -->

  <h2>🎵 SIMAMIA NYIMBO</h2>

  <div
    class="admin-song-list"
    id="adminSongList"
  ></div>

</div>

  </div>  <!-- MUSIC PLAYER -->  <div class="music-player"><div class="player-info">

  <strong id="playerTitle">
    Hakuna wimbo unaochezwa
  </strong>

  <br>

  <span id="playerArtist">
    BONGO FLAVA FOREVER
  </span>

</div>


<audio id="audioPlayer" controls>
  Browser yako haisapoti audio.
</audio>

  </div>  <script>

    /*
      ADMIN LOGIN

      BADILISHA HAPA USERNAME NA PASSWORD
    */

    const ADMIN_USERNAME = "admin";

    const ADMIN_PASSWORD = "1234";


    /*
      DEFAULT SONGS
    */

    let songs = JSON.parse(
      localStorage.getItem("bongoSongs")
    ) || [

      {
        title: "Jina la Wimbo 1",
        artist: "Msanii 1",
        audio: "nyimbo1.mp3",
        cover: "cover1.jpg"
      },

      {
        title: "Jina la Wimbo 2",
        artist: "Msanii 2",
        audio: "nyimbo2.mp3",
        cover: "cover2.jpg"
      },

      {
        title: "Jina la Wimbo 3",
        artist: "Msanii 3",
        audio: "nyimbo3.mp3",
        cover: "cover3.jpg"
      }

    ];


    /*
      SAVE SONGS
    */

    function saveSongs() {

      localStorage.setItem(
        "bongoSongs",
        JSON.stringify(songs)
      );

    }


    /*
      DISPLAY WEBSITE SONGS
    */

    function displaySongs() {

      const chart =
        document.getElementById("chartSongs");

      const newest =
        document.getElementById("newSongs");


      chart.innerHTML = "";

      newest.innerHTML = "";


      songs.forEach((song, index) => {

        chart.innerHTML += `

          <div class="song">

            <div class="rank">
              #${index + 1}
            </div>

            <div class="song-cover">

              <img
                src="${song.cover}"
                alt="Cover"
              >

            </div>


            <div class="song-info">

              <h3>${song.title}</h3>

              <p>
                🎤 ${song.artist}
              </p>

            </div>


            <button
              class="play"
              onclick="playSong(
                '${song.audio}',
                '${song.title}',
                '${song.artist}'
              )"
            >
              ▶
            </button>

          </div>

        `;

      });


      songs.slice(0, 6).forEach((song) => {

        newest.innerHTML += `

          <div class="card">

            <div class="card-cover">

              <img
                src="${song.cover}"
                alt="Cover"
              >

            </div>


            <h3>${song.title}</h3>


            <p>
              ${song.artist}
            </p>


            <button
              class="listen-btn"
              onclick="playSong(
                '${song.audio}',
                '${song.title}',
                '${song.artist}'
              )"
            >
              ▶ Sikiliza
            </button>

          </div>

        `;

      });


      document.getElementById(
        "totalSongs"
      ).textContent = songs.length;


      document.getElementById(
        "totalChart"
      ).textContent = songs.length;

    }


    /*
      PLAY SONG
    */

    function playSong(
      file,
      title,
      artist
    ) {

      const player =
        document.getElementById(
          "audioPlayer"
        );


      document.getElementById(
        "playerTitle"
      ).textContent = title;


      document.getElementById(
        "playerArtist"
      ).textContent = artist;


      player.src = file;

      player.load();

      player.play().catch(() => {

        alert(
          "Wimbo haukuweza kuchezwa. Hakikisha faili la audio lipo vizuri."
        );

      });

    }


    /*
      PLAY FIRST SONG
    */

    function playFirstSong() {

      if (songs.length === 0) {

        alert(
          "Hakuna wimbo bado."
        );

        return;

      }


      playSong(
        songs[0].audio,
        songs[0].title,
        songs[0].artist
      );

    }


    /*
      ADMIN LOGIN
    */

    function openLogin() {

      document.getElementById(
        "loginPage"
      ).style.display = "flex";

    }


    function closeLogin() {

      document.getElementById(
        "loginPage"
      ).style.display = "none";

    }


    function loginAdmin() {

      const username =
        document.getElementById(
          "adminUsername"
        ).value;


      const password =
        document.getElementById(
          "adminPassword"
        ).value;


      if (
        username === ADMIN_USERNAME &&
        password === ADMIN_PASSWORD
      ) {

        document.getElementById(
          "loginPage"
        ).style.display = "none";


        document.getElementById(
          "mainWebsite"
        ).style.display = "none";


        document.getElementById(
          "adminDashboard"
        ).style.display = "block";


        displayAdminSongs();


      } else {

        alert(
          "Username au Password si sahihi!"
        );

      }

    }


    /*
      LOGOUT
    */

    function logoutAdmin() {

      document.getElementById(
        "adminDashboard"
      ).style.display = "none";


      document.getElementById(
        "mainWebsite"
      ).style.display = "block";

    }


    /*
      ADD SONG
    */

    function addSong() {

      const title =
        document.getElementById(
          "songTitle"
        ).value;


      const artist =
        document.getElementById(
          "songArtist"
        ).value;


      const audioInput =
        document.getElementById(
          "songFile"
        );


      const coverInput =
        document.getElementById(
          "coverFile"
        );


      if (
        !title ||
        !artist ||
        !audioInput.files[0]
      ) {

        alert(
          "Jaza jina la wimbo, msanii na chagua MP3!"
        );

        return;

      }


      const audioURL =
        URL.createObjectURL(
          audioInput.files[0]
        );


      let coverURL =
        "https://via.placeholder.com/300?text=BONGO+FLAVA";


      if (coverInput.files[0]) {

        coverURL =
          URL.createObjectURL(
            coverInput.files[0]
          );

      }


      songs.unshift({

        title: title,

        artist: artist,

        audio: audioURL,

        cover: coverURL

      });


      saveSongs();


      displaySongs();

      displayAdminSongs();


      document.getElementById(
        "songTitle"
      ).value = "";


      document.getElementById(
        "songArtist"
      ).value = "";


      document.getElementById(
        "songFile"
      ).value = "";


      document.getElementById(
        "coverFile"
      ).value = "";


      alert(
        "Wimbo umeongezwa successfully! 🎉"
      );

    }


    /*
      ADMIN SONG LIST
    */

    function displayAdminSongs() {

      const list =
        document.getElementById(
          "adminSongList"
        );


      list.innerHTML = "";


      songs.forEach(
        (song, index) => {

          list.innerHTML += `

            <div class="admin-song">

              <div class="admin-cover">

                <img
                  src="${song.cover}"
                  alt="Cover"
                >

              </div>


              <div class="admin-info">

                <h3>
                  ${song.title}
                </h3>

                <p>
                  🎤 ${song.artist}
                </p>

              </div>


              <button
                class="edit-btn"
                onclick="editSong(${index})"
              >
                ✏️
              </button>


              <button
                class="delete-btn"
                onclick="deleteSong(${index})"
              >
                🗑️
              </button>

            </div>

          `;

        }
      );

    }


    /*
      EDIT SONG
    */

    function editSong(index) {

      const newTitle =
        prompt(
          "Badilisha jina la wimbo:",
          songs[index].title
        );


      const newArtist =
        prompt(
          "Badilisha jina la msanii:",
          songs[index].artist
        );


      if (newTitle) {

        songs[index].title =
          newTitle;

      }


      if (newArtist) {

        songs[index].artist =
          newArtist;

      }


      saveSongs();


      displaySongs();

      displayAdminSongs();

    }


    /*
      DELETE SONG
    */

    function deleteSong(index) {

      const confirmDelete =
        confirm(
          "Una uhakika unataka kufuta wimbo huu?"
        );


      if (!confirmDelete) {

        return;

      }


      songs.splice(
        index,
        1
      );


      saveSongs();


      displaySongs();

      displayAdminSongs();

    }


    /*
      START WEBSITE
    */

    displaySongs();

  </script></body>
</html>

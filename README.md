# joinwithmahir
Join With T H MAHIR

<html>
  <head>
    <title>Join With T H MAHIR</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
      html, body {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
        margin: 0;
        font-family: sans-serif;
        font-size: 18px;
      }

      body {
        max-width: 400px;
        padding: 1rem;
        box-sizing: border-box;
      }

      button {
        display: block;
        padding: 0.75rem 1.25rem;
        border: 0;
        border-radius: 4px;
        background-color: hsl(0, 92%, 57%);
        color: #ffffff;
        user-select: none;
        font-size: 1rem;
        transform-style: preserve-3d;
      }

      button:before,
      button:after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        border-radius: 4px;
        background-color: hsl(0, 89%, 45%);
        transform: translateZ( -5px );
      }

      button:after {
        background-color: hsl(0, 90%, 47%);
        transform: translateZ( -10px );
      }

      .button-wrapper {
        position: relative;
        perspective: 400px;
        align-self: flex-start;
      }

      hgroup {
        width: 100%;
        margin: 0 0 2rem 0;
      }

      h1 {
        font-size: 1.5rem;
        font-weight: 600;
        margin: 0 0 1rem 0;
      }

      h3 {
        font-size: 1rem;
        font-weight: 500;
        margin: 0 0 0.5rem 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: #490cf1;
      }

      a {
        color: inherit;
        text-decoration: none;
      }
    </style>
  </head>
  <body>

    <hgroup>
      <h1>যুক্ত হও আমার সাথে</h1>
      <h3><a href="https://bio.link/thmahir" tabindex="-1">— T H MAHIR</a></h3>
    </hgroup>

    <div class="button-wrapper">
      <button>জয়েন</button>
    </div>



    
     


    <p class="copyright-text text-center">Inspired from HAKIM</p>

    <script>
      const button = document.querySelector( 'button' );

      const distanceBetween = ( p1x, p1y, p2x, p2y ) => {
        const dx = p1x-p2x;
        const dy = p1y-p2y;
        return Math.sqrt( dx*dx + dy*dy );
      };

      document.addEventListener( 'mousemove', event => {
        const radius = Math.max( button.offsetWidth*0.75, button.offsetHeight*0.75, 100 );

        const bx = button.parentNode.offsetLeft + button.offsetLeft + button.offsetWidth/2;
        const by = button.parentNode.offsetTop + button.offsetTop + button.offsetHeight/2;

        const dist = distanceBetween( event.clientX, event.clientY, bx, by );
        const angle = Math.atan2( event.clientY - by, event.clientX - bx );

        const ox = -1 * Math.cos( angle ) * Math.max( ( radius - dist ), 0 );
        const oy = -1 * Math.sin( angle ) * Math.max( ( radius - dist ), 0 );

        const rx = oy / 2;
        const ry = -ox / 2;

        button.style.transition = `all 0.1s ease`;
        button.style.transform = `translate(${ox}px, ${oy}px) rotateX(${rx}deg) rotateY(${ry}deg)`;
        button.style.boxShadow = `0px ${Math.abs(oy)}px ${Math.abs(oy)/radius*40}px rgba(0,0,0,0.15)`;
      } );

      const nocheat = () => button.textContent = 'No cheating 🙅‍♂️';
      const notouch = () => button.textContent = 'This thing doesn\'t work with touch 😢';

      button.addEventListener( 'click', event => button.textContent = 'ওররে..' );
      button.addEventListener( 'keydown', event => { event.preventDefault(); nocheat(); } );
      button.click = nocheat;

      if( navigator.userAgent.match( /Android|iPhone|iPad|iPod/i ) ) notouch();
      window.addEventListener( 'touchstart', notouch );
    </script>

  </body>
</html>

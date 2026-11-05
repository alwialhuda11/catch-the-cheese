squeekchain-project: 23ab738a-50e9-499e-8f79-5090a9231c09

# Catch the Cheese

A one-button, 60-second game powered by Squeekchain's live hamster wheel.

Squeektoshi runs the WHEELY9000 wheel. Wheel passes power the cheese chute, and caught cheese feeds Squeektoshi in-game. Live wheel speed changes the game: Nap slows the cheese, Jog is steady, and Zoomies brings fast golden bonus cheese worth double.

## How to play

- Tap the stage, press Space, or hit the CATCH button when a cheese wedge is in the basket zone.
- A perfect-center catch pays double.
- An early tap or a wedge that hits the floor breaks your streak and drains the snack meter.
- Every catch sends a wedge up to Squeektoshi and fills his in-game snack meter.
- A round lasts 60 seconds. The results screen recaps passes banked, drops powered, and snacks fed.

## Live Squeekchain connection

The game reads the public Squeekchain status API every 2 seconds:

- Endpoint: https://api.squeekchain.com/v1/status
- Wheel speed comes from measurement.rpmMilli (divided by 1000 to get RPM), plus wheel status and freshness.
- Cheese drops are paid for by live wheel passes banked during play, not by a random timer. A "next drop" charge bar shows how close the chute is to dropping the next wedge.
- Modes change with live wheel speed:
  - Nap: the wheel is stopped, the hamster sleeps, and cheese trickles down slowly on stored chute power.
  - Jog: the turning wheel banks passes at a steady pace for normal cheese and normal points.
  - Zoomies: the wheel is fast, passes bank quickly, drops come thick and fast, and every wedge is golden bonus cheese worth double.

If the live feed is unreachable, the game switches to a clearly labeled simulated practice pace. Practice mode is not live data.

Feeding Squeektoshi is in-game only and does not affect the real hamster.

## How to run

No backend, no build step, and no installation are needed. Open index.html in a browser, or serve it from any static host, including GitHub Pages. The game fetches the public Squeekchain API directly from the browser.


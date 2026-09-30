# Trainer Tracker

A web app for indoor rides on a **Magene T100** trainer. It shows live power, cadence, speed, distance, heart rate and calories on an iPhone. Rides are saved to **Noah** or **Jake**, compared on a leaderboard, and can be sent to Strava.

The whole app is one file, `index.html`, hosted free on GitHub Pages.

## What you need

- An iPhone with **Bluefy** (from the App Store), a free browser that can use Bluetooth. Safari can't.
- A Magene T100 trainer
- Optional: a heart rate monitor, such as a Fitbit Air or any Bluetooth chest strap
- Optional: a Bluetooth cadence sensor, because the T100 doesn't measure cadence

## Setup

1. **Host it:**
   - In this GitHub repository, open **Settings → Pages**.
   - Set **Source** to **Deploy from a branch**, choose **main** and **/(root)**, then click **Save**.
   - After a minute the app is live at `https://<username>.github.io/<repo>/`.
2. **Open it:** Open that link in **Bluefy** on the iPhone.
3. **Fitbit Air only:** In the Google Health app, tap **Fitbit Air**, go to **Share heart rate** and turn on **Always visible**.
4. **Riders:** Tap the name at the top left and enter both Noah's and Jake's weight.

To update the app, upload a new `index.html` to the repository and reload the page in Bluefy.

## Riding

1. Close Zwift and the Magene app, because the trainer allows only one Bluetooth connection at a time.
2. Start pedalling to wake the trainer.
3. Tap **Sensors → Connect device** and pick the T100. Repeat for the heart rate monitor or cadence sensor.
4. Tap the name at the top left to choose who's riding.
5. Tap **Start ride**, then **Pause** and **Finish** when you're done. The ride saves to that rider's stats.

## Sending a ride to Strava

On the ride summary, tap **Send to Strava**:

1. Save the file. If the iPhone share menu opens, choose **Save to Files**.
2. On Strava's upload page, tap **Choose file**, pick the ride, then **Save & View**. If the page didn't open by itself, tap **Step 2**.

Automatic uploads need a paid Strava subscription for API access, so the app uses Strava's free manual upload instead.

## Stats and leaderboard

Tap **🏆 Stats** to see Noah vs Jake for this week, this month or all time. The categories are:

- rides, distance, time, calories and longest ride
- best average power, best 5-minute and 20-minute power
- best W/kg: watts per kg of body weight, over 20 minutes
- max power

A 👑 marks the leader in each category, and the ride list lets you delete a ride.

**Back up regularly.** Stats are stored in Bluefy on that phone only, so deleting Bluefy or clearing its data erases them. Use **Export backup** and **Restore backup** at the bottom of the Stats screen.

## How the numbers work

| Metric | Source |
|---|---|
| Power | Sent directly by the T100 |
| Speed and distance | Estimated from power and the rider's weight, like Zwift does (about 200 W ≈ 34 km/h) |
| Cadence | From a Bluetooth cadence sensor, if one is connected |
| Heart rate | From a Bluetooth heart rate monitor, such as a Fitbit Air or chest strap |
| Calories | About 1 kcal per kJ of work |

Power, cadence, speed and heart rate on screen are 3-second averages. Rides are recorded every second.

## Troubleshooting

| Problem | Fix |
|---|---|
| "This browser can't use Bluetooth" | Open the link in Bluefy, and allow Bluetooth under iPhone **Settings → Bluefy**. |
| Trainer not in the list | Pedal to wake it, and close Zwift and the Magene app. |
| Fitbit connects but shows no heart rate | Turn on **Always visible** in Google Health, and wear the band snugly. |
| Want to try it without the trainer | Add `?demo` to the end of the link to see fake ride data. |

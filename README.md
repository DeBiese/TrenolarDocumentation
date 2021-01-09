# Content
* [1. Intro](#1-intro)
* [2. Polar](#2-polar)
  * [2.1. Creating a phased training target](#21-Creating-a-phased-training-target)
* [3. Trenolar](#3-trenolar)
  * [3.1. Configure](#31-configure)
  * [3.2. Trenara](#32-trenara)
  * [3.3. Change Pace Zones](#33-change-pace-zones)
  * [3.4. How Trenolar sets your paces](#34-How-Trenolar-sets-your-paces)
* [4. Trenolar Export](#4-trenolar-export)
  * [4.1. Creating a phased training target](#41-Creating-a-phased-training-target)
  * [4.2. Create a list of training sessions](#42-Create-a-list-of-training-sessions)

___

([Go to top](#content))
# Intro 
Creating a phased training target on the Polar Flow website in such a way that your Polar watch gives you a warning when running too slow/fast requires you to visit multiple pages on the [Polar Flow](https://flow.polar.com/diary) website.

When using a training app like [Trenara](https://www.trenara.com/) which gives you different paces to run throughout your training week, you would spend quite some time on the [Polar Flow](https://flow.polar.com/diary) website planning each training.

Trenolar is a Chrome Extension specifically created to facilitate creating one or more phased training targets on the [Polar Flow](https://flow.polar.com/diary) website without having to visit multiple pages.

The ultimate goal of creating Trenolar is having the Trenara app exporting training sessions that can be uploaded to Polar Flow using the Trenolar extension. For the time being, you still have to manually create your training session on a separate site [Trenolar Export](https://trenolar.azurewebsites.net). 

![Trenolar Export](/images/trenolar-export/te001.png)

The process of creating a training session on the export site is a little easier compared to doing it on the [Polar Flow](https://flow.polar.com/diary) website.

Both processes are documented below. So see for yourselves.

When creating a phased training with multiple paces, each for which you want your watch to warn you when you go too fast/slow, you must be aware that with Polar, you are limited to 5 pace zones.

You can set the lower limits of 5 zones and create a training with phases in those 5 zones and your watch will warn you when you go too fast or too slow.

If you want to run a steady pace, you'll probably use the upper or lower limit of a zone as your 'target pace' in order to have a warning.

If you are like me and prefer a warning when going too fast, Polar effectively limits you to 4 paces. 
That being the lower limits of zones 2 through 5 while setting your phases to zones 1 through 4 during training. There is no 'zone 6 lower limit' so you can not have a warning when going too fast in zone 5.

If you prefer a warning when going too slow, you can use all zones 1 through 5 and have a warning for going too slow.

**NOTE:** 
_If a Polar dev stumbles upon this page. Please consider adding the option of creating phased training targets with a free to set pace for each zone with a possible margin for going too fast/slow in each phase and have the sports watch warn on those margins. Reporting on a training can still use the 5 pace zones to show in which zones a training is run. But runners wouldn't be limitted to 5 paces for receiving feedback during a run._

([Go to top](#content))
# 2. Polar
## 2.1. Creating a phased training target
![Polar Flow navigation header](/images/polar/p001.png)

1. Go to your sport profiles

![Polar Flow sport profiles](/images/polar/p002.png)

2. Edit the sport profile of your choosing

![Polar Flow edit profile](/images/polar/p003.png)

3. Edit the pace settings

![Polar Flow edit pace settings](/images/polar/p004.png)

**NOTE:** _Polar stores the paces you set as speed. To do this, it calculates the speed based on your min/km (or min/mi) and rounds this calculated speed to 2 decimals. So sometimes when you put in a pace Polar might alter it with 1 or 2 seconds due to the rounding while saving._

4. Go to the diary and add a training target

![Polar Flow crete training target](/images/polar/p005.png)

5. Fill in the required fields. (Notice the Sport being equal to the sport profile for which the pace was set)

![Polar Flow training metadata](/images/polar/p006.png)

6. Add phases (Distance/Duration)

![Polar Flow phases](/images/polar/p007.png)

7. Set your phase name, target (distance vs duration) and pace zone(s)

![Polar Flow add phase](/images/polar/p008.png)

8. A finished interval training

![Polar Flow interval training](/images/polar/p009.png)

([Go to top](#content))
# 3. Trenolar
You can find Trenolar in the [Chrome Webstore](https://chrome.google.com/webstore/detail/trenolar/lgmpflmiiihefineimpboladhpbeidli).

For Trenolar to work, you need to be on the Polar Flow website and be logged in. 

Trenolar works within the limitations of Polar Flow. (max 5 paces being the most obvious one)

Trenolar does NOT need you to enter credentials in the extension, it relies on the fact that you already provided those to the Polar Flow website.

Trenolar does NOT store sensitive information. Only the sport connected to the sport profile you choose in configure is stored in your browser along with the option you choose for a warning when going too fast or too slow.
(If you only use Trenolar in an In Private browser session or if you clear your browser cache, you will need to re-configure Trenolar)

Trenolar does NOT send any data to another web service.

## 3.1. Configure
When you first open Trenolar, you will be limited to the 'Configure' part. Trenolar shows all the sport profiles you have in use and you have to pick one that Trenolar will use. Once you have picked a sport profile and saved it, you can use the 'Trenara' and 'Change Pace Zones' parts.

![Trenolar configure](/images/trenolar/t001.png)

**NOTE:** Trenolar will alter your pace settings on this sport profile for each training session you upload.

## 3.2. Trenara

Here you set your preferred training method, you select a file you exported using Trenolar Export and click Add to Polar.

Trenolar will alter the pace settings of your chosen sport profile and create a phased training target using those pace settings.

![Trenolar trenara](/images/trenolar/t002.png)

**NOTE:** If you create multiple training sessions on the Trenolar Export site with different paces, you should **NOT** upload them all using Trenolar. But rather upload each after the previous executed training.

Why? 

Because Trenolar changes the pace settings for each training, but Trenolar is limited to what is possible in Polar Flow. You can only store one set of paces for a sport profile. If you would create 2 or more training sessions with completely different paces and upload them all in 1 go. You would end up running all your training sessions using the paces from the last uploaded training session.

## 3.3. Change Pace Zones

This part is created to easily see (and possibly change) your current pace settings for your chosen sport profile. If you created a training on Trenolar Export, you don't need to set your paces here again. That will be done for you when you upload the training session.

![Trenolar pace settings](/images/trenolar/t003.png)

## 3.4. How Trenolar sets your paces
Trenolar interprets the paces you added to your exported file. If you used the maximum of 5, those 5 are copied as is.
If you entered less than 5, Trenolar adds paces using a formula to come to 5. (Because Polar Flow has 5 pace zones and trying to fit the paces in a file in the current paces is too much hassle.)
Your preferred training method (warning when going too fast vs too slow) is also taken into account.

_Note: keep in mind that Polar Flow uses rounded speed calculated from pace which will affect imported paces as well._

The x-es in the tables below are filled in as follows:
- in a lower zone number: speed - 1 (km/u or mph)
- in a higher zone number: speed + 0.5 (km/u or mph)

### 3.4.1 One pace
Your training will be in zone 1.
|Your paces|Zone|Too Fast|Too slow|
|----------|----|--------|--------|
|06:00|5|x|x|
|     |4|x|x|
|     |3|x|x|
|     |2|06:00|x|
|     |1|x|06:00|

### 3.4.2 Two paces
Your training will be in zones 1 and 2.
|Your paces|Zone|Too Fast|Too slow|
|----------|----|--------|--------|
|05:30|5|x|x|
|06:00|4|x|x|
|     |3|05:30|x|
|     |2|06:00|05:30|
|     |1|x|06:00|

### 3.4.3 Three paces
Your training will be in zones 1 through 3.
|Your paces|Zone|Too Fast|Too slow|
|----------|----|--------|--------|
|05:00|5|x|x|
|05:30|4|05:00|x|
|06:00|3|05:30|05:00|
|     |2|06:00|05:30|
|     |1|x|06:00|

### 3.4.4 Four paces
Your training will be in zones 1 through 4.
|Your paces|Zone|Too Fast|Too slow|
|----------|----|--------|--------|
|04:30|5|04:30|x|
|05:00|4|05:00|04:30|
|05:30|3|05:30|05:00|
|06:00|2|06:00|05:30|
|     |1|x|06:00|

### 3.4.5 Five paces
Warn when too fast:

Your training will be in zones 1 through 4.
You can not have 5 paces to warn when going too fast.
If warn when going too fast is your preferred training method, having a training with 5 paces means that you will have one phase that is double used and thus your slowest pace in the training will be a "warn when too slow".
Again, working within the limitations of Polar Flow.

Warn when too slow:

Your training will be in zones 1 through 5.
|Your paces|Zone|Too Fast|Too slow|
|----------|----|--------|--------|
|04:00|5|04:00|04:00|
|04:30|4|04:30|04:30|
|05:00|3|05:00|05:00|
|05:30|2|05:30|05:30|
|06:00|1|06:00|06:00|

([Go to top](#content))
# 4. Trenolar Export
The Trenolar Export site allows you to create a complete training session on 1 page.

You create the paces you need and use those to create training phases. Each pace you create has a distance/duration button to prefill a new training phase.

The training phases grid allows you to easily move phases up and down and even copy phases (above/below/at the top/at the bottom). Even when you choose to have repeating phases, you can still move your phases around.

All in all a more user friendly way of creating a training.

## 4.1. Creating a phased training target

1. Fill in the required fields

![Trenolar Export training](/images/trenolar-export/te003.png)

2. Create the paces required for your training session

![Trenolar Export Paces](/images/trenolar-export/te002.png)

3. Use the buttons on the pace grid to quickly prepare phases

![Trenolar Export](/images/trenolar-export/te004.png)

4. Prepare a training phase (Fields are prefilled when using the buttons on the pace grid)

![Trenolar Export phase](/images/trenolar-export/te005.png)

5. Add the phases for your training

![Trenolar Export finished phases](/images/trenolar-export/te006.png)

6. Export the training session

![Trenolar Export export session](/images/trenolar-export/te007.png)

## 4.2. Create a list of training sessions
_Coming soon_
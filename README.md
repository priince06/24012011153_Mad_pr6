# MAD Practical 6 --- Android Animations & Alarm Service

A Kotlin-based Android application created for **Mobile Application
Development (MAD) Practical 6**. The project demonstrates Android
drawable animations, view animations, a splash screen, a digital clock,
and the basic structure of an alarm service controlled through a
broadcast receiver.

## 📌 Practical Details

-   **Subject:** Mobile Application Development
-   **Practical:** 6
-   **Student:** Prince Prajapati
-   **Enrollment No.:** 24012011153
-   **Platform:** Android
-   **Language:** Kotlin
-   **UI:** XML layouts

## ✨ Concepts Covered

-   **Splash screen:** Displays an animated screen before opening the
    main activity.
-   **Gradient background:** Uses an XML shape drawable with a radial
    gradient.
-   **Frame animation:** Uses `AnimationDrawable` and `<animation-list>`
    to animate drawable frames.
-   **View animations:** Demonstrates XML animation tags:
    -   `<set>` --- groups animations
    -   `<scale>` --- changes size
    -   `<translate>` --- moves a view
    -   `<rotate>` --- rotates a view
    -   `<alpha>` --- changes transparency (where configured)
-   **Animation timing:** Uses attributes such as `android:duration`,
    `android:startOffset`, `android:repeatCount`, and
    `android:repeatMode`.
-   **Digital clock:** Displays the current time and date with
    `TextClock`.
-   **Alarm service structure:** Uses an Android `Service` and
    `MediaPlayer` to play an alarm sound.
-   **Broadcast receiver:** Demonstrates receiving a start/stop action
    and starting or stopping the alarm service.

## 🖥️ Main Screen

The main screen contains: - An animated image area - An explanation of
the alarm controls - A live digital clock - Create Alarm and Cancel
Alarm buttons

The splash screen uses an animated drawable and a view animation before
navigating to `MainActivity`.

## 📁 Important Project Components

  -----------------------------------------------------------------------
  Component                           Purpose
  ----------------------------------- -----------------------------------
  `MainActivity.kt`                   Loads the main layout and
                                      starts/stops drawable animations
                                      when window focus changes.

  `SplashActivity.kt`                 Runs the splash animations and
                                      opens the main activity when the
                                      view animation ends.

  `AlarmService.kt`                   Plays and releases the alarm audio
                                      using `MediaPlayer`.

  `AlarmBroadcastReciver.kt`          Receives a start/stop value and
                                      starts or stops `AlarmService`.

  `activity_main.xml`                 Defines the main screen, animated
                                      images, clock, and buttons.

  `activity_splash.xml`               Defines the splash screen layout.

  `activity_alarm_service.xml`        Layout file associated with the
                                      alarm service component in the
                                      practical.

  `res/drawable/`                     Contains drawable animation lists
                                      and the gradient shape drawable.

  `res/anim/`                         Contains XML view-animation
                                      resources such as scale, translate,
                                      and rotate animations.

  `AndroidManifest.xml`               Declares application activities and
                                      the launcher activity.
  -----------------------------------------------------------------------

> Resource names and package names may vary if the project has been
> renamed or recreated in Android Studio.

## 🚀 Run the Project

1.  Install **Android Studio**.
2.  Open the Android project folder in Android Studio.
3.  Allow Gradle to sync and resolve the project dependencies.
4.  Check that the drawable, animation, and raw audio resources
    referenced by the Kotlin code exist in the appropriate `res/`
    folders.
5.  Select an Android emulator or connect an Android device with USB
    debugging enabled.
6.  Build and run the application.

## ⚙️ Implementation Notes

-   The splash screen is configured as the launcher activity in the
    manifest.
-   The main screen uses `AnimationDrawable` for frame-based drawable
    animation.
-   The splash animation listener starts `MainActivity` after the
    animation finishes.
-   `AlarmService` loads the alarm audio from `res/raw/` and releases
    the `MediaPlayer` when the service is destroyed.
-   To make the Create Alarm and Cancel Alarm buttons fully functional,
    ensure their click listeners send the corresponding start/stop
    values to the broadcast receiver and that the receiver is registered
    appropriately for the Android version targeted.
-   Review service and receiver declarations, permissions, and
    background-execution requirements if adapting this classroom example
    for modern Android versions.

## 🎯 Learning Outcome

This practical helps demonstrate how Android XML resources and Kotlin
code work together to create animations, build a splash screen, display
live time, and organize background audio playback using a service and
broadcast receiver.

## 📄 Academic Use

Prepared as a college **Mobile Application Development Practical 6**
submission. This repository is intended for learning and academic
demonstration.

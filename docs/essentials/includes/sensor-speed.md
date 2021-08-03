---
ms.topic: include
---
## [Sensor Speed](xref:Xamarin.Essentials.SensorSpeed)

- **Fastest** – Get the sensor data as fast as possible (not guaranteed to return on UI thread).
- **Game** – Rate suitable for games (not guaranteed to return on UI thread).
- **Default** – Default rate suitable for screen orientation changes.
- **UI** – Rate suitable for general user interface.

If your event handler is not guaranteed to run on the UI thread, and if the event handler needs to access user-interface elements, use the [`MainThread.BeginInvokeOnMainThread`](~/essentials/main-thread.md) method to run that code on the UI thread.

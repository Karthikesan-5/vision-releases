# Vision — update channel

**Powered by ZentOS.** Builds only. The source lives in
[vision-os](https://github.com/Karthikesan-5/vision-os) (backend + installer) and
[vision-os-unity](https://github.com/Karthikesan-5/vision-os-unity) (desktop app).

## Installing or updating

1. Download `Vision_windows.zip` from the newest release on the
   [Releases](../../releases) page.
2. Extract it anywhere on the Windows PC. Keep `Vision.exe` and the `Backend`
   folder together — that folder is the whole product.
3. Double-click `Vision.exe`. On a new machine it provisions itself: Windows
   asks once for administrator rights, then Vision installs the GPU runtime,
   the PeopleNet model and the engine, and starts when it can prove real
   inference is running.

**Updating an existing install:** extract the new folder next to the old one and
copy your `Backend\configs` folder across (it holds your cameras, zones and the
credentials file). Nothing else needs to be carried over.

## Verifying a download

Every release ships `SHA256SUMS.txt`. On Windows:

```
certutil -hashfile Vision_windows.zip SHA256
```

The printed hash must match the line in `SHA256SUMS.txt`.

## Requirements

- Windows 10/11, 64-bit
- An NVIDIA GPU (GTX 10-series or newer; RTX 3060 and RTX 4080 are the
  validated cards) with a current driver
- About 6 GB free disk for the runtime, model and engine cache
- Internet access on first launch only, to download the runtime and model

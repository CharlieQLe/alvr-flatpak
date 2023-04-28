# ALVR Flatpak

This is an experimental Flatpak for ALVR! It is **only** compatible with the Flatpak version of Steam! For all non-Flatpak Steam users, use the AppImage that is already provided.

## Installation

Currently, no precompiled builds are available. However, building from source does not take very long, and just requires the usage of the terminal.

1. Install the Flatpak dependencies from the Flathub repository

```
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.flatpak.Builder org.freedesktop.Sdk//22.08
```

For AMD users, install the Mesa codec extensions as well

```
flatpak install org.freedesktop.Platform.GL.default//22.08-extra org.freedesktop.Platform.GL32.default//22.08-extra
```

2. Clone and enter this repository

```
git clone https://github.com/CharlieQLe/alvr-flatpak.git
cd alvr-flatpak
```

3. Build and install the flatpak

```
flatpak run org.flatpak.Builder --user --install --force-clean build-dir com.valvesoftware.Steam.Utility.alvr.json
```

## Usage

To launch the ALVR Dashboard, run the following command:

```
flatpak run --command=alvr_dashboard com.valvesoftware.Steam
```


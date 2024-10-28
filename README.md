To install Android Studio on Linux or Ubuntu, follow these steps:

### Step 1: Update and Install Prerequisites
Open a terminal and update the system, then install required packages:

```bash
sudo apt update
sudo apt install -y wget unzip openjdk-11-jdk
```

### Step 2: Download Android Studio
Visit the [Android Studio download page](https://developer.android.com/studio) to get the latest version URL or download it with:

```bash
wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/2023.1.1.20/android-studio-2023.1.1.20-linux.tar.gz
```

### Step 3: Extract the Archive
Extract the downloaded file:

```bash
tar -xzf android-studio-*-linux.tar.gz
```

### Step 4: Move to /opt Directory
Move Android Studio to `/opt` to make it accessible to all users:

```bash
sudo mv android-studio /opt/
```

### Step 5: Launch Android Studio
Start Android Studio using the `studio.sh` script:

```bash
/opt/android-studio/bin/studio.sh
```

### Step 6: Create a Desktop Entry (Optional)
To make it easier to launch, create a desktop entry:

```bash
cat <<EOF | sudo tee /usr/share/applications/android-studio.desktop
[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Icon=/opt/android-studio/bin/studio.png
Exec="/opt/android-studio/bin/studio.sh" %f
Comment=Android Studio IDE
Categories=Development;IDE;
Terminal=false
EOF
```

### Step 7: Complete Installation
Open Android Studio from the applications menu or by running `/opt/android-studio/bin/studio.sh` to complete the setup and install the necessary SDK components.

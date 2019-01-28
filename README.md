# OptiFlow plugin for UE4
This plugin provides the means to extract optical flow data from Unreal Engine. It is based on [ProfFan's optical flow demo](https://github.com/ProfFan/UnrealOpticalFlowDemo).

# Usage
Currently this plugin requires a patched custom-built Unreal Engine 4. Tested for versions 4.20 and 4.21.

You would need to get UE4 source code, apply `OptiFlowUE4.patch` and then compile the engine. To apply the patch, simply put `OptiFlowUE4.patch` into the root directory of the engine and run `patch -p1 UE4.patch`.

After compiling UE4, use it to create a new project or open an existing one, and then copy `OptiFlow` directory into `Plugins` directory (you may need to create it in the root of the project).

# Usability
Currently this plugin correctly displays optical flow data for movable and stationary UE4 actors, based on velocity frame buffer (also used by engine for motion blur). Static actors' optical flow may be estimated incorrectly.

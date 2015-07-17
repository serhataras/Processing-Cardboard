# Processing-Cardboard
Example Processing-Android Cardboard Stereo photo/VR sketch using Google Android Cardboard SDK

 This example program demonstrates an Android activity app coded with the Processing for Android library and
 the Google Cardboard Android SDK. The objective of this work is to provide an easier 
 development platform using Processing for learning to program VR Android apps for the Cardboard viewer.
 The  Processing-Android library was modified to use the Cardboard SDK.
 The Processing library has an abstraction layer for OPENGL that makes it possible
 to write an Android Cardboard app without using direct Android OPENGL calls. 
 
 Processing with Cardboard SDK may be an alternative for writing Android VR applications. At the least it is
 another way to build/explore/learn the Cardboard VR app development platform.
 
 * Requires Android Studio (1.2.2)
 * Cardboard SDK for Android 0.5.4
 * Based on Processing for Android library version 2.2.1 source code from: https://github.com/processing/processing-android
 * Based on Stereo library source code from: https://github.com/CreativeCodingLab/stereo
 
 * Minimum builds supports Android API 4.1 (16) platform and above
 * Tested with Sony Z1S phone, 1920x1080 pixel display, running Android version 5.0.2, with GPU hardware accelerator
 
 * App description
 
The app displays a stereo photo cube in front of a stereo photo background. In the cardboard viewer the user may change the viewing angle and size of the cube with head movement. A screen tap will bring the cube back to its original location. Tilting the viewer left or right will change the cube size.
 
 * Issues:
 
Distortion correction is disabled because the Cardboard correction feature does not work well.
 The display is not distorted enough to matter with my Unofficial cardboard viewer lens and
 home made Cardboard viewer with stereoscopic quality lens.
 
 Out of memory can result when using large images.
 
 No library build was defined here for Processing Android SDK library ( work in progress)
 
 Notes:
 The magnet trigger does not work well with my phone so I use new convert tap to trigger feature
 available in Cardboard V2.

 * Modified the Processing-Android Library:

 * PApplet extends CardboardActivity
 
 * The display thread in Processing that calls draw() was replaced by the thread used by Cardboard SDK for its display rendering.

 * SketchSurfaceView extends CardboardView

 * SketchSurfaceViewGL extends CardboardView

 * CardboardView rendering uses CardboardView.Renderer

 * CardboardView.StereoRenderer code is also available

 * Added PStereo class for stereo view control
  
 * Added headtransform, drawleft, drawright functions to Processing
 
 
 Cardboard is a trademark of Google Inc.

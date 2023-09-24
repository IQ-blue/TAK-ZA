# ATAK-CIV

The Android Team Awareness Kit (ATAK-CIV) offers matching capabilities to the ATAK-MIL baseline with minor changes from the military lexicon. 

TAK-CIV is made available to support the principles of civil authority emergency operations: prevention, mitigation, preparation, response, or emergency evacuation and recovery. 

The primary difference between MIL & CIV is the baseline signing key that restricts military specific capability from being loaded through plugins. Just like ATAK-MIL, ATAK-CIV is network-agnostic and works with many tactical communication systems. 

ATAK-CIV supports DoD and commercial formatted maps, imagery, and overlays. 

Where possible, the ATAK application adheres to the user experience design guidelines produced by Google to ensure that end users have a familiar experience.

# 4.10.0.X Long Term Support  
## Notes

Consider this a strongly recommended upgrade for all previous versions of ATAK (4.9 and lower)     

4.10.0.14 (3e3ea7506)

## Bug Fixes

- Telestration deadlocks

4.10.0.13 (f7a968f3c)

## Bug Fixes

- Rework content-changed dispatch request logic to address a potential starvation condition
- Playstore Crash: Route Planning - Setup Spinner
- Resolve various memory retention issues observed with managed ElevationSource instances (takkernel@4.6.28)
- Update SerialMonitor to handle GPS devices in SiRF binary mode

4.10.0.12 (1f4720b60)

## Bug Fixes

- CoT markers Elevation is entered only in Feet (Even when Meters is the preferred unit)
- GOTO Tool should utilize the last used Coordinate Entry Pane and not default to the standard display coordinate system.
- Add option to place Red X by Long Pressing Map
- CotAutoBroadcast does not immediately broadcast a newly added marker.
- Calling ActionBarReceiver.getInstance().setToolView(_layout); needs to be on the UI thread
- Update video libraries to 20230913

4.10.0.11 (73fe0c10e)

## Bug Fixes

- Playstore: Need a way to force English
- Load Preference Category button does not function
- Revert: construct the proper URL for all protocols
- Update to SerialMonitor 4.10.0.0

4.10.0.10 (d438338cc)

## Bug Fixes

- Playstore Crash: Rectangle SetWidth
- CotMapComponent NullPointerException
- Link Eud doInBackground Exception
- Quick Pics not fully removed
- Playstore Crash: IllegalStateException SettingActivity
- Update to Network Monitor 4.10.0.0

4.10.0.9 (bef1f6c17)

## Bug Fixes

- G-EGD map sources do not stream tiles following restart
- construct the proper URL for all protocols
- address model rendering and import deficiencies identified when integrating with cesium ion
- Playstore Crash: NullPointerException GLFeatureMarker
- Playstore Crash: ImportDTEDZSort ConcurrentModification
- Playstore Crash: Relock NPE on Redmi phone
- Unexpected behavior editing a toolbar
- ATAK 4.9/4.10 not importing files from device "Download" folder
- language pack update
- 4.10.0.8 (bec1d4db)

## Bug Fixes

- Shape does not honor closed for showing the fill and transparency incorrectly applied to stroke
- add in support for the DODSWCA-66 certificate

4.10.0.7 (6fec079fe)

## Bug Fixes

- Playstore: IllegalArgumentException Thirdparty Send
- Hide Link EUD Tool from the default toolbar
- Support a mechanism to reliably send p2p without tcp
- correct extension issue in the AndroidManifest dpkg -> dpk
- Lasso Hashtag
- Ellipses flicker when sending updates
- Micro-optimize feature hit-test
- Native imagery optimizations for large datasets/external SD card
- Long Pressing Route Creation does not drop Waypoint when a filled circle is underneath
- In order to support Gateway Systems, add in the destination for directional sending
- MapOverlayManager NPE
- Installing Plugins automatically while launching ATAK causes a NPE
- Minor typographical changes to the javadoc

4.10.0.6 (5c9b040f0)

## Bug Fixes

- Data Package local file import is delayed
- Visibility of 2525 CoT markers not honored after restart

4.10.0.5 (e5ab08da9)

## Bug Fixes

- Map Markers Color Altered by CoT type
- Send hashtag group (make a datapackage and send it)
- StickyTags ON/OFF Switch
- Unable to import a KMZ file with a large comment block
- Fix for rendering of geographic boundaries KML
- Allow custom BP/HAs greater than 6X6
- Address confusion with the visibility icon being used for eye altitude
- Enable scrolling text for GLMarkerFeature

4.10.0.4 (d8d3a151d)

## Bug Fixes

- ArrayIndexOutOfBoundsException: length=10; index=-3 LassoTool cancel
- Direction Arrow not correct for Markers

4.10.0.3 (3f5bae75)

## Bug Fixes

- TrackDetailHandler cannot handle inf in speed
- 9-Line FAHs stick when target is hidden
- Resection dialog remains open when GPS is recovered

4.10.0.2 (763280ab3)

## Bug Fixes

- During clear content RestoreLocation causes a NPE on some devices (preferences)

4.10.0.1 (060308ecc)

## Bug Fixes

- Fix issue when connected to multiple large datasync feeds, hashtags can get into a situation where they no longer display in the Overlay Manager

4.10.0.0 (154b3c4e0)

## Feature Additions

- Significant Performance and Stability Improvements   (If for no other reason, this is the reason to switch)
- Processing and rendering SA points - Note: could not collect and process 40k with ATAK 4.8
- Significant rendering improvements
- Support for MIL-STD 6090 base Event changes
- GoTo Tool Enhancements
- Polar Coordinate Entry Enhancements
- Improved deployments by introducing automatic scanning of the device download folder
- New User Preference "Center on self when using the back button"
- Simplified Contour Lines User Interface
- Updated Viewshed Options
- Data Sync improvements to allow for Datapackage export
- Slicer - CoT Display Control
- Point Dropper Recently Dropped
- Improved 3D Shape Handling and Drawing Tools
- Newly developed application "Helmet Camera"

## Bug Fixes

- Resolved multiple NPEs reported through Google Play store.
- Resolved JNI error occurring on TAB S4 devices.
- Resolved issue with the Shorten Long Marker Name preference causing erratic label behavior.
- Resolved issue with the Self-Marker getting clipped.
- Resolved issue with ATAK crashing when importing a zipped DTED file.
- Resolved issue with ATAK crashing when moving a marker that was part of a datasync feed.
- Resolved issue where the map would be obscured when playing a video on some devices.

## SDK Improvements

The SDK received updated documentation, a general ATAK Application Programming Interface(API)  cleanup  and  ongoing  code  cleanup  of  Fortify  identified  issues.  In  addition  to  this,  documentation is continuing to be updated in wiki.tak.gov to assist third party developers.

- Migrated to Android Gradle Plugin 7.4.2 and Gradle 7.6.1
- Migration of the core libraries to the following levels:
- implementation 'androidx.fragment:fragment:1.5.7'
- implementation 'androidx.exifinterface:exifinterface:1.3.6'
- implementation 'androidx.localbroadcastmanager:localbroadcastmanager:1.1.0'
- implementation 'androidx.lifecycle:lifecycle-process:2.6.1'
- implementation 'org.greenrobot:eventbus:3.2.0
- Significant effort was made during this release cycle in the following areas:
- Further enhancements to 3rd party developer experiences.
- Continued removal of deprecated features per the deprecation schedule.
- Highlighted new areas to be deprecated in future releases.
- Better documentation of the API.
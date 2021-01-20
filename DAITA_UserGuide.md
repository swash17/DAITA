# Data Acquisition for Intersection and Traffic Applications (DAITA)

# User Guide

## Table of Contents
[Data Entry Interface Features](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#data-entry-interface-features)  
* [Time Settings and Recording Status](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#time-settings-and-recording-status)
* [File Saving and Output File Format](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#file-saving-and-output-file-format)
* [Vehicle Classifications](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#vehicle-classifications)
* [North Direction Designation and Street Naming](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#north-direction-designation-and-street-naming)
* [Vehicle Turning Movement Keys](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#vehicle-turning-movement-keys)

[Menu Commands](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#menu-commands) 
* [File Menu](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#file-menu)
* [Options Menu](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#options-menu)
* [Record Menu](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#record-menu)

[Product Support](https://github.com/swash17/DAITA/blob/main/DAITA_UserGuide.md#product-support)

## Data Entry Interface Features
### Time Settings and Recording Status
The upper right quadrant of the main form displays the current data recording start and end time settings, as well as the data saving interval.  It also displays a signal head that shows the current status of the data collection effort: red signal indicates no data recording in progress; yellow signal indicates a paused data recording session; green signal indicates data recording in progress; and a flashing yellow signal indicates a data recording session about to begin.

### File Saving and Output File Format
In the lower right quadrant of the main form are the file naming controls. The output filename edit box defaults to a file named count.txt, which by default will be saved in the same directory where the DAITA program was executed from.  This name can be changed by just clicking in the edit box and typing a new filename. The drive and/or directory where the file is saved can be changed by clicking on the Browse button directly below the filename edit box.  This will bring up a standard Save As dialog box, where the filename can also be changed, as well as the drive and/or directory.  Before starting a data recording session, the filename and the drive/directory should be set. Once the user selects Start from the Record menu, the program will open the output file and begin writing data to it. After the user selects Stop from the Record menu, the program will close the output file.

Although program execution is identical regardless of the origination drive or file saving drive, it is recommended that the program be run from a hard drive for optimal operation speed.

The saved output file will be in a tab-delimited format, suitable for direct importation into most spreadsheet and word processing programs.  The output file will contain the data collection background information and a summary of the movement volumes and vehicle classifications for each approach, aggregated by the predefined recording interval.

### Vehicle Classifications
The right side of the main form displays the currently selected vehicle classification categories, as well as their corresponding trigger keys. While recording, the user can select a vehicle classification other than the default by just pressing and releasing the corresponding trigger key and then pressing the appropriate turning movement key. This movement will then be recorded under the appropriate vehicle classification. After depressing a particular classification trigger key, the user can change the classification key by pressing a different one before pressing a movement key, or revert back to the default vehicle classification category by pressing the backspace key.

### North Direction Designation and Street Naming
A north arrow is displayed in the upper left quadrant of the main form, between the street name edit boxes.  Clicking on this arrow will rotate it.  Each click will rotate the arrow 90 degrees in a clockwise direction. This will adjust the orientation of the street names and the direction headings in the output file. This will allow the user to choose the most convenient location at an intersection for data collection or to easily adjust to a prerecorded video tape orientation.

Once the user has set the north direction, the streets can be named by just typing the appropriate names in the edit boxes.

Note: Once the data recording session has been started (by selecting Start under the Record menu), neither the street names nor the north direction designation can be changed.

### Vehicle Turning Movement Keys
There are 12 turning movement keys, three for each approach of a four-approach intersection. When a recording session is in progress, the user registers a vehicle movement by simply pressing the appropriate key on the keyboard, as indicated by the alphanumeric label on the screen key button, or by clicking on the button with a mouse or finger (for touch screens).

The total volumes for the current recording interval, inclusive of different vehicle classifications, are displayed next to the turning movement arrows. These volumes will reset to zero at the start of each new recording interval.

## Menu Commands
### File Menu
#### New (Ctrl+N)

Selection of this option will reset the program to start a new data collection effort. This includes setting any displayed volumes to zero, clearing the street names, and resetting the output filename to the default, count.txt.

#### Exit

Selection of this option will close the program window and exit.

### Options Menu
#### Movement Keys (F5)

Selection of this menu option will present a dialog box that allows the user to redefine the default keys assigned to the individual turning movements. This is facilitated by clicking on a movement key with the mouse and then pressing the new key to be used for this movement. Valid key labels consist of any alphanumeric key.  Upon pressing the OK button, the new key definition scheme will become the default. Clicking the Reset button will redefine the movement keys to RTY-UJM-VBN-CDE for southbound, westbound, northbound, and eastbound movements, respectively.

#### Vehicle Keys (F6)

Selection of this menu option will present a dialog box that allows the user to define the vehicle classification keys.  This is facilitated by clicking on a vehicle classification label with the mouse and then typing the new label to be used for this classification.  Valid key labels consist of any alphanumeric key.  The default vehicle classification is car.  This is the classification that is defined when no other classification is chosen for a vehicle movement. This can also be changed by just clicking in the edit box and typing a different name.  The classification labels that the user chooses are what get written in the output file. Only the classifications that get defined appear in the right side pane of the main form. Upon pressing the OK button, the new key definition scheme will become the default. Clicking the reset button will clear any defined classifications and reset the buttons to 1 - 0, as well as revert the default classification to car.  There are two options for which vehicle classifications can be collected:  for unique movements or for approaches only. If the user selects classifications for each movement, the output file will display the volumes for each vehicle classification for each movement. If the user selects classifications by approach only, the output file will display the volumes for the non-default vehicle classifications by approach only, while still displaying the volumes for each movement for the default vehicle classification. **Note:** When recording vehicle classifications by approach only, the volumes listed under the individual turning movement volumes are inclusive of all vehicles, including the volumes of other vehicle classifications listed separately.

The ability to define up to 11 custom vehicle classifications provides a lot of flexibility for various types of studies.  For example, passenger occupancy studies are easily facilitated by defining various vehicle occupancy categories such as SOV, HOV2, and HOV3+.

#### Times (F7)

The Times option will present a dialog box that allows the user to select the time interval over which data entry will occur.  If the Use Real Time checkbox is checked, the data collection times will be referenced to the system clock. If this box is not checked, an arbitrary set of times can be used.  This feature is most useful for performing data collection from pre-recorded video. Thus, the data collection times can be synchronized with the times during which the actual video recording was performed. When an arbitrary time base is being used, a pause feature will be enabled on the record menu. To resume data collection after selecting pause from the Record menu, just select resume from the Record menu.

The recording interval edit box allows the user to specify any integer minute length for a data saving frequency. This time length for a data saving frequency is also the time length for which the data will be aggregated.  Thus, for a saving frequency of every 15 minutes, the data will be aggregated into 15 minute totals.  Since the data is saved directly to disk, only the data collected during the current recording interval is stored in RAM; thus, there is almost no limit to the amount of data that can be collected during a recording session. A practical limitation of course is disk space.  But for typical recording interval lengths and sessions, it is inconceivable that a user would ever encounter memory or storage space limitations.

The record session length can span up to 24 hours. If the finish time is the same or before the start time, it is interpreted as the next day. For example, to record from 11 p.m. to 1 a.m., set the start time to “23:00:00” and the finish time to “1:00:00”.

### Record Menu
#### Start/Stop (F2)

If not using real time, just select the Start option to start the data collection, which will then start the clock in reference to the predefined data collection period. If using real time, selecting the Start option will do one of two things. If the clock time is earlier than the predefined start time for the recording interval, the signal head in the upper right quadrant of the main form will turn to a steady yellow. When the clock time reaches 10 seconds before the start time, the signal head will start flashing yellow.  After 10 seconds, the signal head will turn green, indicating that the user can start collecting data. If the clock time is later than the predefined start time, selecting this option will start the data collection session immediately.

To stop the data collection prior to reaching the end of the predefined stop time, just select the Stop option under the Record menu.  Keep in mind, however, that the data are only saved according to the defined recording interval. Thus, if the record interval is 15 minutes, and the recording session is stopped after 7 minutes, no data will be saved. If, for some reason, this is perceived as a potential problem, it is recommend to use shorter recording intervals. It is always easier to aggregate data than to disaggregate it.

#### Pause/Resume (F3)

If real time is not being used and the data collection needs to be paused for any reason, just select the Pause option.  This will halt the clock and not allow any user input. After pausing, this menu option will change to Resume. To continue the data collection, just select Resume.

## Product Support
If you have questions, comments, or suggestions about DAITA, please send them to Dr. Scott Washburn at:

	Email: swash@ce.ufl.edu
	Web: https://swash.essie.ufl.edu
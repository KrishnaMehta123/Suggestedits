---
title: Journey States (Editing Flow)
excerpt: Learn about different Journey States in CleverTap.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

This document provides information about different aspects of each Journey state in CleverTap. Each state has distinct characteristics that govern how and when users enter and move within the journey. 

The current status of the flow is displayed under the *Journeys* listing page.

<Image alt="Journey Status" align="center" border={true} src="https://files.readme.io/ad98ea96a56d25ab38da99d0994d393de59c2d0bd313992f57a4f92fb78fff63-Journey_States.png">
  Journey Status
</Image>

# Draft

The *Draft* state indicates that the journey is not published yet. You can still modify each and every component of the journey as per your use case before you publish the journey. 

* **Possible next actions**: Edit, Save, Publish, and Clone
* **Possible next states**: Scheduled and Running
* **User Entry**: User Entry does not happen.
* **User Movement**: User Movement does not happen.

# Scheduled

The *Scheduled* state indicates that the journey is set to go live at a future time but is not currently editable except for the *What* section.

* **Possible next actions**: Edit, Clone, Pause, and Stop
* **Possible next states**: Running, Paused, and Stopped
* **User Entry**: User Entry does not happen.
* **User Movement**: User Movement does not happen.
* **Type of Modifications**: *What* section, Provider for Email, SMS, or WhatsApp engagement nodes, and user distribution for IntelliNODE journey split in manual mode.

# Running

The *Running* state indicates that the journey is active and the users are executing actions as defined. The Journey remains non-editable except for the *What* section.

* **Possible next actions**: Edit, Clone, Pause, and Stop
* **Possible next states**: Paused, Stopped, and Completed
* **User Entry**: User Entry happens.
* **User Movement**: User Movement happens.
* **Type of Modifications**: *What* section, Provider for Email, SMS, or WhatsApp engagement nodes, and user distribution for IntelliNODE journey split in manual mode.

# Paused

The *Paused* state indicates that the already qualified users continue to move ahead in the journey. However, no new users will qualify for the journey until it resumes. The Journey remains non-editable except for the *What* section.

* **Possible next actions**: Edit, Clone, Pause, and Stop
* **Possible next states**: Running, Stopped, and Completed
* **User Entry**: User Entry does not happen.
* **User Movement**: User Movement happens.
* **Type of Modifications**: *What* section, Provider for Email, SMS, or WhatsApp engagement nodes, and user distribution for IntelliNODE journey split in manual mode.

# Stopped

The *Stopped* state indicates that the journey has been permanently deactivated. Users currently in the journey do not progress further, and actions are halted. These users systematically exit from the journey over a period of 30 to 60 days. The journey cannot be edited once stopped.

* **Possible next actions**: Clone
* **User Entry**: User Entry does not happen.
* **User Movement**: User Movement does not happen.

# Completed

The *Completed* state indicates that no new users will qualify for the journey, but the already qualified users continue to move ahead in it. The Journey remains non-editable except for the *What* section. It can move to this state if the journey timelines are reached or all the users have moved out of the journey after reaching the last node.

* **Possible next actions**: Clone, Stop
* **Possible next states**: Stopped
* **User Entry**: User Entry does not happen.
* **User Movement**: User Movement happens.
* **Type of Modifications**: *What* section, Provider for Email, SMS, or WhatsApp engagement nodes, and user distribution for IntelliNODE journey split in manual mode.

# Restricted

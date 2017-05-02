[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-FlexibleAdapter-green.svg?style=flat)](http://android-arsenal.com/details/1/2207)
[![Download](https://api.bintray.com/packages/davideas/maven/flexible-adapter/images/download.svg) ](https://bintray.com/davideas/maven/flexible-adapter/_latestVersion)
[![API](https://img.shields.io/badge/API-14%2B-green.svg?style=flat)](https://android-arsenal.com/api?level=14)
[![Licence](https://img.shields.io/badge/Licence-Apache2-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)
[![Methods and Size](https://img.shields.io/badge/Methods%20and%20Size-core:%201162%20|%20159%20KB-e91e63.svg)](http://www.methodscount.com/?lib=eu.davidea%3Aflexible-adapter%3A5.0.0-rc1)

# FlexibleAdapter

#### ANNOUNCEMENT: Important and Revolutionary changes are foreseen in v5.0.0. Please see [issues](https://github.com/davideas/FlexibleAdapter/issues) and [releases](https://github.com/davideas/FlexibleAdapter/releases).

###### Fast and versatile Adapter for your RecyclerView
- **NEW!** First release candidate: [v5.0.0-rc1](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-rc1) built on 2017.01.14
- If you come from previous versions, update your code following the Wiki page [Migrations](https://github.com/davideas/FlexibleAdapter/wiki/Migrations).

> When initially Android team introduced the RecyclerView widget, we had to implement a custom Adapter in several applications, again and again to provide the items for our views.<br/>
We didn't know how to add selection and to combine all the use cases in the same Adapter.
Since I created this library, it has become easy to configure how views will be displayed in a list, and now, nobody wants to use a ListView anymore.

The idea behind is to regroup multiple features in a unique library, without the need to customize and import several third libraries not compatible among them.

The FlexibleAdapter helps developers to simplify this process without worrying too much about the Adapter anymore. It's easy to extend, it has predefined logic for different situations and prevents common mistakes.<br/>
This library is configurable and it guides the developers to create a better user experience and now, even more with the new features.

#### Main features
* Simple item selection with ripple effect, Single & Multi selection mode.
* **NEW!** Customizable [FastScroller](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-FastScroller) with new features.
* Customizable divider item decoration.
* Add and Remove items with custom animations.
* Restore deleted items, **NEW** works with Expandable items too!
* Async [SearchFilter](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-Search-Filter) with Spannable text, **NEW** result list is animated. Works with sub items too!
* **NEW!** [High performance](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-Search-Filter#performance-result-when-animations-are-active) updates and filter on big list.
* **NEW!** Auto mapping multi view types with [Item interfaces](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-Item-Interfaces).
* **NEW!** Predefined [ViewHolders](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-ViewHolders) with callbacks.
* **NEW!** [Headers and Sections](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-Headers-and-Sections) with sticky behaviour fully clickable and collapsible, with elevation, transparency and automatic linkage!
* **NEW!** [Scrollable Headers and Footers](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-Scrollable-Headers-and-Footers) items that lay respectively at the top and at the bottom of the main items.
* **NEW!** Expandable items with _Selection Coherence_ and multi-level expansion.
* **NEW!** [Drag&Drop and Swipe-To-Dismiss](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-Drag&Drop-and-Swipe#swiping-the-front-view) with Leave-Behind pattern and with _Selection Coherence_.
* **NEW!** Customizable scrolling animations based on adapter position and beyond.
* **NEW!** Innovative [EndlessScroll](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-On-Load-More) (_No OnScrollListener_).
* **NEW!** UndoHelper &amp; [ActionModeHelper](https://github.com/davideas/FlexibleAdapter/wiki/5.x-%7C-ActionModeHelper).
* **NEW!** Supports third LayoutManagers.
* **NEW!** DrawableUtils for dynamic backgrounds with ripple (_No XML_).
* **NEW!** Easy runtime position calculation for adding/moving items in sections.
* **NEW!** [Wiki](https://github.com/davideas/FlexibleAdapter/wiki/) pages documentation.

#### Extensions
* **NEW!** Data Binding.

# Setup
```
#### build.gradle
repositories {
	jcenter()
	maven {url = "https://oss.sonatype.org/content/repositories/snapshots/" } //For Snapshots
}
```
```
dependencies {
	// Using JCenter
	compile 'eu.davidea:flexible-adapter:5.0.0-rc1'
	
	// Using MavenSnapshots repository for continuous updates from my development
	compile 'eu.davidea:flexible-adapter:5.0.0-SNAPSHOT'
}
```
#### Stay Updated
<a href='https://bintray.com/davideas/maven/flexible-adapter?source=watch' alt='Get automatic notifications about new "flexible-adapter" versions'><img src='https://www.bintray.com/docs/images/bintray_badge_color.png'></a>

# Wiki!
I strongly recommend to read the **new [Wiki](https://github.com/davideas/FlexibleAdapter/wiki) pages**, where you can find a comprehensive Tutorial*.<br/>
Wiki pages have been completely reviewed to support all the coming features of version 5.0.0.

\* = _Pages are under heavy revision, working in progress_ :-)

#### Pull requests / Issues / Improvement requests
Feel free to contribute and ask!<br/>
Active discussions:
- [The next steps of your development](https://github.com/davideas/FlexibleAdapter/issues/224).
- [Snapshots and Pre-Releases for FlexibleAdapter v5.0.0](https://github.com/davideas/FlexibleAdapter/issues/39).
- [Documentation](https://github.com/davideas/FlexibleAdapter/issues/120).

#### Under the hood
Some simple features have been implemented, thanks to some Blogs (see at the bottom of the page), merged and methods have been improved for speed and scalability.

* At lower level there is `SelectableAdapter` class. It provides selection features and it's able to _maintain the state_ after the rotation: you just need to call the onSave/onRestore methods from the Activity!
* At middle level, the `AnimatorAdapter` class has been added to give some animation at startup and when user scrolls.
* At front level, the core class `FlexibleAdapter`. It holds and handles the main list, performs actions on all different types of item paying attention at the adding and removal of the items, as well as the new concept of "selection coherence".
* New useful extensions and helpers have been added during the time to simplify the development.
* Item interfaces and predefined ViewHolders complete the whole library giving more actions to the items and configuration options to the developers and the end user.

# Showcase of the demo App
You can download the latest demo App from the latest release page OR run it with the emulator.

![Drag Grid & Overall](/screenshots/drag_grid_overall.png)
![Secondary Functionalities](/screenshots/secondary_functionalities.png)
![StickyHeaders & EndlessScrolling](/screenshots/sticky_headers.png)

![Multi Selection & SC](/screenshots/multi_selection_sc.png)
![Undo](/screenshots/undo_single_selection.png)
![Drag Linear](/screenshots/drag_linear.png)

![Search](/screenshots/search_sections.png)
![swipe-to-dismiss1](/screenshots/swipe-to-dismiss1.png)
![swipe-to-dismiss2](/screenshots/swipe-to-dismiss2.png)

![Adapter Animations](/screenshots/adapter_animations.png)
![Dynamic Sections](/screenshots/dynamic_sections.png)
![Staggered Layout](/screenshots/dynamic_staggered_layout.png)

# Change Log
###### Latest release
[v5.0.0-rc1](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-rc1) - 2017.01.14

###### Old releases
[v5.0.0-b8](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b8) - 2016.09.17 |
[v5.0.0-b7](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b7) - 2016.06.20 |
[v5.0.0-b6](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b6) - 2016.05.01 |
[v5.0.0-b5](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b5) - 2016.04.04<br/>
[v5.0.0-b4](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b4) - 2016.02.21 |
[v5.0.0-b3](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b3) - 2016.02.08 |
[v5.0.0-b2](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b2) - 2016.01.31 |
[v5.0.0-b1](https://github.com/davideas/FlexibleAdapter/releases/tag/5.0.0-b1) - 2016.01.03<br/>
[v4.2.0](https://github.com/davideas/FlexibleAdapter/releases/tag/4.2.0) - 2015.12.12 |
[v4.1.0](https://github.com/davideas/FlexibleAdapter/releases/tag/4.1.0) - 2015.11.29 |
[v4.0.1](https://github.com/davideas/FlexibleAdapter/releases/tag/4.0.1) - 2015.11.01 |
[v4.0.0](https://github.com/davideas/FlexibleAdapter/releases/tag/4.0.0) - 2015.10.18<br/>
[v3.1](https://github.com/davideas/FlexibleAdapter/releases/tag/v3.1) - 2015.08.18 |
[v3.0](https://github.com/davideas/FlexibleAdapter/releases/tag/v3.0) - 2015.07.29 |
[v2.2](https://github.com/davideas/FlexibleAdapter/releases/tag/v2.2) - 2015.07.20 |
[v2.1](https://github.com/davideas/FlexibleAdapter/releases/tag/v2.1) - 2015.07.03 |
[v2.0](https://github.com/davideas/FlexibleAdapter/releases/tag/v2.0) - 2015.06.19 |
[v1.0](https://github.com/davideas/FlexibleAdapter/releases/tag/v1.0) - 2015.05.03

# Limitations
Item half swipe cannot be implemented due to how the `android.support.v7.widget.helper.ItemTouchHelper` is done, also clicks on rear view are not possible, same reason.
Half swipe can be done with others means, please see issues #98 and #100. See also commits of Apr 25, 2016. 

# Thanks
I've used these blogs as starting point:
- http://enoent.fr/blog/2015/01/18/recyclerview-basics/
- https://www.grokkingandroid.com/statelistdrawables-for-recyclerview-selection/

Special thanks goes to
- Martin Guillon ([Akylas](https://github.com/Akylas)) to have contributed at the development of the new technique for the Sticky Header.
- [Arpinca](https://github.com/arpinca) who added new features for FastScroller like _autoHide_ and _ignoreTouchesOutsideHandle_ and more.

# Imported libraries
- The library [LollipopContactsRecyclerViewFastScroller](https://github.com/AndroidDeveloperLB/LollipopContactsRecyclerViewFastScroller) has been imported, improved and adapted to work in conjunction with `AnimatorAdapter`.
- The library [sticky-headers-recyclerview](https://github.com/timehop/sticky-headers-recyclerview) was initially imported, then it was removed in favor of the new technique able to manage a real _View_ and so to handle the click events.

# Apps that use this Adapter
It will be a pleasure to add your App here, once it is published.

[Module.org](https://play.google.com/store/apps/details?id=org.module.app) |
[Socio - Shake and Connect!](https://play.google.com/store/apps/details?id=com.atsocio.socio) |
[Shibagram](https://play.google.com/store/apps/details?id=com.apripachkin.shibagram) |
[BNVR Client](https://play.google.com/store/apps/details?id=ru.beward.bnvr)

# License

#### FlexibleAdapter

    Copyright 2015-2017 Davide Steduto

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

#### FastScroller

    Copyright 2016-2017 AndroidDeveloperLB, Davide Steduto & Arpinca

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
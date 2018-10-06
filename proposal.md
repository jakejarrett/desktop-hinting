# Desktop Hinting for Linux Desktop Environments

## Problem
As a developer, it is hard to develop nice UI features (transparency & blur support etc) into applications without building against some wide assumptions (EG/ all DE's support that feature, that ONLY kde supports that feature or that your users only use KDE with those specific features enabled / supported)

## Solution
An interface that works across all systems so that developers can develop against a more concrete API while DE developers can incrementally introduce features etc.

### Proposed API

### org.desktop.hints

#### Properties
* Supports
	**String[]**
	`Read only`
	***
	**`List of features that are supported by the current DE`**
	* Example return value
	`"gaussian blur","launcher api","transparency","client side decorations"`

* CurrentEnvironment
	**String**
	`Read Only`
	***
	**`Lists the current setup (DE, WM & versions)`**
	* Example return value
	`"Gnome:3.30;Mutter:3.30"`

* Disabled
	**String[]**
	`Read Only`
	***
	**`System/Desktop Environment explicitly disabled this value`**
	* Example return value
	`"appindicators"`

* UserDisabled
	**String[]**
	`Read Only`
	***
	**`User explicitly disabled this value`**
	* Example return value
	`"client side decorations"`

##### Possible properties, these are just ideas

* Experimental
	**String[]**
	`Read Only`
	***
	**`Exposed for building against experimental features`**
	* Example return value
	`"wobbly windows","clicking a button causes kernel panic"`

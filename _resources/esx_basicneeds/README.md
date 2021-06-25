<<<<<<< HEAD
# esx_status
ESX Status
[INSTALLATION]

1) CD in your resources/[esx] folder
2) Clone the repository
```
git clone https://github.com/ESX-Org/esx_status esx_status
```
3) Import esx_status.sql in your database
4) Add this in your server.cfg :

```
start esx_status
```

[HOWTO]

server.lua
```lua

local name    = 'hunger'
local default = 1000000
local color   = '#CFAD0F'

TriggerEvent('esx_status:registerStatus', name, default, color, 
	function(status) -- Visible calllback, if it return true the status will be visible
		return true
	end,
	function(status) -- Tick callback, what to do at each tick
		status.remove(200)
	end,
	{remove = 200} -- Client action (add / remove) so the client can be in sync with server
)


```
=======
# esx_basicneeds
This script implements hunger and thirst status, they can be increased when eating bread or drinking water.

## Requirements
- [esx_status](https://github.com/ESX-Org/esx_status)

## Download & Installation

### Using [fvm](https://github.com/qlaffont/fvm-installer)
```
fvm install --save --folder=esx esx-org/esx_basicneeds
```

### Using Git
```
cd resources
git clone https://github.com/ESX-Org/esx_basicneeds [esx]/esx_basicneeds
```

### Manually
- Download https://github.com/ESX-Org/esx_basicneeds/archive/master.zip
- Put it in the `[esx]` directory


## Installation
- Import `esx_basicneeds.sql` in your database
- Add this in your server.cfg :

```
start esx_basicneeds
```

# Legal
### License
esx_basicneeds - thirst and hunger system

Copyright (C) 2015-2020 Jérémie N'gadi

This program Is free software: you can redistribute it And/Or modify it under the terms Of the GNU General Public License As published by the Free Software Foundation, either version 3 Of the License, Or (at your option) any later version.

This program Is distributed In the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty Of MERCHANTABILITY Or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License For more details.

You should have received a copy Of the GNU General Public License along with this program. If Not, see http://www.gnu.org/licenses/.
>>>>>>> esx_basicneeds/master
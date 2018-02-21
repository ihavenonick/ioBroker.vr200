![Logo](admin/VR200.png)
# ioBroker.vr200
This is a full fork of botvac adapter. Only difference is to use the corrosponding node-kobold module.
Im not the Author of the adapter. The full respect is giving to Pmant.

## Installation
- Install the adapter
- fill in your Vorwerk user credentials
- if needed change the poll interval (60 is minimum)

## Usage
- use the states in the commands channel to control your VR200
- use the can* states in the status channel to see which commands are valid
- all states in the status channel are read-only

## Examples
### clean in eco mode
- check if status.canStart is ```true```
- set commands.eco to ```true```
- set commands.clean to ```true```

### clean a 150cm * 150cm spot
- place the VR200 in front of the desired location
- check if status.canStart is ```true```
- set commands.spotHeight and commands.spotWidth to ```150``` 
- set commands.cleanSpot to ```true```

### return to base
- status.dockHasBeenSeen has to be ```true```
- VR200 has to be in paused or stopped state (commands.stop / commands.pause)
- set commands.goToBase to ```true```

## Changelog

### 0.1.0
- (Eisbaeeer) inital commit from Pmant�s adapter

## License
The MIT License (MIT)

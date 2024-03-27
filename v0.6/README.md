# WinchRack v0.6
Motor powered standalone spool rewinder for Annex Tradrack

Operates at 5 volt. (Can use 5v pin on control board or external power source)

just 5 voltage, nothing else required.

![image](https://github.com/v6cl/WinchRack/assets/16078263/c94f0b1d-32d0-4daa-8e72-0be90596ac8d)

![image](https://github.com/v6cl/WinchRack/assets/16078263/11d83d9b-03ac-4441-8721-6844db9099bf)


## BOM

Wago 3pin x 2

n20 gear motor 300 rpm 5v ~ 6v x  1 

ls-p20/15 3kg x 2 

623zz x 5

silicon ring x 1 (https://zrr.kr/E5Dk)

PTFE tube 3x4 or 2x4 

m3 insert nut (OD 5mm, L 4mm)

m3 bolts 

m4 bolt 10mm x 2 (For ls-p20/15)

m2 self tapping screw 10mm x 2

6mm collet for 4mm PTFE Tube x 1 (https://zrr.kr/7WdG)

D2F-L Micro switch 

## Tradrack experiment function for rewinder branch

for resolve exception situation.

On ssh teriminal

```
cd ~
./trad_rack_klippy_module/Klipper_Stuff/klippy_module/install.sh
./trad_rack_klippy_module/Klipper_Stuff/klippy_module/install.sh rewinder-experiments
```

On Mainsail in moonraker.conf

```
[update_manager trad_rack]
type: git_repo
path: ~/trad_rack_klippy_module
origin: https://github.com/Annex-Engineering/TradRack.git
primary_branch: rewinder-experiments
managed_services: klipper
```

and [trad_rack] in trad_rack.cfg

```
selector_unload_length_extra: 4.0 # BufferRail_rev2.stl update
```

# unresolved problems

- Problem with new filament spools coming loose and tangling



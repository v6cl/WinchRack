# WinchRack v0.5
Motor powered standalone spool rewinder for Annex Tradrack

![image](https://github.com/v6cl/WinchRack/assets/16078263/adada34e-6afa-4bf0-a330-dc1c9d353933)

Operates at 5 volt. (Can use 5v pin on control board or external power source)

just 5 voltage, nothing else required.


## Test video

Visit https://www.youtube.com/watch?v=kO5R-0rNxZA

Visit https://www.youtube.com/shorts/trHfZH3sDRs


## BOM

Wago 5pin x 2

Opto endstop x 1 (https://zrr.kr/ZYrV)

n20 gear motor 300 rpm 5v ~ 6v x  1 (https://zrr.kr/aFPa)

ls-p20/15 3kg x 2 (https://zrr.kr/Rqkb)

mosfet switch 1ch x 1 (https://zrr.kr/TrOc)

608zz x 3

623zz x 8

silicon ring 13mm x 1 [link](https://ko.aliexpress.com/item/1005005445878990.html)

PTFE tube 3x4 or 2x4 

m3 insert nut (OD 5mm, L 4mm)

m3 bolts 

m4 bolt 15mm x 2 (For ls-p20/15)

m2 self tapping screw 8~10mm x 4

6mm collet for 4mm PTFE Tube x 1 [link](https://ko.aliexpress.com/item/4001119588533.html?pdp_npi=4%40dis%21KRW%21%E2%82%A9%20700%21%E2%82%A9%20659%21%21%210.51%210.48%21%402141113617075557439996244e6a34%2110000014544527050%21sh%21KR%21889811361%21&spm=a2g0o.store_pc_allItems_or_groupList.new_all_items_2007473650367.4001119588533&gatewayAdapt)

D2F Micro switch 

4mm Bearing ball (same tradrack bom)

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



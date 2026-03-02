# OAT 2020 + 50deg Print List

## Authoritative sources used
- `README.md` points to the **Printed Parts Chooser** as the official way to select printed parts.
- `changelog.md` records current/newer part revisions (notably RA motor mount v4 and pole v5), so newer matching variants were preferred.
- STL folder structure indicates variant split:
  - `STL/All latitudes/` = common core parts
  - `STL/2020 Base/` = 2020 base-specific parts
  - `STL/50deg/` = 50-degree latitude parts

---

## Repo Map (STL + docs)
- Docs:
  - `README.md`
  - `changelog.md`
- Main STL folders:
  - `STL/All latitudes/`
  - `STL/50deg/`
  - `STL/2020 Base/`
  - `STL/Printed Base & Printed Camera mount/`
  - `STL/Universal mount/`

---

## REQUIRED

### RA assembly
- `STL/All latitudes/03_polemount_6801_v3.STL`
- `STL/All latitudes/05_pole_v5.STL`
- `STL/All latitudes/06_splitring_v9_singlePiece.STL`
- `STL/All latitudes/14_RAmotor_mount_NEMA_down_v4.STL`
- `STL/All latitudes/15_Pulley_GT2.STL`
- `STL/All latitudes/RA_BearingSupportx2.stl`

### DEC / camera axis and drive
- `STL/Printed Base & Printed Camera mount/07_camera_mount_left.STL`
- `STL/Printed Base & Printed Camera mount/08_camera_mount_right.STL`
- `STL/Printed Base & Printed Camera mount/10_drivedisc_DEC_timingbelt.STL`
- `STL/All latitudes/11_DEC_motor_mount_v11_NEMA.stl`
- `STL/All latitudes/11.1_DEC_idler_bracket_v1_NEMA.stl`

### Base / latitude wedge (2020 + 50deg)
- `STL/50deg/02_angle_50deg_v4_2020base.STL`
- `STL/50deg/04_rollmount left_50°_v6_2020base.STL`
- `STL/50deg/04_rollmount right_50°_v6_2020base.STL`
- `STL/2020 Base/M14_mount_left_2020base.STL`
- `STL/2020 Base/M14_mount_right_2020base.STL`
- `STL/2020 Base/M14_mount_rear_2020base_v4.STL`
- `STL/2020 Base/b1_connector_left.STL`
- `STL/2020 Base/b1_connector_right.STL`
- `STL/2020 Base/b3_2020 adapter.STL`

### Electronics enclosure
- `STL/2020 Base/16_NEMA_electronicsbox.STL`
- `STL/2020 Base/16_NEMA_electronicsbox_lid.STL`

---

## OPTIONAL (purpose)
- `STL/All latitudes/00_calibration.STL` — calibration/test piece before main prints.
- `STL/All latitudes/DEC_DistancingRing.stl` — DEC motor spacing shim if needed.
- `STL/All latitudes/DEC_StepperBoardClip.stl` — clip for DEC stepper board/cable management.
- `STL/All latitudes/05.2_stabilizer.STL` — added structural stabilization part for pole area.
- `STL/2020 Base/16_electronicsbox_bottom.STL` — alternate electronics box style (non-NEMA split design).
- `STL/2020 Base/16_electronicsbox_top_2020base.STL` — alternate top for non-NEMA box.
- `STL/2020 Base/16_electronicsbox_top_2020base_cat6.STL` — alternate top with CAT6 opening.
- `STL/2020 Base/b2_level holder_31mm.STL` — optional bubble-level holder, 31 mm variant.
- `STL/2020 Base/b2_level holder_60mm.STL` — optional bubble-level holder, 60 mm variant.
- `STL/2020 Base/b2_level holder_65mm.STL` — optional bubble-level holder, 65 mm variant.

---

## ALTERNATES / VARIANTS (selection rule)
- **Threaded-insert versions (`*_TI.STL`)** for matching parts in `STL/All latitudes/` and `STL/50deg/`.
  - Rule: choose `*_TI` only if your hardware plan uses heat-set threaded inserts.
- `STL/All latitudes/06a_splitring_part1_v4.STL` + `06b...` + `06c...`
  - Rule: use segmented ring instead of `06_splitring_v9_singlePiece.STL` if build volume is too small.
- `STL/All latitudes/For 200x200 printers/06a_splitring_part1_v4f_200x200.STL` and `06c_splitring_part3_v4f_200x200.STL`
  - Rule: use for 200x200 class printers where full-size ring parts do not fit.
- `STL/All latitudes/14_RAmotor_mount_NEMA_down_SngleRAring_v4.STL`
  - Rule: use only with the **single ring-specific** RA configuration stated in filename.
- `STL/All latitudes/14_RAmotor_mount_low_v4.STL` / `14_RAmotor_mount_v5.STL`
  - Rule: legacy/other pulley geometry; default to `NEMA_down_v4` per latest changelog note.
- `STL/All latitudes/11_DEC_motor_mount_v9_NEMA.STL` / `11_DEC_motor_mount_v7.STL` / `11_DEC_motor_mount_v8_low.STL` / `11_DEC_motor_strong_mount_w_idlers_NEMA.STL`
  - Rule: legacy or alternate DEC motor mount families; default to latest `v11_NEMA` path.
- `STL/Printed Base & Printed Camera mount/07_camera_mount_left_biglens.STL` and `08_camera_mount_right_biglens.STL`
  - Rule: choose for large-diameter lenses.
- `STL/Printed Base & Printed Camera mount/07_camera_mount_left_guidescope.STL` and `08_camera_mount_right_guidescope.STL`
  - Rule: choose when integrating a guidescope camera mount configuration.
- `STL/50deg/04_rollmount left_50°_v6_2020base_TI.STL` and `...right..._TI.STL`
  - Rule: choose TI versions if using threaded inserts in rollmounts.

---

## Print Queue (recommended order)
1. `STL/All latitudes/00_calibration.STL` (optional validation)
2. Structural base parts (`STL/2020 Base/b3_2020 adapter.STL`, `b1_connector_left/right`, `M14_mount_left/right/rear_2020base_v4`)
3. Latitude wedge (`STL/50deg/02_angle_50deg_v4_2020base.STL`, then left/right rollmounts)
4. RA structure (`03_polemount_6801_v3`, `05_pole_v5`, `RA_BearingSupportx2`)
5. RA drive (`06_splitring_v9_singlePiece`, `14_RAmotor_mount_NEMA_down_v4`, `15_Pulley_GT2`)
6. DEC/camera axis (`07_camera_mount_left`, `08_camera_mount_right`, `10_drivedisc_DEC_timingbelt`)
7. DEC motor/idler (`11_DEC_motor_mount_v11_NEMA`, `11.1_DEC_idler_bracket_v1_NEMA`, optional `DEC_DistancingRing`)
8. Electronics enclosure (`16_NEMA_electronicsbox`, `16_NEMA_electronicsbox_lid`, optional clips/level holder)

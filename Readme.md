This repo is a fork of m-weigand's custom linux kernel for the pinenote intended for testing tweaks and added features. Novel branches so far:

* **tunable_2bit_thresholds** -- clone of branch_pinenote_6-3-10_v1 with modifications to allow changing thresholds for 4 tone grayscale mode (bw_mode = 3) via module parameters.


# Description of new branches and merge order

## Branches

* (pinenote_6-2_v3)[https://github.com/m-weigand/linux/tree/pinenote_6-2_v3] --
  Kernel 6.2 with patches applied to work on the Pinenote. See section below
  for a list of merged branches
* **mw/rk35/pinenote-next-t1** -- Contains all changes merged into one branch
  that can be used on the Pinenote.
* **mw/rk35/ebc-drm-v5-modifications-t1** -- Changes to the rockchip_ebc driver
  controlling the Pinenote epd display
* **mw/rk35/pinenote-defconfig-changes** -- Changes to the Pinenote defconfig tree
* **mw/rk35/pinenote_dts_changes** -- Changes to the Pinenote device tree
* **mw/rk35/rk356x-rga** -- Changes to the RGA V4L2 driver for the rockchip-rga of
  the Pinenote. The RGA can be used to convert RGB images to Y4 grayscale for
  the EPD display. It also supports dithering to monochrome colors.
* [mw/rk35/tps65185](https://github.com/m-weigand/linux/tree/mw/rk35/tps65185) -- some fixes/additions to the tps65185 epd pmic driver, mostly related to resume/suspend
* [lm3630a](https://github.com/m-weigand/linux/tree/lm3630a) Small fixes to the lm3630a backlight led driver

* **master**: this is the main branch forked from torvalds/linux

## Kernel 6.2

The Kernel 6.2 branch,
(pinenote_6-2_v3)[https://github.com/m-weigand/linux/tree/pinenote_6-2_v3],
consists of a vanilla mainline 6.2 kernel with the following branches merged
in:

	* branch_rebase_6.2_rk_suspend_driver (rockchip suspend driver required for proper suspend/resume)
	* branch_rebase_6.2_pn_dts_v2 (dts changes for the PineNote)
	* branch_rebase_6.2_cyttsp5 (changes to the touchscreen driver)
	* branch_rebase_6.2_tps65185 (driver for the ebc pmic)
	* branch_rebase_6.2_ebc (driver for the ebc display driver)
	* branch_rebase_6.2_defconfig (defconfig for the Pinenote)
	* branch_rebase_6.2_lm3630a (modifications of the backlight driver)

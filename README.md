This fork is for improving Ardour's integration with certain controllers and synthesizers; starting with the [Yamaha MX (49/61/88)](share/patchfiles/Yamaha_MX-49-61-88.midnam).

Compared to the version in master, this midnam file offers the following:
- All patch banks and patches are implemented. Add Peformance, User Voice and User Drum banks.
  - Add Performance names for all presets (e.g. `[001] MXCategory`). The Performance Number is provided since user performances overwrite these slots. The number can be referenced against the MX panel if the name is wrong.
  - Voice names look like `[ORG|TnWhl] Draw Organ`. All Voice names are the 10 character MX version. The category prefix is whitespace-padded, which may turn out to be inconveniently long.
  - Several corrections to the voice descriptions. Some had incorrect categories, and one drum kit (Wacko Kit) had an XS name that the MX doesn't have (the Guitar/Bass FX Kit).
  - All patch changes lovingly tested against my MX88, leading to a few corrections in the GM bank.
- All CCs implemented with useful names (`Cutoff`, `Reverb`, etc) and automation-friendly.
- Author credit stolen by me.


Current TODOs:
- Write a reduced ControlNameList with only the implemented controls.
  - Use the short list by default, but keep the old one, for those not into the whole brevity thing.
- Bring back PatchNameLists that use the longer (and comprehensible) MOTIF XS voice names. Banks could then point to either the XS or MX version of the voice names.

Extra extra credit:
Get the Ardour Patch Selector to expand the text field on the buttons when the dialog is resized.


Please see the [Ardour web site](https://ardour.org) for all information about Ardour.

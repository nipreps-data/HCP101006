# HCP-BIDS: Participant 101006

This dataset contains a partial conversion of the Human Connectome Project
subject 101006 to the BIDS format, for use in testing BIDS-compatible
processing pipelines

## Notes

This dataset was largely curated by hand.

The phase-encoding directions in the filenames are inconsistent with the data.
All files are LAS-oriented, and files with `dir-LR` in the data have
`PhaseEncodingDirection` of `"i"` instead of `"i-"`.
Examining the data, the images are right-to-left encoded (that is, there is
visible compression on the right hemisphere and spread in the left), so `"i"`
is correct, but `LR` is misleading.
However, `LR` is how the data are labeled in the original HCP data, so for
consistency in identifying original and resulting files, we preserve this
mislabeling.

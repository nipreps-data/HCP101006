# HCP-BIDS: Participant 101006

This dataset contains a partial conversion of the Human Connectome Project
subject 101006 to the BIDS format, for use in testing BIDS-compatible
processing pipelines

## Notes

This dataset was largely curated by hand.

### August 7, 2023
The phase-encoding directions have been reverted back to the original after
some discussion ([nipreps/sdcflows#376](https://github.com/nipreps/sdcflows/issues/376)).

See changes on commit [`9511f69`](https://github.com/nipreps-data/HCP101006/commit/9511f69b1e508564feaf4a53f0e94bf4ca98b1e7).

The labeling discussed below seems to come from Siemens' naming of the phase encode parameter.

### March 20, 2023
The phase-encoding directions in the filenames are inconsistent with the data.
All files are LAS-oriented, and files with `dir-LR` in the data have
`PhaseEncodingDirection` of `"i"` instead of `"i-"`.
Examining the data, the images are right-to-left encoded (that is, there is
visible compression on the right hemisphere and spread in the left), so `"i"`
is correct, but `LR` is misleading.
However, `LR` is how the data are labeled in the original HCP data, so for
consistency in identifying original and resulting files, we preserve this
mislabeling.

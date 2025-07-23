---
permalink: /markdown/
title: "Learn Along the Way"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

{% include toc %}

## Import BioSemi 32-channel EEG electrode locations to EEGLab

The definition of channel locations for BioSemi EEG systems can be downloaded [here](https://sccn.ucsd.edu/eeglab/download/BIOSEMI_cap_coords_all.xls).

On the official EEGLab tutorials, we can see a list of supported formats for channel locations at this [link](https://eeglab.org/tutorials/04_Import/Channel_Locations.html).

We decided to use a spherical coordinates file (.sph) as the BioSemi document is providing the values in the same format as EEGLab wants it. The provided format is specified as in the table below.

| #   | Azimut  | Horiz. | Label |
|-----|---------|--------|-------|
| 1   | -63.36  | -72    | Fp1   |
| 2   | 63.36   | 72     | Fp2   |
| 3   | 32.58   | 0      | C3    |
| 4   | 32.58   | 0      | C4    |

**Note** that when generating this file, you should not include the header line into the file and on each line, the contents should be separated by tab.

> The `Azimut` column is corresponding to the `sph_theta` column in the BioSemi definition file and the `Horiz.` is corresponding to the `sph_phi` column in the BioSemi definition file. There is no need for a conversion. 

[32-channels .ced file](/files/biosemi_32-channels.ced)
[32-channels .sph file](/files/biosemi_32-channels.sph)


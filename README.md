# Fibers 3D — Paris 4 sample

Media for the draft VC3D feature PR, captured on macOS arm64 from feature commit `8fcfd24c01a635f7ee0c6cb9c7b81f0c2370be4a` on 26 October 2026.

[Download the screenshot/video AFV](https://dl.ash2txt.org/community-uploads/qual/AutomatedFiberVolumes/Paris4_1mm_v2_sample.afv). File identity and coordinate provenance: [input.json](input.json).

The 43-second, 1920 × 1080, 60 fps demo starts with a ten-second continuous overview of all 364,708 fibers in the sample. It uses VC3D's geometry/shaders/palettes with export-only camera, filter and color interpolation. The remainder is rendered from the real VC3D widgets, including the CT, public surface and Line Annotation. The screenshot frames are native application captures. Loading waits are omitted; this is not a benchmark of interactive loading speed. No generated imagery is used.

Source coordinates remain unchanged. The public surface is a contiguous 5.0162 cm² crop of `20231221180251`, registered to the Paris 4 scan; display cropping is not reconstruction.

The sample is a 4,000-native-voxel central Z crop of an AFV filtered to fibers >1 mm and simplified with a maximum deviation of 0.25 native voxels. Crop boundary fragments may be shorter than 1 mm. The native CT frame is `PHercParis4/20230205180739` at 7.91 µm.

`tests.txt` records nine passing focused suites. `validation.txt` describes a separate full-collection regression run, not the screenshot sample. `source-sha256.json` records the feature files verified against the Mac build.

No ink inference or source-fiber editing was performed.

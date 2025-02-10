---
layout: default
title: "Results"
comments: true
---

# <span style="color:black"> Results </span>

## From Visual Stimulus to BOLD 

| ![](/figures/barMap.png){width="300px" align=center}|
|:--:|
|**Figure 1. Input for BOLD simulation.** [Drifting bar](https://drive.google.com/file/d/14MRGpbjya8KwtLup8kAvR8EmKF5svNSr/view?usp=sharing) (original resolution from mrVista parameter files was 768 x 768) was downsampled to 64 x 64 pixels. .|


| ![](/figures/stHRF_BOLD_sim_cortex.png){width="600px" align=center}|
|:--:|
|**Figure 2. Cortical BOLD response.** Flattened cortical reconstruction showing  [cortical hemodynamic responses to the drifting bar](https://drive.google.com/file/d/17JkrsSYfcZkWn2gZsGGb1wURvY_gLqTL/view?usp=sharing) stimuli commonly used in pRF mapping (depicted on a flattened cortical reconstruction using the Freesurfer's *fsaverage*  template) and visual cortical maps V1, V2 and V3 (black outlines). Within each of these maps, nearby neurons respond to nearby locations in the visual image, with this property (receptive fields) extending along cortical hierarchy. Neuronal responses across cortical sites were approximated using a mean field approximation of retino-cortical inputs, resulting on stimuli-dependent estimates for the neuronal drive in V1, V2 and V3. These estimates are then translated to BOLD activity using an empirically established spatiotemporal hemodynamic response function (st-HRF).|


## The Human Foveal Confluence

|![](/figures/retMaps_bandedDoubleSech.png){width="900px" align=center}|
|:--:|
|**Figure 3. V1, V2 and V3 sites cluster around the foveal confluence.**  For V1, V2 and V3, left and right halves of the visual field project to opposite cortical hemispheres, with visual field selectivity inverted across the horizontal meridian. Furthermore, V2 and V3 are split into dorsal and ventral quarter-fields, each containing an inverted representation of the upper and lower visual field. The organization of early visual cortical maps V1, V2 and V3 cluster around a single foveal representation can be described using an banded 2D model that accounts for retinotopy, cortical magnification and anisotropy.|



## Hemodynamic Waves

|![](/figures/tSeries_bandedDoubleSech.png){width="600px" align=center}|
|:--:|
|**Figure 4. Simulated BOLD time series obtained using the st-HRF.**|


| ![](/figures/stHRF_BOLD_sim_bandedDoubleSech.png){width="600px" align=center}|
|:--:|
|**Figure 5. Simulated BOLD time series projected onto the banded-DoubleSech model of the V1-V2-V3.** Hemodynamic  [wave-like responses to the drifting bar](https://drive.google.com/file/d/13tFxnNaqPVHgYauDXN5xiREETby12mkx/view?usp=sharing) stimuli unfold across the V1-V2-V3 hierarchy by following inter-areal homotopy.|

## <span style="color:lightblue">Discussion📜</span>


```{disqus}
```

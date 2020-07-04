# ChromaCode: A Fully Imperceptible Screen-Camera Communication System

## Overview

Hidden screen-camera communication techniques emerge as a new paradigm that embeds data imperceptibly into regular videos while remaining unobtrusive to human viewers. Three key goals on imperceptible, high rate, and reliable communication are desirable but conflicting, and existing solutions usually made a trade-off among them. 
In this paper, we present the design and implementation of ChromaCode, a screen-camera communication system that achieves all three goals simultaneously. 
In our design, we consider for the first time color space for perceptually uniform lightness modifications. 
On this basis, we design an outcome-based adaptive embedding scheme, which adapts to both pixel lightness and regional texture. 
Last, we propose a concatenated code scheme for robust coding and devise multiple techniques to overcome various screen-camera channel errors. 
Our prototype and experiments demonstrate that ChromaCode achieves remarkable raw throughputs of >700 kbps, data goodputs of 120 kbps with BER of 0.05, and with fully imperceptible flicker for viewing proved by user study, which significantly outperforms previous works.

## Paper

[ChromaCode: A Fully Imperceptible Screen-Camera Communication System](https://doi.org/10.1145/3241539.3241543)

Kai Zhang*, Chenshu Wu*, Chaofan Yang, Yi Zhao, 
Kehong Huang, Chunyi Peng, Yunhao Liu, Zheng Yang  (*: co-primary authors)

[ACM International Conference on Mobile Computing and Networking (MobiCom), 2018](http://www.sigmobile.org/mobicom/2018)

[[PDF]](com022-zhangA.pdf) [[Video]](https://youtu.be/WmkyRoM4Ja4) [[PPT]](ChromaCode_PPT.pptx)

## Materials

In the following, we provide the high resolution versions of several figures (Figure 3) in the paper for better viewing. 

### Impact of color space

The below figures depict the user-perceptual uniformity under HSL, a non-uniform color space, and CIELAB, a uniform color space respectively. 
In the first two figures (Hue palettes), the original colors (middle of the each sector) are of the same saturation (100%) and lightness (50%), but are different in hue ranging from 0 to 300. 
For each original color, we increase and decrease the lightness (outer and inner sector) by the same amount
(∆L = 4%). 
As seen, given the same lightness changes, the resulted color differences are considerably more uniform (meaning that the perceptually color changes are more close under the same amount of lightness changes) in
CIELAB space, regardless of the hue values. 
Similar results can be observed in the later two figures (Lightness palettes) where we keep hue (120) and
saturation (100%) unchanged and alter lightness dimension from 10% to 90%.

<table align="center">
  <tr>
    <td><img src="images/hue_plate_hsl.png" width="300"/></td>
    <td><img src="images/hue_plate_lab.png" width="300"/></td>
  </tr>
  <tr>
    <td align="center">Hue palette in HSL color space<a href="images/hue_plate_hsl.pdf">[PDF]</a></td>
    <td align="center">Hue palette in LAB color space with CIEDE2000<a href="images/hue_plate_lab.pdf">[PDF]</a></td>    
  </tr>
</table>

<table align="center">
  <tr>
    <td><img src="images/lightness_plate_hsl.png" width="300"/></td>
    <td><img src="images/lightness_plate_lab.png" width="300"/></td>
  </tr>
  <tr>
    <td align="center">Lightness palette in HSL color space<a href="images/lightness_plate_hsl.pdf">[PDF]</a></td>
    <td align="center">Lightness palette in LAB color space with CIEDE2000<a href="images/lightness_plate_lab.pdf">[PDF]</a></td>    
  </tr>
</table>


### Impact of texture

The below shows the impacts of video texture on perceptual lightness changes. 
As seen, smooth regions usually expose noticeable flicker more easily while textured regions help hide flicker.

<table align="center">
  <tr>
    <td><img src="images/texture_plate.png" width="300"/></td>
  </tr>
  <tr>
    <td align="center">Texture plate<a href="images/texture_plate.pdf">[PDF]</a></td>
  </tr>
</table>

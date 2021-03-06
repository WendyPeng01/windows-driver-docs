---
title: Prediction Planes
description: Prediction Planes
ms.assetid: 967d52d1-c4e1-4a81-a1ad-40a09040c3a8
keywords: ["decoding video WDK DirectX VA , macroblock prediction", "video decoding WDK DirectX VA , macroblock prediction", "prediction planes WDK DirectX VA", "macroblocks WDK DirectX VA , prediction"]
---

# Prediction Planes


## <span id="ddk_prediction_planes_gg"></span><span id="DDK_PREDICTION_PLANES_GG"></span>


The following figure illustrates the conceptual macroblock prediction planes that exist prior to forming the final prediction.

![diagram illustrating plane example for field macroblock prediction](images/m2planes.png)

MPEG-2 has two planes: forward and backward (bidirectional prediction), or same-parity and opposite-parity (dual-prime). The forward reference plane consists of blocks from the closest previous I or P picture. The backward reference plane consists of blocks from the closest future I or P picture.

In the cases of MPEG-1 and MPEG-2, prediction planes are combined by averaging between the corresponding block pixel values of the two prediction planes and rounding each up to the nearest integer. More sophisticated prediction schemes, such as H.263's overlapped block motion compensated (OBMC) prediction, have three planes.

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20[display\display]:%20Prediction%20Planes%20%20RELEASE:%20%282/10/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





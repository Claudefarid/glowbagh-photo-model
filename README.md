# MobileNet v2 for Glowbagh photo search

Unchanged copy of Google's **MobileNet V2 (100%, 224×224) image classification model, version 2**, in
TensorFlow.js graph-model format, as published on TensorFlow Hub / Kaggle Models
(`google/imagenet/mobilenet_v2_100_224/classification/2`).

It is served from jsDelivr so the photo search on [glowbagh.com](https://glowbagh.com) loads it quickly
in Bangladesh:

    https://cdn.jsdelivr.net/gh/Claudefarid/glowbagh-photo-model@v2/fp16/model.json   (used, 7 MB)
    https://cdn.jsdelivr.net/gh/Claudefarid/glowbagh-photo-model@v1/model.json        (original, 14 MB)

`fp16/` is the same model with its weights stored as float16 (TF.js dequantizes them on load):
half the download. On 38 Glowbagh product photos its 1280-number embeddings match the original
at cosine 0.9999 on average (min 0.9994), and the nearest product is the same for all 38.

Licence: Apache License 2.0 (Google), see https://www.apache.org/licenses/LICENSE-2.0 and the model
page https://www.kaggle.com/models/google/mobilenet-v2. The files in the root are not modified; `fp16/` differs only in the stored precision of the weights.

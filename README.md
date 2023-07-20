1. Pull data to folder data

    panpp_focus
    └── data
        ├── CTW1500
        │   ├── train
        │   │   ├── text_image
        │   │   └── text_label_curve
        │   └── test
        │       ├── text_image
        │       └── text_label_curve
        ├── total_text
        │   ├── Images
        │   │   ├── Train
        │   │   └── Test
        │   └── Groundtruth
        │       ├── Polygon
        │       └── Rectangular
        ├── ICDAR2015
        │   └── Challenge4
        │       ├── ch4_training_images
        │       ├── ch4_training_localization_transcription_gt
        │       ├── ch4_test_images
        │       └── ch4_test_localization_transcription_gt
        ├── MSRA-TD500
        │   ├── train
        │   └── test
        ├── HUST-TR400
        ├── COCO-Text
        │   └── train2014
        ├── SynthText
        │   ├── 1
        │   ├── ...
        │   └── 200
        └── ICDAR2017-MLT
            ├── ch8_training_images
            ├── ch8_validation_images
            ├── ch8_training_localization_transcription_gt_v2
            └── ch8_validation_localization_transcription_gt_v2

2. Create conda anv

    Required: torch (latest) with cuda toolkit 11.8, mmcv==1.3.1

```shell
    pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

```shell
    pip install -U openmim
    mim install mmcv==1.3.1
```
3. Install libraries

```shell
    conda env create -n text 
    pip install -r requirement.txt
```

4. Train
If use pretrained, please uncoment 'config/pan/pan_r18_ctw_finetune.py#L55' else:

```shell
    sh train.sh
```
5. Test

```shell
    sh test.sh
```



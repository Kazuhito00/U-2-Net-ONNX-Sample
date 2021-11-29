# U-2-Net-ONNX-Sample
<img src="https://user-images.githubusercontent.com/37477845/143875127-d3629a3e-3a40-44cd-b0b7-ce87a23addf5.png" width="75%"><br>
<img src="https://user-images.githubusercontent.com/37477845/143875154-fe9bd64c-2488-43b9-9269-87e3bb554dc5.png" width="75%"><br>
[U-2-Net](https://github.com/xuebinqin/U-2-Net)のPythonでのONNX推論サンプルです。<br>
ONNXに変換したモデルも同梱しています。<br>
変換自体を試したい方はColaboratoryなどで[U-2-Net-Convert2ONNX.ipynb](U-2-Net-Convert2ONNX.ipynb)を使用ください。<br>

# Requirement(ONNX変換)
* Pytorch 1.9.0 or later
* onnx 1.10.2 or later
* onnx-simplifier 0.3.6 or later

# Requirement(ONNX推論)
* gdown 4.2.0 or later
* OpenCV 4.5.3.56 or later
* onnxruntime-gpu 1.9.0 or later <br>※onnxruntimeでも動作しますが、推論時間がかかるのでGPUをお勧めします

# Demo(u2net、u2netp、u2net_human_seg)
デモの実行方法は以下です。<br>
デモ実行前に、Googleドライブから[u2net.onnx](https://drive.google.com/uc?export=download&id=1pDjgTn-9my55rkSICbMANHdVVzWJPo4s)、[u2netp.onnx](https://drive.google.com/uc?export=download&id=1SySup4MV-XmOQz_1i55mpTpRnSwSCc5z)、[u2net_human_seg.onnx](https://drive.google.com/uc?export=download&id=1MhF6Ceeb9w23iUczHX5EPApETk23F2oT)の何れかをダウンロードし、modelディレクトリに格納してください。<br>
実行対象のモデルが格納されていない場合、gdownを用いたダウンロードが実行されます(gdownインストール必要)
```bash
python sample_u2net_onnx.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：640
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：360
* --model<br>
ロードするモデルの格納パス<br>
デフォルト：model/u2net.onnx
選択肢：model/u2net.onnx、model/u2netp.onnx、model/u2net_human_seg.onnx
* --input_shape<br>
モデルの入力サイズ<br>
デフォルト：320

# Demo(u2net_portrait)
デモの実行方法は以下です。<br>
デモ実行前に、Googleドライブから[u2net_portrait.onnx](https://drive.google.com/uc?export=download&id=1lQczvEk2w74rnUpY_4Q0Et9iNywmnxE3)の何れかをダウンロードし、modelディレクトリに格納してください。<br>
u2net_portrait.onnxが格納されていない場合、gdownを用いたダウンロードが実行されます(gdownインストール必要)
```bash
python sample_u2net_onnx.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：640
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：360
* --model<br>
ロードするモデルの格納パス<br>
デフォルト：model/u2net_portrait.onnx
* --input_shape<br>
モデルの入力サイズ<br>
デフォルト：512

# Reference
* [xuebinqin/U-2-Net](https://github.com/xuebinqin/U-2-Net)

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
U-2-Net-ONNX-Sample is under [Apache 2.0 License](LICENSE).

# License(Image)
猫の画像と女性の画像は[フリー素材ぱくたそ](https://www.pakutaso.com)様の写真を利用しています。

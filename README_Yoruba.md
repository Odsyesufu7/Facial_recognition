# Idanimọ oju

_O tun le ka ẹda ti o tumọ ti faili yii [ni Swahili](https://github/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/README.md) ati Awọn ede Nàìjíríà mẹ́ta.

Ṣe idanimọ ati riboribo awọn oju lati Python tabi lati laini aṣẹ pẹlu
ile-ikawe idanimọ oju ti o rọrun julọ ni agbaye.

Ti a kọ ni lilo [dlib](http://dlib.net/) idanimọ oju-ti-ti-ti-aworan
itumọ ti pẹlu jin eko. Awọn awoṣe ni o ni ohun išedede ti 99,38% lori awọn
[Awọn oju ti a samisi ni Egan] bi ala-ilẹ.

Eyi tun pese ọpa laini aṣẹ 'face_recognition' ti o rọrun ti o jẹ ki
o ṣe idanimọ oju lori folda ti awọn aworan lati laini aṣẹ!


[![PyPI](https://img.shields.io/pypi/v/face_recognition.svg)](https://pypi.python.org/pypi/face_recognition)
[![Ipo Iwe aṣẹ](https://readthedocs.org/projects/face-recognition/badge/?version=latest)](http://face-recognition.readthedocs.io/en/latest/?badge=latest) )

## Awọn ẹya ara ẹrọ

#### Wa awọn oju ni awọn aworan

Wa gbogbo awọn oju ti o han ninu aworan kan:

![](https://cloud.githubusercontent.com/assets/896692/23625227/42c65360-025d-11e7-94ea-b12f28cb34b4.png)

`` Python
gbe wọle face_recognition
aworan = face_recognition.load_image_file ("your_file.jpg")
oju_locations = oju_recognition.face_locations(aworan)
```

#### Wa ki o ṣe afọwọyi awọn ẹya oju ni awọn aworan

Gba awọn ipo ati awọn ilana ti oju eniyan kọọkan, imu, ẹnu ati gba pe.

![](https://cloud.githubusercontent.com/assets/896692/23625282/7f2d79dc-025d-11e7-8728-d8924596f8fa.png)

`` Python
gbe wọle face_recognition
aworan = face_recognition.load_image_file ("your_file.jpg")
face_landmarks_list = oju_recognition.face_landmarks(aworan)
```

Wiwa awọn ẹya oju jẹ iwulo pupọ fun ọpọlọpọ nkan pataki. Ṣugbọn o tun le lo fun awọn nkan aṣiwere gaan
bii lilo [ẹke oni-nọmba] (ro 'Meitu'):

![](https://cloud.githubusercontent.com/assets/896692/23625283/80638760-025d-11e7-80a2-1d2779f7ccab.png)

#### Ṣe idanimọ awọn oju ni awọn aworan

Ṣe idanimọ ẹniti o farahan ninu fọto kọọkan.

![](https://cloud.githubusercontent.com/assets/896692/23625229/45e049b6-025d-11e7-89cc-8a71cf89e713.png)

`` Python
gbe wọle face_recognition
known_image = face_recognition.load_image_file ("biden.jpg")
unknown_image = face_recognition.load_image_file("unknown.jpg")

biden_encoding = face_recognition.face_encodings(image_known)[0]
unknown_encoding = face_recognition.face_encodings(unknown_image)[0]

awọn esi = face_recognition.compare_faces ([biden_encoding], unknown_encoding)
```

O le paapaa lo ile-ikawe yii pẹlu awọn ile-ikawe Python miiran lati ṣe idanimọ oju-akoko gidi:

![](https://cloud.githubusercontent.com/assets/896692/24430398/36f0e3f0-13cb-11e7-8258-4d0c9ce1e419.gif)

Wo [apẹẹrẹ yii](https://github.com/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/examples/facerec_from_webcam_faster.py) fun koodu naa.

## Online Demos

Olumulo-ṣe idasi pinpin Jupyter notebook demo (kii ṣe atilẹyin ni ifowosi): [![Deepnote](https://beta.deepnote.org/buttons/try-in-a-jupyter-notebook.svg)](https://beta) .deepnote.org/launch?template=face_recognition)

## Fifi sori ẹrọ

### Awọn ibeere

   Python 3.3+ tabi Python 2.7
   * MacOS, Lainos ati Windows ni atilẹyin laisi iṣeduro ṣugbọn o tun ṣiṣẹ.

### Awọn aṣayan fifi sori ẹrọ:

#### Fifi sori Mac tabi Lainos

Ni akọkọ, rii daju pe o ti fi sori ẹrọ dlib tẹlẹ pẹlu awọn asopọ Python:

   * [Bawo ni lati fi sori ẹrọ dlib lati orisun lori MacOS tabi Ubuntu](https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf)
  
Lẹhinna rii daju pe o ti fi cmake sori ẹrọ:
 
```fifi sori ẹrọ cmake``

Nikẹhin, fi sori ẹrọ module yii lati pypi ni lilo `pip3` (tabi `pip2` fun Python 2):

`` bash
pip3 fi sori ẹrọ face_recognition
```

Ni omiiran, o le gbiyanju ile-ikawe yii pẹlu [Docker](https://www.docker.com/), wo [apakan yii](#deployment).



#### Fifi sori ọkọ Nvidia Jetson Nano

  * [Jetson Nano awọn ilana fifi sori ẹrọ](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python -a25cb8c891fd)
    * Jọwọ tẹle awọn ilana ti o wa ninu nkan naa ni iṣọra. Kokoro kan wa lọwọlọwọ ninu awọn ile-ikawe CUDA lori Jetson Nano ti yoo fa ki ile-ikawe yii kuna ni idakẹjẹ ti o ko ba tẹle awọn ilana inu nkan naa lati ṣalaye laini kan ni dlib ki o tun ṣe akopọ.

#### Fifi sori Rasipibẹri Pi 2+

   * [Rasipibẹri Pi 2+ awọn ilana fifi sori ẹrọ]

#### fifi sori FreeBSD

`` bash
pkg fi sori ẹrọ eya/py-face_recognition
```

#### Fifi sori ẹrọ lori Windows

Lakoko ti a ko ṣe atilẹyin Windows ni ifowosi, awọn olumulo ti o ṣe iranlọwọ ti fi awọn itọnisọna sori bi o ṣe le fi ile-ikawe yii sori ẹrọ:

   * [@masoudr's Windows 10 itọsọna fifi sori ẹrọ (dlib + face_recognition)]

#### Nfi aworan ẹrọ foju ti a ti ṣeto tẹlẹ

   * [Ṣe igbasilẹ aworan VM ti a ti ṣatunṣe tẹlẹ].

## Lilo

### Òfin-Line Interface

Nigbati o ba fi sori ẹrọ `face_recognition`, o gba laini pipaṣẹ meji ti o rọrun
awọn eto:

* `Imọ_oju` - Mọ awọn oju ni aworan tabi folda ti o kun fun
    awọn aworan.
* `fac

e_detection` - Wa awọn oju ni aworan tabi folda ti o kun fun awọn fọto.

#### `face_recognition` ọpa laini aṣẹ

Aṣẹ 'oju_recognition' jẹ ki o mọ awọn oju ni aworan kan tabi
folda ti o kun fun awọn fọto.

Ni akọkọ, o nilo lati pese folda kan pẹlu aworan kan ti eniyan kọọkan ti o
ti mọ tẹlẹ. O yẹ ki o jẹ faili aworan kan fun eniyan kọọkan pẹlu
awọn faili ti a darukọ gẹgẹbi ẹniti o wa ninu aworan:

![mọ](https://cloud.githubusercontent.com/assets/896692/23582466/8324810e-00df-11e7-82cf-41515eba704d.png)

Nigbamii, o nilo folda keji pẹlu awọn faili ti o fẹ ṣe idanimọ:

![aimọ](https://cloud.githubusercontent.com/assets/896692/23582465/81f422f8-00df-11e7-8b0d-75364f641f58.png)

Lẹhinna ninu rẹ kan ṣiṣe aṣẹ naa 'oju_ idanimọ', ti nwọle wọle
folda ti awọn eniyan ti a mọ ati folda (tabi aworan kan) pẹlu aimọ
eniyan ati pe o sọ fun ọ ẹniti o wa ninu aworan kọọkan:

`` bash
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_person
```

Laini kan wa ninu abajade fun oju kọọkan. Awọn data ti wa ni ipin koma-koma
pẹlu orukọ faili ati orukọ eniyan ti a rii.

'Eniyan_aimọ' jẹ oju kan ninu aworan ti ko baramu ẹnikẹni ninu
folda rẹ ti awọn eniyan ti a mọ.

#### 'oju_detection` ọpa laini aṣẹ

Aṣẹ `face_detection` jẹ ki o wa ipo naa (awọn ipoidojuko piksẹli)
ti eyikeyi oju ni aworan kan.

Kan ṣiṣẹ aṣẹ naa `oju_detection`, ti nkọja sinu folda ti awọn aworan
lati ṣayẹwo (tabi aworan kan):

`` bash
$ oju_detection ./folder_with_pictures/

apẹẹrẹ / image1.jpg,65,215,169,112
apẹẹrẹ / image2.jpg,62,394,211,244
apẹẹrẹ / image2.jpg,95,941,244,792
```

O ṣe atẹjade laini kan fun oju kọọkan ti a rii. Awọn ipoidojuko
royin ni oke, ọtun, isalẹ ati osi ipoidojuko ti awọn oju (ni awọn piksẹli).
 
##### Ifarada Iṣatunṣe / Ifamọ

Ti o ba n gba awọn ere-kere pupọ fun eniyan kanna, o le jẹ iyẹn
awọn eniyan ti o wa ninu awọn fọto rẹ jọra pupọ ati iye ifarada kekere
nilo lati ṣe awọn afiwe oju diẹ sii ti o muna.

O le ṣe bẹ pẹlu paramita `--lerance'. Ifarada aiyipada
iye jẹ 0.6 ati awọn nọmba kekere ṣe awọn afiwe oju diẹ sii ti o muna:

`` bash
$ face_recognition --ifarada 0.54 ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_person
```

Ti o ba fẹ wo ijinna oju ti a ṣe iṣiro fun ibaamu kọọkan ni ibere
lati ṣatunṣe eto ifarada, o le lo `--show-distance otitọ':

`` bash
$ face_recognition --show-ijinna ootọ ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama,0.378542298956785
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_person, Kò
```

##### Awọn apẹẹrẹ diẹ sii

Ti o ba kan fẹ lati mọ orukọ awọn eniyan ti o wa ninu aworan kọọkan ṣugbọn kii ṣe
bikita nipa awọn orukọ faili, o le ṣe eyi:

`` bash
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/ | ge -d ',' -f2

Barack Obama
aimọ_eniyan
```

##### Iyara soke idanimọ oju

Idanimọ oju le ṣee ṣe ni afiwe ti o ba ni kọnputa pẹlu
ọpọ Sipiyu inu ohun kohun. Fun apẹẹrẹ, ti eto rẹ ba ni awọn ohun kohun Sipiyu 4, o le
ilana nipa 4 igba bi ọpọlọpọ awọn aworan ni iye kanna ti akoko nipa lilo
gbogbo awọn ohun kohun Sipiyu rẹ ni afiwe.

Ti o ba nlo Python 3.4 tabi tuntun, kọja ni `-cpus <number_of_cpu_cores_to_use>` paramita:

`` bash
$ face_recognition --cpus 4 ./pictures_of_people_i_know/ ./unknown_pictures/
```

O tun le kọja ni `--cpus -1` lati lo gbogbo awọn ohun kohun Sipiyu ninu eto rẹ.

#### Python Module

O le ṣe agbewọle module `face_recognition` ati lẹhinna ni irọrun ṣe afọwọyi
oju pẹlu o kan kan tọkọtaya ti ila ti koodu. O rọrun pupọ!

API Docs: [https://face-recognition.readthedocs.io](https://face-recognition.readthedocs.io/en/latest/face_recognition.html).

##### Ni aifọwọyi wa gbogbo awọn oju ni aworan kan

`` Python
gbe wọle face_recognition

aworan = face_recognition.load_image_file ("my_picture.jpg")
oju_locations = oju_recognition.face_locations(aworan)

# awọn ipo_oju ni bayi atokọ akojọpọ awọn ipoidojuko ti oju kọọkan!
```

Wo [apẹẹrẹ yii](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
  lati gbiyanju o jade.

O tun le jade si awoṣe wiwa oju ti o da lori ẹkọ-jinle deede diẹ sii.

Akiyesi: Isare GPU (nipasẹ ile-ikawe CUDA NVidia) nilo fun rere
išẹ pẹlu awoṣe yi. Iwọ yoo tun fẹ lati mu atilẹyin CUDA ṣiṣẹ
nigbati compliling `dlib`.

`` Python
gbe wọle face_recognition

aworan = face_recognition.load_image_file ("my_picture.jpg")
face_locations = face_recognition.face_locations (aworan, awoṣe = "cnn")

# awọn ipo_oju ni bayi atokọ akojọpọ awọn ipoidojuko ti oju kọọkan!
```

Wo [apẹẹrẹ yii](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
  lati gbiyanju o jade.

Ti o ba ni aworan pupọ

s ati ki o kan GPU, o tun le
[wa awọn oju ni awọn ipele](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py).

##### Ni aifọwọyi wa awọn ẹya oju ti eniyan ni aworan kan

`` Python
gbe wọle face_recognition

aworan = face_recognition.load_image_file ("my_picture.jpg")
face_landmarks_list = oju_recognition.face_landmarks(aworan)

# face_landmarks_list jẹ akojọpọ bayi pẹlu awọn ipo ti ẹya oju kọọkan ni oju kọọkan.
# face_landmarks_list[0]['osi_oju'] yoo jẹ ipo ati ilana oju osi eniyan akọkọ.
```

Wo [apẹẹrẹ yii](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
  lati gbiyanju o jade.

##### Ṣe idanimọ awọn oju ni awọn aworan ki o ṣe idanimọ ti wọn jẹ

`` Python
gbe wọle face_recognition

picture_of_me = face_recognition.load_image_file("me.jpg")
my_face_encoding = face_recognition.face_encodings(picture_of_me)[0]

# koodu_oju_mi_mi ni bayi ni 'iyipada' gbogbo agbaye ti awọn ẹya oju mi ti o le ṣe afiwe si eyikeyi aworan miiran ti oju kan!

unknown_picture = face_recognition.load_image_file("unknown.jpg")
unknown_face_encoding = face_recognition.face_encodings(unknown_picture)[0]

# Bayi a le rii pe awọn koodu oju meji jẹ ti eniyan kanna pẹlu `afiwera_oju`!

awọn esi = face_recognition.compare_faces ([my_face_encoding], unknown_face_encoding)

ti awọn abajade ba [0] == Lootọ:
     tẹjade ("Aworan mi ni!")
miran:
     tẹjade ("Kii ṣe aworan mi!")
```

Wo [apẹẹrẹ yii](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
  lati gbiyanju o jade.

## Awọn apẹẹrẹ koodu Python

Gbogbo awọn apẹẹrẹ wa [nibi](https://github.com/Odsyesufu7/face_recognition/tree/master/emples).


#### Iwari oju

* [Wa awọn oju ni aworan kan](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
* [Wa awọn oju ni aworan kan (lilo ẹkọ ti o jinlẹ)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
* [Wa awọn oju ni awọn ipele ti awọn aworan w/ GPU (lilo ẹkọ ti o jinlẹ)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py)
* [Doju gbogbo awọn oju inu fidio laaye ni lilo kamera wẹẹbu rẹ (Nilo OpenCV lati fi sii)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/blur_faces_on_webcam.py)

#### Oju Awọn ẹya ara ẹrọ

* [Ṣe idanimọ awọn ẹya oju kan pato ninu aworan](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
* [Waye (ẹgbin ti o buruju) atike oni nọmba](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/digital_makeup.py)

#### Idanimọ Oju

* [Wa ki o ṣe idanimọ awọn oju aimọ ni aworan ti o da lori awọn fọto ti awọn eniyan ti a mọ](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
* [Ṣe idanimọ ati ya awọn apoti ni ayika eniyan kọọkan ninu fọto](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/identify_and_draw_boxes_on_faces.py)
* [Ṣe afiwe awọn oju nipasẹ ijinna oju nomba dipo awọn ibaamu otitọ/Iro nikan](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_distance.py)
* [Ṣe idanimọ awọn oju ni fidio ifiwe ni lilo kamera wẹẹbu rẹ - Irọrun / Ẹya Slower (Nilo OpenCV lati fi sii)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam.py)
* [Ṣe idanimọ awọn oju ni fidio ifiwe ni lilo kamera wẹẹbu rẹ - Ẹya Yara (Nilo OpenCV lati fi sii)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam_faster.py)
* [Ṣe idanimọ awọn oju inu faili fidio kan ki o kọ faili fidio tuntun (Nilo OpenCV lati fi sii)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_video_file.py)
* [Ṣe idanimọ awọn oju lori Rasipibẹri Pi w/ kamẹra](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_on_raspberry_pi.py)
* [Ṣiṣe iṣẹ wẹẹbu kan lati ṣe idanimọ awọn oju nipasẹ HTTP (Nilo Flask lati fi sii)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/web_service_example.py)
* [Ṣe idanimọ awọn oju pẹlu ikasi awọn aladugbo K-sunmọ](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_knn.py)
* [Kọ awọn aworan pupọ fun eniyan lẹhinna da awọn oju mọ nipa lilo SVM](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_svm.py)

## Ṣiṣẹda Standalone Executable
- [Idanimọ oju pẹlu OpenCV, Python, ati ẹkọ ti o jinlẹ](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/) nipasẹ Adrian Rosebrock
   - Ni wiwa bi o ṣe le lo idanimọ oju ni iṣe
- [Rasipibẹri Pi idanimọ oju](https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/) nipasẹ Adrian Rosebrock
   - Ni wiwa bi o ṣe le lo eyi lori Rasipibẹri Pi
- [Ṣijọpọ oju pẹlu Python](https://www.pyimagesearch.com/2018/07/09/

oju-clustering-with-python/) nipasẹ Adrian Rosebrock
   - Ni wiwa bi o ṣe le ṣajọ awọn fọto laifọwọyi da lori ẹni ti o han ni fọto kọọkan nipa lilo ẹkọ ti ko ni abojuto

## Awọn akiyesi

* Awoṣe idanimọ oju jẹ ikẹkọ lori awọn agbalagba ati pe ko ṣiṣẹ daradara lori awọn ọmọde. O duro lati dapọ
   soke omo oyimbo rorun a lilo awọn aiyipada lafiwe ala ti 0,6.
* Yiye le yatọ laarin awọn ẹgbẹ ẹya.

## <a name="deployment">Ifiranṣẹ si Awọn ogun Awọsanma (Heroku, AWS, ati bẹbẹ lọ)</a>

Níwọ̀n bí `ìdámọ̀ ojú_oju' gbarale `dlib` tí a kọ sí C++, ó lè jẹ́ ẹ̀tàn láti gbé ìṣàfilọ́lẹ̀ kan lọ
lilo rẹ si olupese alejo gbigba awọsanma bi Heroku tabi AWS.

Lati jẹ ki awọn nkan rọrun, apẹẹrẹ Dockerfile wa ninu repo yii ti o fihan bi o ṣe le ṣiṣẹ app ti a ṣe pẹlu
`Oju_recognition' ni a [Docker] (https://www.docker.com/) eiyan. Pẹlu iyẹn, o yẹ ki o ni anfani lati fi ranṣẹ
si eyikeyi iṣẹ ti o ṣe atilẹyin awọn aworan Docker.

O le gbiyanju aworan Docker ni agbegbe nipa ṣiṣiṣẹ: `docker-compose up --build`

O tun wa [ọpọlọpọ awọn aworan Docker ti a ti kọ tẹlẹ.](docker/README.md)

Awọn olumulo Linux pẹlu GPU (awọn awakọ> = 384.81) ati [Nvidia-Docker] (https://github.com/NVIDIA/nvidia-docker) ti fi sori ẹrọ le ṣiṣẹ apẹẹrẹ lori GPU: Ṣii [docker-compose.yml] (docker-compose.yml) faili ati uncomment `dockerfile: Dockerfile.gpu` ati ` asiko isise: nvidia` laini.

## O ṣeun

* Ọpọlọpọ, ọpọlọpọ ọpẹ si Davis King [@nulhom]
   fun ṣiṣẹda dlib ati fun ipese wiwa ẹya oju ti ikẹkọ ati awọn awoṣe fifi koodu oju
   lo ni yi ìkàwé. Fun alaye diẹ sii lori ResNet ti o ṣe agbara awọn koodu oju, ṣayẹwo
   re [bulọọgi post] (http://blog.dlib.net/2017/02/high-quality-face-recognition-with-deep.html).
* Ṣeun si gbogbo eniyan ti o ṣiṣẹ lori gbogbo awọn ile-ikawe imọ-jinlẹ data Python oniyi bii numpy, scipy, scikit-image,
   irọri, ati bẹbẹ lọ, ati bẹbẹ lọ ti o jẹ ki iru nkan yii rọrun ati igbadun ni Python.
* Ọpẹ si [Cookiecutter] Audreyrproject awoṣe
   fun a ṣe Python ise agbese apoti ọna diẹ ifarada.

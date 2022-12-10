# Nchọpụta ihu

_Ịnwekwara ike ịgụ ụdị faịlụ a atụgharịrị [na Swahili](https://github/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/README.md) na Asụsụ Naijiria atọ.

Chọpụta ma jikwaa ihu sitere na Python ma ọ bụ site na ahịrị iwu nwere
ọba akwụkwọ njirimara ihu kacha dị n'ụwa.

Ewuru site na iji [dlib](http://dlib.net/) njirimara ihu ọhụụ nke nka
wuru na mmụta miri emi. Ihe nlereanya ahụ nwere izi ezi nke 99.38% na
[Ihu ndị akpọrọ n'ime ọhịa] dị ka akara aka.

Nke a na-enyekwa ngwaọrụ ahịrị iwu 'face_recognition' dị mfe nke na-ahapụ
ị na-eme njirimara ihu na nchekwa nke onyonyo sitere na ahịrị iwu!


[![PyPI](https://img.shields.io/pypi/v/face_recognition.svg)](https://pypi.python.org/pypi/face_recognition)
[![Ọnọdụ akwụkwọ](https://readthedocs.org/projects/face-recognition/badge/?version=latest)](http://face-recognition.readthedocs.io/en/latest/?badge=latest) )

## Akụkụ

#### Chọta ihu na foto

Chọta ihu niile pụtara na eserese:

![](https://cloud.githubusercontent.com/assets/896692/23625227/42c65360-025d-11e7-94ea-b12f28cb34b4.png)

"Python
mbubata ihu_recognition
onyonyo = face_recognition.load_image_file("your_file.jpg")
ihu_locations = ihu_recognition.face_locations(onyinyo)
``

#### Chọta ma megharịa atụmatụ ihu na foto

Nweta ọnọdụ na ndepụta nke anya onye ọ bụla, imi, ọnụ na agba.

![](https://cloud.githubusercontent.com/assets/896692/23625282/7f2d79dc-025d-11e7-8728-d8924596f8fa.png)

"Python
mbubata ihu_recognition
onyonyo = face_recognition.load_image_file("your_file.jpg")
face_landmarks_list = ihu_recognition.face_landmarks(onyinyo)
``

Ịchọta ọdịdị ihu dị oke uru maka ọtụtụ ihe dị mkpa. Ma ị nwekwara ike iji ya maka ihe nzuzu n'ezie
dị ka itinye [dijitalụ etemeete] (chee 'Meitu'):

![](https://cloud.githubusercontent.com/assets/896692/23625283/80638760-025d-11e7-80a2-1d2779f7ccab.png)

#### Chọpụta ihu na foto

Mara onye na-egosi na foto ọ bụla.

![](https://cloud.githubusercontent.com/assets/896692/23625229/45e049b6-025d-11e7-89cc-8a71cf89e713.png)

"Python
mbubata ihu_recognition
known_image = face_recognition.load_image_file("biden.jpg")
unknown_image = face_recognition.load_image_file("unknown.jpg")

biden_encoding = face_recognition.face_encodings(amaara_image)[0]
unknown_encoding = face_recognition.face_encodings(unknown_image)[0]

nsonaazụ = face_recognition.compare_faces([biden_encoding], amaghị_encoding)
``

Ịnwere ike iji ọba akwụkwọ Python ndị ọzọ mee njirimara ihu ozugbo:

![](https://cloud.githubusercontent.com/assets/896692/24430398/36f0e3f0-13cb-11e7-8258-4d0c9ce1e419.gif)

Hụ [ihe atụ a](https://github.com/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/examples/facerec_from_webcam_faster.py) maka koodu.

## Ihe ngosi ntanetị

Ngosi akwụkwọ ndetu Jupyter nke onye ọrụ nyere aka (anaghị akwado ọchịchị): [![Deepnote](https://beta.deepnote.org/buttons/try-in-a-jupyter-notebook.svg)](https://beta) .deepnote.org/launch?template=face_recognition)

## Nwụnye

### chọrọ

   Python 3.3+ ma ọ bụ Python 2.7
   * MacOS, Linux na Windows na-akwadoghị mana ọ na-arụkwa ọrụ.

### Nhọrọ nwụnye:

#### Wụnye na Mac ma ọ bụ Linux

Nke mbụ, jide n'aka na ị tinyelarị dlib na Python bindings:

   * [Etu esi etinye dlib site na isi mmalite na macOS ma ọ bụ Ubuntu](https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf)
  
Mgbe ahụ, gbaa mbọ hụ na etinyere cmake:
 
```brew install cmake``

N'ikpeazụ, wụnye modul a site na pypi iji 'pip3' (ma ọ bụ 'pip2' maka Python 2):

`` bash
pip3 tinye face_recognition
``

N'aka nke ọzọ, ịnwere ike iji [Docker] (https://www.docker.com/) nwalee ọba akwụkwọ a, lee [ngalaba a](#deployment).



#### Ịwụnye na bọọdụ Nvidia Jetson Nano

  * [Jetson Nano ntuziaka nwụnye](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python -a25cb8c891fd)
    * Biko soro ntuziaka dị n'isiokwu a nke ọma. Enwere ahụhụ dị ugbu a na ọba akwụkwọ CUDA dị na Jetson Nano nke ga-eme ka ọbaakwụkwọ a daa n'ime nkịtị ma ọ bụrụ na ị naghị agbaso ntuziaka dị n'isiokwu ahụ iji kwuo otu ahịrị na dlib wee chịkọta ya.

#### Ịwụnye na Raspberry Pi 2+

   * [Raspberry Pi 2+ ntuziaka nwụnye]

#### wụnye na FreeBSD

`` bash
pkg tinye eserese/py-face_recognition
``

#### wụnye na Windows

Ọ bụ ezie na akwadoghị Windows n'ihu ọha, ndị ọrụ na-enyere aka etinyela ntuziaka maka otu esi etinye ọba akwụkwọ a:

   * [@masoudr's Windows 10 ntuziaka nwụnye (dlib + face_recognition)]

#### Ịwụnye ihe oyiyi igwe mebere ahazi nke ọma

   * [Budata onyonyo VM ahaziri mbụ].

## Ojiji

### Iwu-Line Interface

Mgbe ị rụnyere 'face_recognition', ị ga-enweta ahịrị iwu abụọ dị mfe
mmemme:

* ` ihu_mmata` - Mara ihu na foto ma ọ bụ nchekwa juputara maka
    foto.
* 'fac

e_detection` - Chọta ihu na foto ma ọ bụ nchekwa juputara maka foto.

Ngwá ọrụ ahịrị iwu #### `face_recognition`

Iwu 'ihu_ịmata' na-enye gị ohere ịmata ihu na foto ma ọ bụ
folda juru maka foto.

Nke mbụ, ịkwesịrị ịnye folda otu foto nke onye ọ bụla
maralarị. Ekwesịrị inwe otu faịlụ onyonyo maka onye ọ bụla nwere ya
faịlụ ndị akpọrọ dịka onye dị na foto a si dị:

![mara](https://cloud.githubusercontent.com/assets/896692/23582466/8324810e-00df-11e7-82cf-41515eba704d.png)

Ọzọ, ịchọrọ folda nke abụọ nwere faịlụ ndị ịchọrọ ịmata:

![amaghị](https://cloud.githubusercontent.com/assets/896692/23582465/81f422f8-00df-11e7-8b0d-75364f641f58.png)

Mgbe ahụ, n'ime gị na-agba ọsọ 'face_recognition', na-abanye
nchekwa nke ndị ama ama na nchekwa (ma ọ bụ otu onyonyo) na-amaghị ama
ndị mmadụ ma ọ na-agwa gị onye nọ na onyonyo ọ bụla:

`` bash
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg, Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_person
``

Enwere otu ahịrị na mmepụta maka ihu ọ bụla. E kewapụrụ data ahụ-rịkọm
na aha faịlụ na aha onye ahụ achọtara.

'Onye amaghị_onye' bụ ihu dị n'onyinyo nke na-adabaghị na onye ọ bụla
nchekwa gị nke ndị ama ama.

Ngwá ọrụ ahịrị iwu #### `face_detection`

Iwu 'face_detection' na-enye gị ohere ịchọta ebe ahụ (nchịkwa pixel)
nke ihu ọ bụla na onyonyo.

Naanị gbaa iwu 'face_detection', na-agafe na nchekwa foto
ịlele (ma ọ bụ otu onyonyo):

`` bash
$ ihu_nyocha ./folder_with_pictures/

atụ/image1.jpg,65,215,169,112
ihe atụ/image2.jpg,62,394,211,244
ihe atụ/image2.jpg,95,941,244,792
``

Ọ na-ebipụta otu ahịrị maka ihu ọ bụla achọpụtara. Ndị nhazi
akọwara bụ nhazi elu, aka nri, ala na aka ekpe nke ihu (na pikselụ).
 
##### Na-emezi nnabata / uche

Ọ bụrụ na ị na-enweta ọtụtụ egwuregwu maka otu onye, ọ nwere ike ịbụ nke ahụ
ndị mmadụ na foto gị yiri nke ukwuu na uru nnabata dị ala
dị mkpa iji mee ka ntụnyere ihu sie ike karị.

Ị nwere ike ime nke ahụ site na iji paramita '--tolerance'. Nkwenye ndabara
uru bụ 0.6 na ọnụ ọgụgụ dị ala na-eme ka ntụnyere ihu sie ike karị:

`` bash
$ face_recognition --tolerance 0.54 ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg, Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_person
``

Ọ bụrụ na ịchọrọ ịhụ ka agbakọrọ anya ihu maka egwuregwu ọ bụla n'usoro
iji dozie ntọala nnabata, ị nwere ike iji `--show-distance true':

`` bash
$ face_recognition --show-distance true ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg, Barack Obama, 0.378542298956785
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_person, Ọ dịghị onye
``

##### Ihe atụ ndị ọzọ

Ọ bụrụ na ịchọrọ ịmata aha ndị nọ na foto ọ bụla mana ị chọghị
na-eche maka aha faịlụ, ị nwere ike ime nke a:

`` bash
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/ | ịkpụ -d ',' -f2

Barack Obama
onye amaghi ama
``

##### Na-eme ka njirimara ihu dị ngwa

Enwere ike ime njirimara ihu n'otu oge ma ọ bụrụ na ị nwere kọmputa
ọtụtụ cores CPU. Dịka ọmụmaatụ, ọ bụrụ na sistemụ gị nwere cores CPU 4, ị nwere ike
hazie ihe dị ka ugboro 4 ọtụtụ onyonyo n'otu oge site na iji
cores CPU gị niile n'otu oge.

Ọ bụrụ na ị na-eji Python 3.4 ma ọ bụ nke ọhụrụ, gafere na '--cpus <number_of_cpu_cores_to_use>' parameter:

`` bash
$ face_recognition --cpus 4 ./pictures_of_people_i_know/ ./unknown_pictures/
``

Ị nwekwara ike ịgafe na '--cpus -1' iji jiri cores CPU niile dị na sistemụ gị.

#### Modul Python

Ị nwere ike ibubata modul 'face_recognition' wee jirikwa ngwa ngwa
chere ihu nwere naanị ahịrị koodu abụọ. Ọ dị oke mfe!

API Docs: [https://face-recognition.readthedocs.io](https://face-recognition.readthedocs.io/en/latest/face_recognition.html).

##### Chọta ihu niile dị na foto na akpaghị aka

"Python
mbubata ihu_recognition

onyonyo = face_recognition.load_image_file("my_picture.jpg")
ihu_locations = ihu_recognition.face_locations(onyinyo)

# ihu_locations bụ usoro na-edepụta nhazi ihu ọ bụla!
``

Hụ [ihe atụ a](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
  ịnwale ya.

Ị nwekwara ike ịbanye na ụdị nchọpụta ihu dabere na mmụta miri emi nke ziri ezi.

Mara: Achọrịrị ngwangwa GPU (site n'ọbá akwụkwọ CUDA NVidia) maka ịdị mma
arụmọrụ na ihe nlereanya a. Ị ga-achọkwa ịkwado nkwado CUDA
mgbe ị na-agbakọ 'dlib'.

"Python
mbubata ihu_recognition

onyonyo = face_recognition.load_image_file("my_picture.jpg")
face_locations = ihu_recognition.face_locations(onyinyo, ụdị = "cnn")

# ihu_locations bụ usoro na-edepụta nhazi ihu ọ bụla!
``

Hụ [ihe atụ a](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
  ịnwale ya.

Ọ bụrụ na ị nwere ọtụtụ ihe oyiyi

s na GPU, ị nwekwara ike
[chọta ihu na batches](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py).

##### Chọpụta ọdịdị ihu mmadụ na akpaghị aka

"Python
mbubata ihu_recognition

onyonyo = face_recognition.load_image_file("my_picture.jpg")
face_landmarks_list = ihu_recognition.face_landmarks(onyinyo)

# face_landmarks_list bụ ahaziri n'usoro nwere ọnọdụ ihu ọ bụla na ihu ọ bụla.
# face_landmarks_list[0]['left_eye'] ga-abụ ebe na ndepụta nke anya ekpe nke onye mbụ.
``

Hụ [ihe atụ a](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
  ịnwale ya.

##### Chọpụta ihu na onyonyo wee chọpụta ndị ha bụ

"Python
mbubata ihu_recognition

picture_of_me = face_recognition.load_image_file("me.jpg")
my_face_encoding = ihu_recognition.face_encodings(foto_m)[0]

# my_face_encoding ugbu a nwere 'encoding' nke ọdịdị ihu m nke enwere ike iji tụnyere foto ihu ọ bụla ọzọ!

unknown_picture = face_recognition.load_image_file("unknown.jpg")
unknown_face_encoding = face_recognition.face_encodings(unknown_picture)[0]

# Ugbu a, anyị nwere ike ịhụ na nzuzo ihu abụọ a bụ otu onye nwere 'tụnyere ihu'!

nsonaazụ = face_recognition.compare_faces([my_face_encoding], unknown_face_encoding)

ọ bụrụ nsonaazụ[0] == Eziokwu:
     ebipụta ("Ọ bụ foto m!")
ọzọ:
     ebipụta ("Ọ bụghị foto m!")
``

Hụ [ihe atụ a](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
  ịnwale ya.

## Ihe atụ Eke Ọgba

Ihe atụ niile dị [ebe a](https://github.com/Odsyesufu7/face_recognition/tree/master/emples).


#### Nchọpụta ihu

* [Chọta ihu na foto](https://github.com/Odsyesufu7/face_recognition/blob/master/emples/find_faces_in_picture.py)
* [Chọta ihu na foto (iji mmụta miri emi)](https://github.com/Odsyesufu7/face_recognition/blob/master/emples/find_faces_in_picture_cnn.py)
* [Chọta ihu na batches nke onyonyo w/ GPU (iji mmụta miri emi)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py)
* [Mechie ihu niile na vidiyo dị ndụ site na iji kamera weebụ gị (chọrọ ka etinyere OpenCV)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/blur_faces_on_webcam.py)

#### Akụkụ ihu

* [Chọpụta ụdị ihu a kapịrị ọnụ na foto](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
* [Tinye (nke jọgburu onwe ya) etemeete dijitalụ](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/digital_makeup.py)

#### Nghọta ihu

* [Chọta ma mata ihu ndị amabeghị na foto dabere na foto ndị ama ama](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
* [Chọpụta ma see igbe gburugburu onye ọ bụla na foto](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/identify_and_draw_boxes_on_faces.py)
* [Tụlee ihu site na anya ihu ọnụọgụ karịa naanị eziokwu/ụgha ụgha](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_distance.py)
* [Mata ihu na vidiyo dị ndụ site na iji kamera weebụ gị - Ụdị dị mfe / nwayọ (chọrọ ka etinyere OpenCV)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam.py)
* [Mata ihu na vidiyo dị ndụ site na iji kamera weebụ gị - Ngwa ngwa ngwa (chọrọ ka etinyere OpenCV)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam_faster.py)
* [Mata ihu na faịlụ vidiyo wee dee faịlụ vidiyo ọhụrụ (chọrọ ka etinyere OpenCV)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_video_file.py)
* [Mata ihu na igwefoto Raspberry Pi w/](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_on_raspberry_pi.py)
* [Mee ọrụ webụ ka ịmata ihu site na HTTP (chọrọ ka etinyere flask)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/web_service_example.py)
* [Jiri ihe nhazi ndị agbata obi kacha nso mara ihu](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_knn.py)
* [Zụlite ọtụtụ onyonyo otu onye wee mata ihu site na iji SVM](https://github.com/Odsyesufu7/face_recognition/blob/master/emples/face_recognition_svm.py)

## Ịmepụta ihe kwụ ọtọ
- [Njikwa ihu na OpenCV, Python, na mmụta miri emi](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/) nke Adrian Rosebrock dere
   - Na-ekpuchi otu esi eji njirimara ihu na omume
- [Raspberry Pi Face Recognition](https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/) nke Adrian Rosebrock
   - Ekpuchi otu esi eji nke a na Raspberry Pi
- [ụyọkọ ihu na Python](https://www.pyimagesearch.com/2018/07/09/

ihu-clustering-na-python/) nke Adrian Rosebrock dere
   - Na-ekpuchi otu esi achịkọta foto na-akpaghị aka dabere na onye pụtara na foto ọ bụla site na iji mmụta anaghị elekọta ya

## Amụma

* A zụrụ ụdị njirimara ihu na ndị okenye na ọ naghị arụ ọrụ nke ọma na ụmụaka. Ọ na-achọ ịgwakọta
   ịzụlite ụmụaka n'ụzọ dị mfe iji ndabara ntụnyere 0.6.
* Izi ezi nwere ike ịdị iche n'etiti agbụrụ.

## <a name="deployment">Nkwanye na ndị ọbịa igwe ojii (Heroku, AWS, wdg)</a>

Ebe ọ bụ na 'ịmata ihu' dabere na 'dlib' nke edere na C++, ọ nwere ike ịdị aghụghọ ibuga ngwa.
iji ya na onye na-eweta igwe ojii dị ka Heroku ma ọ bụ AWS.

Iji mee ka ihe dịrị mfe, enwere ihe atụ Dockerfile na repo a na-egosi otu esi eme ngwa ejiri arụ ọrụ
'Ịmata_ihu' n'ime akpa [Docker](https://www.docker.com/). Na nke ahụ, ị ga-enwe ike ibuga
na ọrụ ọ bụla na-akwado onyonyo Docker.

Ị nwere ike ịnwale onyonyo Docker na mpaghara site na ịgba ọsọ: `docker-compose up --build'

Enwekwara [ọtụtụ onyonyo Docker emeburu.](docker/README.md)

Ndị ọrụ Linux nwere GPU (ndị ọkwọ ụgbọ ala> = 384.81) na [Nvidia-Docker] (https://github.com/NVIDIA/nvidia-docker) arụnyere nwere ike ịme ihe atụ na GPU: Mepee [docker-compose.yml] (docker-compose.yml) faịlụ ma kwupụta 'dockerfile: Dockerfile.gpu' na 'oge ọ na-agba ọsọ: nvidia'.

## Daalụ

* Ọtụtụ, ọtụtụ ekele Davis King [@nulhom]
   maka ịmepụta dlib na maka ịnye njirimara ihu a zụrụ azụ na ụdị mkpuchi ihu
   eji n'ọbá akwụkwọ a. Maka ozi ndị ọzọ na ResNet nke na-eme ka ngbanwe ihu, lelee
   ya [blog post](http://blog.dlib.net/2017/02/high-quality-face-recognition-with-deep.html).
* Ekele dịrị onye ọ bụla na-arụ ọrụ na ọba akwụkwọ sayensị data Python dị egwu dị ka ọnụọgụ, scipy, scikit-image,
   ohiri isi, wdg, wdg na-eme ka ụdị ihe a dị mfe ma na-atọ ụtọ na Python.
* Daalụ [Cookiecutter] Audreyrproject ndebiri
   maka ime ka ngwugwu ọrụ Python bụrụ nke a na-anabatakarị.

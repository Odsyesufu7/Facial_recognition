# Gane Fuska

_Zaku iya karanta fassarar fassarar wannan fayil ɗin [a cikin Swahili](https://github/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/README.md) da Harsunan Najeriya guda uku.

Gane da sarrafa fuskoki daga Python ko daga layin umarni tare da
ɗakin karatu mafi sauƙin fuska a duniya.

Gina ta amfani da [dlib](http://dlib.net/) gane fuska na zamani na zamani
gina tare da zurfin koyo. Samfurin yana da daidaito na 99.38% akan
[Labeled Faces in the Wild] a matsayin ma'auni.

Wannan kuma yana ba da kayan aikin layin umarni mai sauƙi 'face_recognition' wanda zai bari
kuna gane fuska akan babban fayil ɗin hotuna daga layin umarni!


[![PyPI](https://img.shields.io/pypi/v/face_recognition.svg)](https://pypi.python.org/pypi/face_recognition)
[![Yanayin Takardu](https://readthedocs.org/projects/face-recognition/badge/?version=latest)](http://face-recognition.readthedocs.io/en/latest/?badge=latest) )

## Fasali

#### Nemo fuskoki a hotuna

Nemo duk fuskokin da suka bayyana a hoto:

![](https://cloud.githubusercontent.com/assets/896692/23625227/42c65360-025d-11e7-94ea-b12f28cb34b4.png)

`` Python
shigo da face_recognition
hoto = face_recognition.load_image_file("your_file.jpg")
face_locations = face_recognition.face_locations(hoton)
```

#### Nemo ku sarrafa fasalin fuska a hotuna

Samo wurare da fassarorin idanun kowane mutum, hancinsa, baki da hancinsa.

![](https://cloud.githubusercontent.com/assets/896692/23625282/7f2d79dc-025d-11e7-8728-d8924596f8fa.png)

`` Python
shigo da face_recognition
hoto = face_recognition.load_image_file("your_file.jpg")
face_landmarks_list = face_recognition.face_landmarks(hoto)
```

Nemo fasalin fuska yana da matukar amfani ga abubuwa masu mahimmanci da yawa. Amma zaka iya amfani da shi don ainihin wawanci
kamar shafa [digital makeup](tunanin 'Meitu'):

![](https://cloud.githubusercontent.com/assets/896692/23625283/80638760-025d-11e7-80a2-1d2779f7ccab.png)

#### Gano fuskoki a hotuna

Gane wanda ya bayyana a kowane hoto.

![](https://cloud.githubusercontent.com/assets/896692/23625229/45e049b6-025d-11e7-89cc-8a71cf89e713.png)

`` Python
shigo da face_recognition
known_image = face_recognition.load_image_file("biden.jpg")
unknown_image = face_recognition.load_image_file("unknown.jpg")

biden_encoding = face_recognition.face_encodings(sani_image)[0]
unknown_encoding = face_recognition.face_encodings(unknown_image)[0]

sakamako = face_recognition.compare_faces([biden_encoding], unknown_encoding)
```

Kuna iya amfani da wannan ɗakin karatu tare da sauran ɗakunan karatu na Python don yin ainihin lokacin gane fuska:

![](https://cloud.githubusercontent.com/assets/896692/24430398/36f0e3f0-13cb-11e7-8258-4d0c9ce1e419.gif)

Duba [wannan misalin](https://github.com/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/examples/facerec_from_webcam_faster.py) don lambar.

## Demos na kan layi

Gudunmuwar da mai amfani ya ba da demo littafin rubutu na Jupyter (ba a tallafawa bisa hukuma): [![Deepnote](https://beta.deepnote.org/buttons/try-in-a-jupyter-notebook.svg)](https://beta) .deepnote.org/launch?template=face_recognition)

## Shigarwa

### Abubuwan Bukatu

   Python 3.3+ ko Python 2.7
   * MacOS, Linux da Windows ba a ba da shawarar ba amma kuma yana aiki.

### Zaɓuɓɓukan Shigarwa:

#### Shigarwa akan Mac ko Linux

Da farko, tabbatar cewa an riga an shigar da dlib tare da ɗaurin Python:

   * [Yadda ake shigar dlib daga tushe akan macOS ko Ubuntu](https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf)
  
Bayan haka, tabbatar cewa an shigar da cmake:
 
```fasa shigar cmake``

A ƙarshe, shigar da wannan ƙirar daga pypi ta amfani da `pip3` (ko `pip2` don Python 2):

``bash
pip3 shigar face_recognition
```

A madadin, zaku iya gwada wannan ɗakin karatu tare da [Docker](https://www.docker.com/), duba [wannan sashe](#deployment).



#### Shigarwa akan allon Nvidia Jetson Nano

  * [Jetson Nano umarnin shigarwa](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python -a25cb8c891fd)
    * Da fatan za a bi umarnin da ke cikin labarin a hankali. Akwai bug a halin yanzu a cikin ɗakunan karatu na CUDA akan Jetson Nano wanda zai sa wannan ɗakin karatu ya gaza shiru idan ba ku bi umarnin da ke cikin labarin ba don yin sharhi kan layi a dlib kuma ku sake tattara shi.

#### Shigarwa akan Rasberi Pi 2+

   * [Raspberry Pi 2+ umarnin shigarwa]

#### Shigarwa akan FreeBSD

``bash
pkg shigar graphics/py-face_recognition
```

#### Shigarwa akan Windows

Yayin da ba a tallafawa Windows bisa hukuma, masu amfani masu taimako sun sanya umarni kan yadda ake shigar da wannan ɗakin karatu:

   * [@masoudr's Windows 10 jagorar shigarwa (dlib + face_recognition)]

#### Ana shigar da hoton na'ura mai ba da hanya tsakanin hanyoyin sadarwa

   * [Zazzage hoton VM da aka riga aka tsara].

## Amfani

### Interface-Command-Line Interface

Lokacin da kuka shigar 'face_recognition', kuna samun layin umarni guda biyu masu sauƙi
shirye-shirye:

*'Gane_fuska' - Gane fuskoki a cikin hoto ko babban fayil cike don
    hotuna.
* Face

e_detection` - Nemo fuskoki a cikin hoto ko babban fayil cike da hotuna.

#### kayan aikin layin umarni 'fuska_gane

Umurnin 'gane_fuska' yana ba ku damar gane fuskoki a cikin hoto ko
babban fayil cike da hotuna.

Da farko, kuna buƙatar samar da babban fayil tare da hoto ɗaya na kowane mutum ku
riga sani. Ya kamata a sami fayil ɗin hoto guda ɗaya ga kowane mutum tare da
fayilolin mai suna bisa ga wanda ke cikin hoton:

![wanda aka sani](https://cloud.githubusercontent.com/assets/896692/23582466/8324810e-00df-11e7-82cf-41515eba704d.png)

Na gaba, kuna buƙatar babban fayil na biyu tare da fayilolin da kuke son ganowa:

![Ba a sani ba](https://cloud.githubusercontent.com/assets/896692/23582465/81f422f8-00df-11e7-8b0d-75364f641f58.png)

Sa'an nan kuma a cikin ku kawai ku aiwatar da umarni 'face_recognition', ku shiga
babban fayil na sanannun mutane da babban fayil (ko hoto ɗaya) wanda ba a sani ba
mutane kuma yana gaya muku wanda ke cikin kowane hoto:

``bash
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_mutumin
```

Akwai layi ɗaya a cikin fitarwa don kowace fuska. An raba bayanan waƙafi
tare da sunan fayil da sunan wanda aka samo.

Wani 'mutumin_wanda ba a sani ba' shine fuska a cikin hoton da bai dace da kowa a ciki ba
babban fayil ɗin ku na sanannun mutane.

#### kayan aikin layin umarni 'gane_face

Umurnin 'face_detection' yana baka damar nemo wurin (pixel coordinatates)
na kowace fuska a cikin hoto.

Kawai gudanar da umarni 'face_detection', wucewa cikin babban fayil na hotuna
don duba (ko hoto guda):

``bash
$ face_detection ./folder_with_pictures/

misalai/image1.jpg,65,215,169,112
misalai/image2.jpg,62,394,211,244
misalai/image2.jpg,95,941,244,792
```

Yana buga layi ɗaya don kowace fuska da aka gano. The daidaitawa
an ruwaito sune saman, dama, kasa da hagu na daidaitawar fuska (a cikin pixels).
 
##### Daidaita Haƙuri / Hankali

Idan kuna samun matches da yawa don mutum ɗaya, yana iya zama haka
Mutanen da ke cikin hotunanku suna kama da kamanni da ƙarancin haƙuri
ana buƙatar don sanya kwatancen fuska da ƙarfi.

Kuna iya yin hakan tare da ma'aunin '--tolerance'. Haƙuri na asali
ƙimar ita ce 0.6 kuma ƙananan lambobi suna sa kwatancen fuska da ƙarfi:

``bash
$ face_recognition --haƙuri 0.54 ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_mutumin
```

Idan kana son ganin an lissafta tazarar fuska don kowane wasa a jere
don daidaita saitin haƙuri, zaku iya amfani da `--show-distance gaskiya':

``bash
$ face_recognition --show-distance gaskiya ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg, Barack Obama, 0.378542298956785
/face_recognition_test/unknown_pictures/unknown.jpg,unknown_mutumin, Babu
```

##### Karin Misalai

Idan kawai kuna son sanin sunayen mutanen da ke cikin kowane hoto amma ba ku sani ba
damu game da sunayen fayil, kuna iya yin haka:

``bash
$ face_recognition ./pictures_of_people_i_sani/ ./unknown_pictures/ | yanke -d',' -f2

Barack Obama
wanda ba a sani ba
```

##### Gaggauta Gane Fuska

Ana iya gano fuskar fuska a layi daya idan kana da kwamfuta
mahara CPU cores. Misali, idan tsarin ku yana da muryoyin CPU guda 4, zaku iya
aiwatar da kusan sau 4 fiye da hotuna masu yawa a cikin adadin lokaci ɗaya ta amfani da
duk kwayoyin CPU ɗin ku a layi daya.

Idan kana amfani da Python 3.4 ko sabo, wuce cikin madaidaicin `--cpus <lambar_cpu_cores_to_use>`:

``bash
$ face_recognition --cpus 4 ./pictures_of_people_i_know/ ./unknown_pictures/
```

Hakanan zaka iya wucewa cikin '--cpus -1' don amfani da duk abin da ke cikin tsarin ku.

#### Python Module

Kuna iya shigo da tsarin 'face_recognition' sannan kuma a sauƙaƙe sarrafa
suna fuskantar layukan code guda biyu kawai. Yana da matukar sauki!

API Docs: [https://face-recognition.readthedocs.io](https://face-recognition.readthedocs.io/en/latest/face_recognition.html).

##### Nemo duk fuskokin hoto ta atomatik

`` Python
shigo da face_recognition

hoto = face_recognition.load_image_file("my_picture.jpg")
face_locations = face_recognition.face_locations(hoton)

# face_locations yanzu tsararru ce da ke jera abubuwan haɗin gwiwar kowace fuska!
```

Duba [wannan misalin](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
  don gwada shi.

Hakanan zaka iya ficewa zuwa samfurin gano fuska mai zurfi na tushen ilmantarwa.

Lura: Ana buƙatar haɓaka GPU (ta hanyar ɗakin karatu na CUDA na NVidia) don mai kyau
aiki tare da wannan samfurin. Hakanan kuna son kunna tallafin CUDA
lokacin da aka haɗa 'dlib'.

`` Python
shigo da face_recognition

hoto = face_recognition.load_image_file("my_picture.jpg")
face_locations = face_recognition.face_locations(hoto, samfurin = "cnn")

# face_locations yanzu tsararru ce da ke jera abubuwan haɗin gwiwar kowace fuska!
```

Duba [wannan misalin](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
  don gwada shi.

Idan kuna da hoto mai yawa

s da GPU, zaka iya kuma
[nemo fuskoki a batches](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py).

##### Gano yanayin fuskar mutum ta atomatik a cikin hoto

`` Python
shigo da face_recognition

hoto = face_recognition.load_image_file("my_picture.jpg")
face_landmarks_list = face_recognition.face_landmarks(hoto)

# face_landmarks_list yanzu jeri ne tare da wuraren kowane fasalin fuska a kowace fuska.
# face_landmarks_list[0]['left_eye'] zai zama wuri da sigar idon hagu na mutum na farko.
```

Duba [wannan misalin](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
  don gwada shi.

##### Gane fuskoki a cikin hotuna kuma gano su waye

`` Python
shigo da face_recognition

picture_of_me = face_recognition.load_image_file("me.jpg")
my_face_encoding = face_recognition.face_encodings(hoton_na)[0]

# Encoding_face_na yanzu yana dauke da ''encoding'' na fuskar fuskata wanda za'a iya kwatanta shi da kowane hoton fuska!

unknown_picture = face_recognition.load_image_file("unknown.jpg")
unknown_face_encoding = face_recognition.face_encodings(unknown_picture)[0]

# Yanzu muna iya ganin ɓangarorin fuskoki biyu na mutum ɗaya ne tare da 'kwatanta_fuskoki'!

sakamako = face_recognition.compare_faces([my_face_encoding], unknown_face_encoding)

idan sakamako[0] == Gaskiya:
     buga ("Hoton na ne!")
wani:
     buga ("Ba hotona bane!")
```

Duba [wannan misalin](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
  don gwada shi.

## Misalan Code Code

Duk misalan suna nan [a nan](https://github.com/Odsyesufu7/face_recognition/tree/master/emples).


#### Gane Fuska

* [Nemi fuskoki a cikin hoto](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
* [Nemi fuskoki a cikin hoto (ta amfani da zurfin koyo)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
* [Nemi fuskoki a cikin batches na hotuna tare da GPU (ta amfani da zurfin koyo)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py)
* [Blure duk fuskokin da ke cikin bidiyo kai tsaye ta amfani da kyamarar gidan yanar gizonku (yana buƙatar OpenCV don shigar da shi)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/blur_faces_on_webcam.py)

#### Fuskokin Fuska

* [Gano takamaiman fasalin fuska a hoto](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
* [Aiwatar (mummunan munin) kayan shafa na dijital](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/digital_makeup.py)

#### Gane Fuska

* [Nemo ku gane fuskokin da ba a san su ba a cikin hoto dangane da hotunan sanannun mutane](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
* [Gano kuma zana kwalaye kusa da kowane mutum a cikin hoto](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/identify_and_draw_boxes_on_faces.py)
* [ Kwatanta fuskoki da nisan fuska na lamba maimakon matches na Gaskiya/Ƙarya kawai](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_distance.py)
* [Gane fuskoki a cikin bidiyo kai tsaye ta amfani da kyamarar gidan yanar gizonku - Sauƙaƙe / Siffar Slower (yana buƙatar buɗewa da shigar da CV)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam.py)
* [Gane fuskoki a cikin bidiyo kai tsaye ta amfani da kyamarar gidan yanar gizonku - Faster Siffar (yana buƙatar OpenCV don shigar da shi)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam_faster.py)
* [Gane fuskoki a cikin fayil ɗin bidiyo kuma rubuta sabon fayil ɗin bidiyo (yana buƙatar OpenCV don shigar da shi)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_video_file.py)
* [Gane fuskoki akan Rasberi Pi w/ kamara](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_on_raspberry_pi.py)
* [Gudu da sabis na yanar gizo don gane fuskoki ta hanyar HTTP (yana buƙatar Flask don shigar da shi)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/web_service_example.py)
* [Gane fuskoki tare da mai rarraba maƙwabtan K-kusa](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_knn.py)
* [Kwatar da hotuna da yawa kowane mutum sannan ku gane fuskoki ta amfani da SVM](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_svm.py)

## Ƙirƙirar Mai Aiwatar da Kai tsaye
- [Ganewar fuska tare da OpenCV, Python, da zurfin koyo](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/) na Adrian Rosebrock
   - Ya ƙunshi yadda ake amfani da sanin fuska a aikace
- [Gane Fuskar Rasberi Pi](https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/) na Adrian Rosebrock
   - Ya ƙunshi yadda ake amfani da wannan akan Rasberi Pi
- [Tarin fuska tare da Python](https://www.pyimagesearch.com/2018/07/09/

fuska-clustering-da-python/) na Adrian Rosebrock
   - Yana rufe yadda ake tattara hotuna ta atomatik dangane da wanda ya bayyana a kowane hoto ta amfani da koyo mara kulawa

##Gaskiya

* An horar da samfurin gane fuska akan manya kuma baya aiki sosai akan yara. Yana son hadawa
   Haɓaka yara suna da sauƙi ta amfani da madaidaicin kwatancen 0.6.
* Daidaito na iya bambanta tsakanin kabilu.

## <a name="deployment">Aikewa zuwa Cloud Runduna (Heroku, AWS, da sauransu)</a>

Tunda 'gane_fuskar' ya dogara da 'dlib' wanda aka rubuta a C++, yana iya zama da wahala a tura app
amfani da shi zuwa mai ba da sabis na girgije kamar Heroku ko AWS.

Don sauƙaƙe abubuwa, akwai misali Dockerfile a cikin wannan repo wanda ke nuna yadda ake gudanar da ƙa'idar da aka gina da ita
'Gane_fuska' a cikin akwati [Docker] (https://www.docker.com/). Tare da wannan, ya kamata ku iya turawa
zuwa kowane sabis da ke goyan bayan hotunan Docker.

Kuna iya gwada hoton Docker a gida ta hanyar gudu: `docker-compose up --build'

Hakanan akwai [Hotunan Docker da yawa da aka riga aka gina su.](docker/README.md)

Masu amfani da Linux tare da GPU (dirabai> = 384.81) da [Nvidia-Docker] (https://github.com/NVIDIA/nvidia-docker) shigar zasu iya gudanar da misali akan GPU: Buɗe [docker-compose.yml] (docker-compose.yml) fayil kuma ba da amsa ga layin 'dockerfile: Dockerfile.gpu' da 'lokacin aiki: nvidia'.

## Mun gode

* Mutane da yawa, godiya ga Davis King [@nulhom]
   don ƙirƙirar dlib da kuma samar da horarrun gano fasalin fuska da samfuran ɓoye fuska
   amfani a cikin wannan ɗakin karatu. Don ƙarin bayani kan ResNet da ke ba da ikon rikodi na fuska, duba
   [blog post](http://blog.dlib.net/2017/02/high-quality-face-recognition-with-deep.html).
* Godiya ga duk wanda ke aiki akan duk manyan ɗakunan karatu na kimiyyar Python kamar su numpy, scipy, scikit-image,
   matashin kai, da sauransu, da sauransu wanda ke sa irin wannan kayan ya zama mai sauƙi da jin daɗi a Python.
* Godiya ga samfurin [Cookiecutter] Aureyrproject samfuri
   don sanya marufin aikin Python hanya mafi jurewa.

# Utambuzi wa Uso

_Unaweza pia kusoma toleo lililotafsiriwa la faili hii [kwa Kiswahili](https://github/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/README.md) na Lugha Tatu rasmi za Kinijeria.

Tambua na ubadilishe nyuso kutoka kwa Python au kutoka kwa safu ya amri na
maktaba rahisi zaidi ulimwenguni ya utambuzi wa uso.

Imejengwa kwa kutumia [dlib](http://dlib.net/) utambuzi wa uso wa hali ya juu
iliyojengwa kwa kujifunza kwa kina. Mfano huo una usahihi wa 99.38% kwenye
[Imeandikwa Nyuso Katika Pori] kama kigezo.

Hii pia hutoa zana rahisi ya amri ya `face_recognition` ambayo inaruhusu
unafanya utambuzi wa uso kwenye folda ya picha kutoka kwa safu ya amri!


[![PyPI](https://img.shields.io/pypi/v/face_recognition.svg)](https://pypi.python.org/pypi/face_recognition)
[![Hali ya Hati](https://readthedocs.org/projects/face-recognition/badge/?version=latest)](http://face-recognition.readthedocs.io/en/latest/?badge=latest )

## Vipengele

#### Tafuta nyuso katika picha

Tafuta nyuso zote zinazoonekana kwenye picha:

![](https://cloud.githubusercontent.com/assets/896692/23625227/42c65360-025d-11e7-94ea-b12f28cb34b4.png)

``` chatu
agiza utambulisho_wa_uso
picha = face_recognition.load_image_file("your_file.jpg")
face_locations = face_recognition.face_locations(picha)
```

#### Tafuta na ubadilishe vipengele vya uso katika picha

Pata maeneo na muhtasari wa macho, pua, mdomo na kidevu cha kila mtu.

![](https://cloud.githubusercontent.com/assets/896692/23625282/7f2d79dc-025d-11e7-8728-d8924596f8fa.png)

``` chatu
agiza utambulisho_wa_uso
picha = face_recognition.load_image_file("your_file.jpg")
face_landmarks_list = face_recognition.face_landmarks(picha)
```

Kupata vipengele vya uso ni muhimu sana kwa vitu vingi muhimu. Lakini pia unaweza kuitumia kwa mambo ya kijinga sana
kama kupaka [uundaji wa dijiti] (fikiria 'Meitu'):

![](https://cloud.githubusercontent.com/assets/896692/23625283/80638760-025d-11e7-80a2-1d2779f7ccab.png)

#### Tambua nyuso katika picha

Tambua ni nani anayeonekana katika kila picha.

![](https://cloud.githubusercontent.com/assets/896692/23625229/45e049b6-025d-11e7-89cc-8a71cf89e713.png)

``` chatu
agiza utambulisho_wa_uso
known_image = face_recognition.load_image_file("biden.jpg")
haijulikani_image = face_recognition.load_image_file("unknown.jpg")

biden_encoding = face_recognition.face_encodings(picha_inayojulikana)[0]
usimbaji_usiojulikana = face_recognition.face_encodings(picha_isiyojulikana)[0]

matokeo = face_recognition.compare_faces([biden_encoding], unknown_encoding)
```

Unaweza kutumia maktaba hii na maktaba zingine za Python kufanya utambuzi wa uso wa wakati halisi:

![](https://cloud.githubusercontent.com/assets/896692/24430398/36f0e3f0-13cb-11e7-8258-4d0c9ce1e419.gif)

Tazama [mfano huu](https://github.com/Odsyesufu7/Portfolio-Project-IoT_Cybersecurity/blob/master/examples/facerec_from_webcam_faster.py) kwa msimbo.

## Maonyesho ya Mtandaoni

Onyesho la daftari la Jupyter lililoshirikiwa na mtumiaji (halitumiki rasmi): [![Deepnote](https://beta.deepnote.org/buttons/try-in-a-jupyter-notebook.svg)](https://beta .deepnote.org/launch?template=face_recognition)

## Ufungaji

### Mahitaji

   * Chatu 3.3+ au Chatu 2.7
   * macOS, Linux na Windows imeungwa mkono bila kupendekezwa lakini pia inafanya kazi.

### Chaguzi za Usakinishaji:

#### Inasakinisha kwenye Mac au Linux

Kwanza, hakikisha kuwa tayari umesakinisha dlib na vifungo vya Python:

   * [Jinsi ya kusakinisha dlib kutoka chanzo kwenye macOS au Ubuntu](https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf)
  
Kisha, hakikisha umesakinisha cmake:
 
``` brew install cmake```

Mwishowe, sakinisha moduli hii kutoka kwa pypi kwa kutumia `pip3` (au `pip2` kwa Python 2):

```bashi
pip3 sakinisha face_recognition
```

Vinginevyo, unaweza kujaribu maktaba hii na [Docker](https://www.docker.com/), angalia [sehemu hii](#deployment).



#### Inasakinisha kwenye ubao wa Nvidia Jetson Nano

  * [Maagizo ya usakinishaji ya Jetson Nano](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python -a25cb8c891fd)
    * Tafadhali fuata maagizo katika makala kwa uangalifu. Hivi sasa kuna mdudu kwenye maktaba za CUDA kwenye Jetson Nano ambayo itasababisha maktaba hii kutofaulu kimya ikiwa hutafuata maagizo kwenye kifungu kutoa maoni kwenye mstari kwenye dlib na kuirudisha.

#### Inasakinisha kwenye Raspberry Pi 2+

   * [Raspberry Pi 2+ maagizo ya ufungaji]

#### Inasakinisha kwenye FreeBSD

```bashi
pkg sakinisha michoro/py-face_recognition
```

#### Inasakinisha kwenye Windows

Ingawa Windows haitumiki rasmi, watumiaji muhimu wamechapisha maagizo ya jinsi ya kusakinisha maktaba hii:

   * [mwongozo wa usakinishaji wa Windows 10 wa @masoudr (dlib + face_recognition)]

#### Inasakinisha picha ya Mashine Pepe iliyosanidiwa awali

   * [Pakua picha ya VM iliyosanidiwa awali].

##Matumizi

### Kiolesura cha Mstari wa Amri

Unaposakinisha `face_recognition`, unapata safu mbili za amri rahisi
programu:

* `face_recognition` - Tambua nyuso katika picha au folda iliyojaa
    picha.
* `uso

e_detection` - Tafuta nyuso katika picha au folda iliyojaa picha.

Zana ya amri ya #### `utambuzi_wa_uso`

Amri ya `face_recognition` hukuruhusu kutambua nyuso katika picha au
folda kamili kwa picha.

Kwanza, unahitaji kutoa folda na picha moja ya kila mtu wewe
tayari kujua. Kunapaswa kuwa na faili moja ya picha kwa kila mtu aliye na faili ya
faili zilizotajwa kulingana na aliye kwenye picha:

![inajulikana](https://cloud.githubusercontent.com/assets/896692/23582466/8324810e-00df-11e7-82cf-41515eba704d.png)

Ifuatayo, unahitaji folda ya pili na faili unazotaka kutambua:

![haijulikani](https://cloud.githubusercontent.com/assets/896692/23582465/81f422f8-00df-11e7-8b0d-75364f641f58.png)

Kisha ndani yako endesha tu amri `face_recognition`, kupita
folda ya watu wanaojulikana na folda (au picha moja) isiyojulikana
watu na inakuambia ni nani aliye katika kila picha:

```bashi
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,mtu_asiyejulikana
```

Kuna mstari mmoja kwenye pato kwa kila uso. Data imetenganishwa kwa koma
na jina la faili na jina la mtu aliyepatikana.

`Mtu_asiyejulikana` ni uso katika picha ambao haukulingana na mtu yeyote
folda yako ya watu wanaojulikana.

Zana ya amri ya #### `utambuzi_wa_uso`

Amri ya `face_detection` hukuruhusu kupata eneo (pixel coordinatates)
ya nyuso zozote kwenye picha.

Endesha tu amri `face_detection`, ukipita kwenye folda ya picha
kuangalia (au picha moja):

```bashi
$ face_detection ./folder_with_pictures/

mifano/picha1.jpg,65,215,169,112
mifano/picha2.jpg,62,394,211,244
mifano/picha2.jpg,95,941,244,792
```

Inachapisha mstari mmoja kwa kila uso uliogunduliwa. Viratibu
zilizoripotiwa ni viwianishi vya juu, kulia, chini na kushoto vya uso (katika saizi).
 
##### Kurekebisha Uvumilivu / Unyeti

Ikiwa unapata mechi nyingi za mtu mmoja, huenda ikawa hivyo
watu katika picha zako wanafanana sana na thamani ya chini ya uvumilivu
inahitajika kufanya ulinganisho wa uso kuwa mkali zaidi.

Unaweza kufanya hivyo na parameta ya `--tolerance`. Uvumilivu wa chaguo-msingi
thamani ni 0.6 na nambari za chini hufanya ulinganisho wa uso kuwa mkali zaidi:

```bashi
$ face_recognition --tolerance 0.54 ./pictures_of_people_i_know/ ./unknown_pictures/

/unknown_pictures/unknown.jpg,Barack Obama
/face_recognition_test/unknown_pictures/unknown.jpg,mtu_asiyejulikana
```

Ikiwa unataka kuona umbali wa uso uliohesabiwa kwa kila mechi kwa mpangilio
kurekebisha mpangilio wa uvumilivu, unaweza kutumia `--show-distance true`:

```bashi
$ face_recognition --show-distance true ./pictures_of_people_i_know/ ./unknown_pictures/

/picha_zisizojulikana/hazijulikani.jpg,Barack Obama,0.378542298956785
/face_recognition_test/unknown_pictures/unknown.jpg,mtu_asiyejulikana,Hakuna
```

##### Mifano Zaidi

Ikiwa unataka tu kujua majina ya watu katika kila picha lakini hutaki
kujali majina ya faili, unaweza kufanya hivi:

```bashi
$ face_recognition ./pictures_of_people_i_know/ ./unknown_pictures/ | kata -d ',' -f2

Barack Obama
mtu_asiyejulikana
```

##### Kuharakisha Utambuzi wa Uso

Utambuzi wa uso unaweza kufanywa kwa sambamba ikiwa una kompyuta nayo
cores nyingi za CPU. Kwa mfano, ikiwa mfumo wako una cores 4 za CPU, unaweza
kuchakata takriban mara 4 ya picha nyingi katika muda sawa kwa kutumia
cores zako zote za CPU sambamba.

Ikiwa unatumia Python 3.4 au mpya zaidi, pitisha `--cpus <number_of_cpu_cores_to_use>` parameta:

```bashi
$ face_recognition --cpus 4 ./pictures_of_people_i_know/ ./unknown_pictures/
```

Unaweza pia kupita katika `--cpus -1` ili kutumia cores zote za CPU kwenye mfumo wako.

#### Moduli ya Chatu

Unaweza kuleta moduli ya `face_recognition` kisha ubadilishe kwa urahisi
inakabiliwa na mistari michache tu ya msimbo. Ni rahisi sana!

Hati za API: [https://face-recognition.readthedocs.io](https://face-recognition.readthedocs.io/en/latest/face_recognition.html).

##### Pata nyuso zote kiotomatiki kwenye picha

``` chatu
agiza utambulisho_wa_uso

picha = face_recognition.load_image_file("my_picture.jpg")
face_locations = face_recognition.face_locations(picha)

# face_locations sasa ni safu inayoorodhesha viwianishi vya kila uso!
```

Tazama [mfano huu](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
  ili kuijaribu.

Unaweza pia kuchagua kuingia kwa muundo sahihi zaidi wa utambuzi wa uso unaotegemea mafunzo kwa kina.

Kumbuka: Uongezaji kasi wa GPU (kupitia maktaba ya CUDA ya NVidia) inahitajika kwa manufaa
utendaji na mtindo huu. Pia utataka kuwezesha usaidizi wa CUDA
wakati wa kukamilisha `dlib`.

``` chatu
agiza utambulisho_wa_uso

picha = face_recognition.load_image_file("my_picture.jpg")
face_locations = face_recognition.face_locations(picha, model="cnn")

# face_locations sasa ni safu inayoorodhesha viwianishi vya kila uso!
```

Tazama [mfano huu](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
  ili kuijaribu.

Ikiwa una picha nyingi

s na GPU, unaweza pia
[tafuta nyuso katika makundi](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py).

##### Tafuta kiotomatiki vipengele vya uso vya mtu kwenye picha

``` chatu
agiza utambulisho_wa_uso

picha = face_recognition.load_image_file("my_picture.jpg")
face_landmarks_list = face_recognition.face_landmarks(picha)

# orodha_ya_alama_za_alama sasa ni safu iliyo na maeneo ya kila kipengele cha uso katika kila uso.
# orodha_ya_alama_za_alama[0]['jicho_la_kushoto'] patakuwa mahali na muhtasari wa jicho la kushoto la mtu wa kwanza.
```

Tazama [mfano huu](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
  ili kuijaribu.

##### Kutambua nyuso katika picha na kutambua wao ni nani

``` chatu
agiza utambulisho_wa_uso

picha_ya_me = face_recognition.load_image_file("me.jpg")
my_face_encoding = face_recognition.face_encodings(picha_ya_mimi)[0]

# usimbaji_wa_uso_wangu sasa una 'encoding' ya jumla ya vipengele vyangu vya uso ambavyo vinaweza kulinganishwa na picha nyingine yoyote ya uso!

haijulikani_picture = face_recognition.load_image_file("unknown.jpg")
unknown_face_encoding = face_recognition.face_encodings(picha_isiyojulikana)[0]

# Sasa tunaweza kuona usimbaji wa nyuso mbili ni za mtu yule yule aliye na `linganisha_nyuso`!

matokeo = face_recognition.compare_faces([my_face_encoding], unknown_face_encoding)

ikiwa matokeo[0] == Kweli:
     print("Ni picha yangu!")
kwingine:
     print("Sio picha yangu!")
```

Tazama [mfano huu](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
  ili kuijaribu.

## Mifano ya Msimbo wa Python

Mifano yote inapatikana [hapa]( https://github.com/Odsyesufu7/face_recognition/tree/master/examples).


#### Utambuzi wa Uso

* [Tafuta nyuso katika picha](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture.py)
* [Tafuta nyuso katika picha (kwa kutumia mafunzo ya kina)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_picture_cnn.py)
* [Tafuta nyuso katika makundi ya picha na GPU (kwa kutumia mafunzo ya kina)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_faces_in_batches.py)
* [Weka ukungu kwenye nyuso zote katika video ya moja kwa moja kwa kutumia kamera yako ya wavuti (Inahitaji OpenCV kusakinishwa)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/blur_faces_on_webcam.py)

#### Sifa za Uso

* [Tambua vipengele mahususi vya uso katika picha](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/find_facial_features_in_picture.py)
* [Weka vipodozi vya kidijitali (mbaya sana) (https://github.com/Odsyesufu7/face_recognition/blob/master/examples/digital_makeup.py)

#### Utambuzi wa Uso

* [Tafuta na utambue nyuso zisizojulikana katika picha kulingana na picha za watu wanaojulikana](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/recognize_faces_in_pictures.py)
* [Tambua na uchore visanduku karibu na kila mtu katika picha](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/identify_and_draw_boxes_on_faces.py)
* [Linganisha nyuso kwa umbali wa uso wa nambari badala ya mechi za Kweli/Uongo pekee](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_distance.py)
* [Tambua nyuso katika video ya moja kwa moja kwa kutumia kamera yako ya wavuti - Toleo Rahisi / Polepole (Linahitaji OpenCV kusakinishwa)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam.py)
* [Tambua nyuso katika video ya moja kwa moja ukitumia kamera yako ya wavuti - Toleo la Haraka (Linahitaji OpenCV kusakinishwa)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam_faster.py)
* [Tambua nyuso katika faili ya video na uandike faili mpya ya video (Inahitaji OpenCV kusakinishwa)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_video_file.py)
* [Tambua nyuso kwenye kamera ya Raspberry Pi](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_on_raspberry_pi.py)
* [Endesha huduma ya wavuti ili kutambua nyuso kupitia HTTP (Inahitaji Flask kusakinishwa)](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/web_service_example.py)
* [Tambua nyuso ukitumia kiainishi cha majirani wa K-karibu zaidi](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_knn.py)
* [Zoeza picha nyingi kwa kila mtu kisha utambue nyuso kwa kutumia SVM](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/face_recognition_svm.py)

## Kuunda Kitekelezo Kinachojitegemea
- [Kutambua uso kwa OpenCV, Python, na kujifunza kwa kina](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/) na Adrian Rosebrock
   - Inashughulikia jinsi ya kutumia utambuzi wa uso katika mazoezi
- [Utambuzi wa Uso wa Raspberry Pi](https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/) na Adrian Rosebrock
   - Inashughulikia jinsi ya kutumia hii kwenye Raspberry Pi
- [Kuunganishwa kwa uso na Chatu](https://www.pyimagesearch.com/2018/07/09/

uso- nguzo-na-python/) na Adrian Rosebrock
   - Inashughulikia jinsi ya kuunganisha picha kiotomatiki kulingana na anayeonekana katika kila picha kwa kutumia mafunzo yasiyosimamiwa

## Tahadhari

* Mtindo wa utambuzi wa uso umefunzwa kwa watu wazima na haufanyi kazi vizuri sana kwa watoto. Inaelekea kuchanganya
   kuinua watoto kwa urahisi kwa kutumia kiwango cha ulinganishaji chaguo-msingi cha 0.6.
* Usahihi unaweza kutofautiana kati ya makabila.

## <a name="deployment">Kutumwa kwa Wapangishi wa Wingu (Heroku, AWS, n.k)</a>

Kwa kuwa `utambuzi_wa_uso` unategemea `dlib` ambayo imeandikwa kwa C++, inaweza kuwa gumu kupeleka programu.
kuitumia kwa mtoa huduma wa kupangisha wingu kama vile Heroku au AWS.

Ili kurahisisha mambo, kuna mfano wa Dockerfile kwenye repo hili ambao unaonyesha jinsi ya kuendesha programu iliyojengwa nayo
`face_recognition` katika chombo cha [Docker](https://www.docker.com/). Pamoja na hayo, unapaswa kuwa na uwezo wa kupeleka
kwa huduma yoyote inayotumia picha za Docker.

Unaweza kujaribu picha ya Docker ndani ya nchi kwa kukimbia: `docker-compose up --build`

Pia kuna [picha kadhaa za Docker zilizojengwa awali.](docker/README.md)

Watumiaji wa Linux walio na GPU (viendeshaji >= 384.81) na [Nvidia-Docker](https://github.com/NVIDIA/nvidia-docker) iliyosakinishwa wanaweza kutekeleza mfano kwenye GPU: Fungua [docker-compose.yml] (docker-compose.yml) na uondoe maoni ya mistari ya `dockerfile: Dockerfile.gpu` na `muda wa kukimbia: nvidia`.

## Asante

* Shukrani nyingi kwa Davis King [@nulhom]
   kwa kuunda dlib na kwa kutoa mafunzo ya utambuzi wa vipengele vya uso na miundo ya usimbaji wa nyuso
   kutumika katika maktaba hii. Kwa habari zaidi juu ya ResNet inayowezesha usimbaji wa uso, angalia
   [chapisho lake la blogi](http://blog.dlib.net/2017/02/high-quality-face-recognition-with-deep.html).
* Asante kwa kila mtu ambaye anafanya kazi kwenye maktaba zote nzuri za sayansi ya data ya Python kama vile numpy, scipy, scikit-picha,
   mto, nk, nk ambayo hufanya aina hii ya vitu kuwa rahisi na ya kufurahisha katika Python.
* Shukrani kwa [Cookiecutter] Audreyrproject template
   kwa kufanya ufungaji wa mradi wa Python uvumilie zaidi.

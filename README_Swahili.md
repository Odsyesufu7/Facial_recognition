# Utambuzi wa Uso

_Unaweza pia kusoma toleo lililotafsiriwa la faili hii [katika Kiswahili](https://github.com/m-i-k-i/face_recognition/blob/master/README_Swahili.md)._

Tambua na ubadilishe nyuso kutoka kwa Python au kutoka kwa safu ya amri na
maktaba rahisi zaidi duniani ya utambuzi wa nyuso.

Imejengwa kwa kutumia [dlib](http://dlib.net/) utambuzi wa uso wa hali ya juu
iliyojengwa kwa kujifunza kwa kina. Mfano huo una usahihi wa 99.38% kwenye
[Nyuso Zilizo na Lebo katika Pori](http://vis-www.cs.umass.edu/lfw/) kigezo.

Hii pia hutoa zana rahisi ya amri ya `face_recognition` ambayo inaruhusu
unafanya utambuzi wa uso kwenye folda ya picha kutoka kwa safu ya amri!


[![PyPI](https://img.shields.io/pypi/v/face_recognition.svg)](https://pypi.python.org/pypi/face_recognition)
[![Hali ya Kujenga](https://github.com/ageitgey/face_recognition/workflows/CI/badge.svg?branch=master&event=push)](https://github.com/ageitgey/face_recognition/actions?query =mtiririko wa kazi%3ACI)
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
kama vile kupaka [mapodozi ya kidijitali](https://github.com/Odsyesufu/face_recognition/blob/master/examples/digital_makeup.py) (fikiria 'Meitu'):

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

Tazama [mfano huu](https://github.com/Odsyesufu7/face_recognition/blob/master/examples/facerec_from_webcam_faster.py) kwa msimbo.

## Maonyesho ya Mtandaoni

Onyesho la daftari la Jupyter lililoshirikiwa na mtumiaji (halitumiki rasmi): [![Deepnote](https://beta.deepnote.org/buttons/try-in-a-jupyter-notebook.svg)](https://beta .deepnote.org/launch?template=face_recognition)

## Ufungaji

### Mahitaji

   * Chatu 3.3+ au Chatu 2.7
   * macOS au Linux (Windows haitumiki rasmi, lakini inaweza kufanya kazi)

### Chaguzi za Usakinishaji:

#### Inasakinisha kwenye Mac au Linux

Kwanza, hakikisha kuwa tayari umesakinisha dlib na vifungo vya Python:

   * [Jinsi ya kusakinisha dlib kutoka chanzo kwenye macOS au Ubuntu](https://gist.github.com/Odsyesufu7/629d75c1baac34dfa5ca2a1928a7aeaf)
  
Kisha, hakikisha umesakinisha cmake:
 
``` brew install cmake```

Mwishowe, sakinisha moduli hii kutoka kwa pypi kwa kutumia `pip3` (au `pip2` kwa Python 2):

```bashi
pip3 sakinisha face_recognition
```

Vinginevyo, unaweza kujaribu maktaba hii na [Docker](https://www.docker.com/), angalia [sehemu hii](#deployment).

Ikiwa una shida na usakinishaji, unaweza pia kujaribu a
[VM iliyosanidiwa awali](https://medium.com/@ageitgey/try-deep-learning-in-python-now-with-a-fully-pre-configured-vm-1d97d4c3e9b).

#### Inasakinisha kwenye ubao wa Nvidia Jetson Nano

  * [Maagizo ya usakinishaji ya Jetson Nano](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python -a25cb8c891fd)
    * Tafadhali fuata maagizo katika makala kwa uangalifu. Kuna hitilafu katika maktaba za CUDA kwenye Jetson Nano ambayo itasababisha maktaba hii kutofaulu kimya ikiwa hutafuata maagizo kwenye kifungu kutoa maoni kwenye mstari kwenye dlib na kuirudisha.

#### Inasakinisha kwenye Raspberry Pi 2+

   * [Maelekezo ya usakinishaji ya Raspberry Pi 2+](https://gist.github.com/Odsyesufu7/1ac8dbe8572f3f533df6269dab35df65)

#### Inasakinisha kwenye FreeBSD

```bashi
pkg sakinisha michoro/py-face_recognition
```

#### Inasakinisha kwenye Windows

Wakati Dirisha

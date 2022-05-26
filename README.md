# Practica-7 BUSES DE COMUNICACIÓN II

Les dades de so s'emmagatzemen un una matriu a la memòria RAM interna del nostre ESP32. 
I tot seguit utilitzem el protocol I2S (a través de la placa de connexió d'àudio) per a generar les dedas de so digital sense tenir pèrdues de qualitat

# Material

- ESP32
- Placa de connexió d'àudio MAX98357 I2S
- Altaveu

# Funcionament

Com podem observar al principi del codi, hem hagut de fer #include de diverses llibreries i capçaleres, una d'aquestes ñes el sampleaac.h,
per aconseguir que ens funcionés hem hagut d'afegir llibreries i ens ha creat un nou document al nostre src, com es pot comprovar al repositori.

'''
#include <Arduino.h>
#include "AudioGeneratorAAC.h"
#include "AudioOutputI2S.h"
#include "AudioFileSourcePROGMEM.h"
#include "sampleaac.h"
'''

Tot seguit, com es pot observar al codi, hem declarat els paràmetres d'etrada, sortida i la font d'àudio

Abans que es reprodueixi per l'altaveu hem d'establir un guany i assignar uns pins. El guany l'hem posat de 0.125 i hem establert els pins 26, 25 i 22.

Com veiem al final del loop, cada vegada que se'ns reprodueixi el so ens apareixerà "Sound Generator" per la sortida del port sèrie.

Tot es pot veure al vídeo adjuntat al repositori.

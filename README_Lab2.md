# Sistemes de Codificació d'Àudio i Video: Pràctica 2
**Instruccions per executar el fitxer**
1. Executeu el fitxer `P2-CarmeCorbi.py` especificant el número d'exercici com a argument. Per exemple, per executar l'Exercici 1, utilitzeu la següent comanda:
   ```python
   python3 P2-CarmeCorbi.py 1

## Exercici 1: Passar de MP4 a MP2 i guardar la informació
El propòsit d'aquest exercici implica la conversió d'un vídeo del format MP4 al format MP2 i guardar la informació del vídeo en un fitxer d'informació.




```python
# Executa l'exercici 1
python3 P2-CarmeCorbi.py 1
```
**Resultat de l'exercici 1:**

![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici1.png)


## Exercici 2: Redimensionar i reduir la qualitat d'imatges
El propòsit d'aquest exercici és crear una funció que faci servir FFmpeg per redimensionar una imatge a una nova amplada i alçada, així com per reduir la seva qualitat.
He creat una funció anomenada **resize_and_lower_quality** per redimensionar la imatge d'entrada a una nova amplada i sortida, així com es redueix la seva qualitat. Aquesta funció utilitza la comanda **ffmpeg -i image_entrada -vf 'scale=amplada:alcada' -q:v qualitat -frames:v 1 image_sortida**, on -i imatge_entrada especifica la imatge d'entrada, -vf 'scale=amplada:alcada' utilitza el filtre de vídeo FFmpeg per redimensionar la imatge amb una nova amplada i alçada, -q:v qualitat controla la qualitat de sortida de la imatge i -frame:v 1 limita la sortida a un únic frame.

Dins la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge d'entrada, la imatge de sortida, l'amplada,l'alçada i la qualitat, paràmetres que es poden modificar. Seguidament, es crida a la funció **resize_and_lower_quality**.

```python
# Executa l'exercici 2
python3 P2-CarmeCorbi.py 2
```
**Resultat de l'exercici 2:**

![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici2.JPG)

## Exercici 3: Llegir bytes d'una imatge amb patró serpentina
El proposit d'aquest exercici és crear una funció que llegueix els bytes d'una imatge en una patró serpertina, llegeix els bytes d'una imatge seguint un patró específic que serpenteja dreta i esquerra a travñes de les files i les columnes de la imatge.

He creat la funció **serpentine**  que llegeix els bytes d'una imatge seguint un patró de serpentina, zigzaguejant a través de les files i les columnes de la imatge. La funció a través d'un bucle recorre els bytes de la imatge seguint aquest patró.

Dins la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge que el vol utilitzar, aquesta es pot modificar. Seguidament, es crida a la funció **serpentine** i s'imprimeixen els primers 20 bytes.

```python
# Executa l'exercici 3
python3 P2-CarmeCorbi.py 3
```
**Resultat de l'exercici 3:**
![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici3.png)

## Exercici 4: Conversió d'imatges a blanc i negre i compressió extrema:
El proposit d'aquest exercici és crear una funció que utitzi FFmpeg per convertir una imatge a blanc i negre i aplicar una compressió extrema.

He creat la funció **convert_to_bw_width_hard_compression** per convertir la imatge d'entrada en blanc i negre i aplicar una compressió extrema. Aquesta funció utilitza la comanda **ffmpeg -i imatge_entrada -vf format=gray -crf 51 imatge_sortida** on -i imatge_entrada especifica la imatge d'entrada, -vf format=gray utilitza el filtre de vídeo de FFmpeg per convertir la imatge a blanc i negre, crf 51 controla la compressió de la imatge (un valor elevat com 51 representa una compressió extrema, el que resulta en una pèrdua significa).

Dins la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge d'entrada i el nom de la imatge de sortida. Seguidament, es crida la funció **convert_to_bw_with_hard_compression**.

```python
# Executa l'exercici 4
python3 P2-CarmeCorbi.py 4
```
**Resultat de l'exercici 4:**
![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici4.JPG)

## Exercici 5: Aplicar Run-Length-Encoding (RLE) a una seqüència de bytes
El propòsit d'aquest exercici és crear una funció que apliqui l'algorisme RLE a una seqüència de bytes. 

He creat la funció **codificacio_run_length**. Aquesta pren una seqüència de bytes i aplica l'algorisme RLE, aquest compta les repeticions consecutives del mateix valor i les emmagatzema com a parelles (valor, nombres de repeticions).

Dins de la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix una seqüència de bytes, la qual es pot modificar. Seguidament, es crida la funció **codificacio_run_length** i s'imprimeix aquesta seqüència RLE per pantalla.

```python
# Executa l'exercici 5
python3 P2-CarmeCorbi.py 5
```
**Resultat de l'exercici 5:**

![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici5.png)






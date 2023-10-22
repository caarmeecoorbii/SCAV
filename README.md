# Sistemes de Codificació d'Àudio i Video: Pràctica 1
**Instruccions per executar el fitxer**
1. Executeu el fitxer `rgb_yuv.py` especificant el número d'exercici com a argument. Per exemple, per executar l'Exercici 1, utilitzeu la següent comanda:
   ```python
   python3 rgb_yuv.py 1

## Exercici 1: Conversió de RGB a YUV
El propòsit d'aquest exercici és crear una funció que prengui tres valors RGB (Vermell, Verd i Blau) i els converteixi en els valors YUV. També s'ha de crear una funció per fer la inversa.
He creat dues funcions anomenades **rgb_to_yuv** i **yuv_to_rgb** on realitzen aquests càlculs. 

Dins de la funció **main** es verifica si es selecciona adequadament aquest exercici. S'assignen valors R,G,B i es criden a les dues funcions. Per posar altres valors, s'ha d'editar la funció **main**.

```python
# Executa l'exercici 1
python3 rgb_yuv.py 1
```
**Resultat de l'exercici 1:**

![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici1.png)


## Exercici 2: Redimensionar i reduir la qualitat d'imatges
El propòsit d'aquest exercici és crear una funció que faci servir FFmpeg per redimensionar una imatge a una nova amplada i alçada, així com per reduir la seva qualitat.
He creat una funció anomenada **resize_and_lower_quality** per redimensionar la imatge d'entrada a una nova amplada i sortida, així com es redueix la seva qualitat. Aquesta funció utilitza la comanda **ffmpeg -i image_entrada -vf 'scale=amplada:alcada' -q:v qualitat -frames:v 1 image_sortida**, on -i imatge_entrada especifica la imatge d'entrada, -vf 'scale=amplada:alcada' utilitza el filtre de vídeo FFmpeg per redimensionar la imatge amb una nova amplada i alçada, -q:v qualitat controla la qualitat de sortida de la imatge i -frame:v 1 limita la sortida a un únic frame.

Dins la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge d'entrada, la imatge de sortida, l'amplada,l'alçada i la qualitat, paràmetres que es poden modificar. Seguidament, es crida a la funció **resize_and_lower_quality**.

```python
# Executa l'exercici 2
python3 rgb_yuv.py 2
```
**Resultat de l'exercici 2:**

![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici2.JPG)

## Exercici 3: Llegir bytes d'una imatge amb patró serpentina
El proposit d'aquest exercici és crear una funció que llegueix els bytes d'una imatge en una patró serpertina, llegeix els bytes d'una imatge seguint un patró específic que serpenteja dreta i esquerra a travñes de les files i les columnes de la imatge.

He creat la funció **serpentine**  que llegeix els bytes d'una imatge seguint un patró de serpentina, zigzaguejant a través de les files i les columnes de la imatge. La funció a través d'un bucle recorre els bytes de la imatge seguint aquest patró.

Dins la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge que el vol utilitzar, aquesta es pot modificar. Seguidament, es crida a la funció **serpentine** i s'imprimeixen els primers 20 bytes.

```python
# Executa l'exercici 3
python3 rgb_yuv.py 3
```
**Resultat de l'exercici 3:**
![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici3.png)

## Exercici 4: Conversió d'imatges a blanc i negre i compressió extrema:
El proposit d'aquest exercici és crear una funció que utitzi FFmpeg per convertir una imatge a blanc i negre i aplicar una compressió extrema.

He creat la funció **convert_to_bw_width_hard_compression** per convertir la imatge d'entrada en blanc i negre i aplicar una compressió extrema. Aquesta funció utilitza la comanda **ffmpeg -i imatge_entrada -vf format=gray -crf 51 imatge_sortida** on -i imatge_entrada especifica la imatge d'entrada, -vf format=gray utilitza el filtre de vídeo de FFmpeg per convertir la imatge a blanc i negre, crf 51 controla la compressió de la imatge (un valor elevat com 51 representa una compressió extrema, el que resulta en una pèrdua significa).

Dins la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge d'entrada i el nom de la imatge de sortida. Seguidament, es crida la funció **convert_to_bw_with_hard_compression**.

```python
# Executa l'exercici 4
python3 rgb_yuv.py 4
```
**Resultat de l'exercici 4:**
![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici4.JPG)

## Exercici 5: Aplicar Run-Length-Encoding (RLE) a una seqüència de bytes
El propòsit d'aquest exercici és crear una funció que apliqui l'algorisme RLE a una seqüència de bytes. 

He creat la funció **codificacio_run_length**. Aquesta pren una seqüència de bytes i aplica l'algorisme RLE, aquest compta les repeticions consecutives del mateix valor i les emmagatzema com a parelles (valor, nombres de repeticions).

Dins de la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix una seqüència de bytes, la qual es pot modificar. Seguidament, es crida la funció **codificacio_run_length** i s'imprimeix aquesta seqüència RLE per pantalla.

```python
# Executa l'exercici 5
python3 rgb_yuv.py 5
```
**Resultat de l'exercici 5:**

![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici5.png)

## Exercici 6: Conversió de la DCT
El propòsit d'aquest exercici és crear una classe que realitza la DCT i la IDCT en una imatge.

He creat una classe anomenada **DCTConverter** que realitza la DCT i la IDCT en una imatge. Aquesta classe fa servir les llibreries **scipy.fftpack** per realitzar les transformades. Aquesta es defineixen dues funcions: **dct2** (aplica la DCT 2D a una imatge) i **idct2** (aplica la IDCT 2D a una imatge).

Dins de la funció **main** es verifica si es selecciona adequadament aquest exercici. Es defineix la imatge en la qual s'aplicarà les transformades. Seguidament, es criden a les funcions **dct2** i **idct2** de la classe DCTConverter. Per últim, es fa un plot amb la imatge d'entrada i la imatge reconstrüida després d'aplicar la IDCT a la imatge.

```python
# Executa l'exercici 6
python3 rgb_yuv.py 6
```
**Resultat de l'exercici 6:**
![](https://github.com/caarmeecoorbii/SCAV/blob/main/resultat_exercici6.png)




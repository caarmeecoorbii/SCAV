# Sistemes de Codificació d'Àudio i Video: Pràctica 1
**Instruccions per executar el fitxer**
1. Executeu el fitxer `rgb_yuv.py` especificant el número d'exercici com a argument. Per exemple, per executar l'Exercici 1, utilitzeu la següent comanda:
   ```python
   python3 rgb_yuv.py 1

## Exercici 1: Conversió de RGB a YUV
El proposit d'aquest exercici és crear una funció que prengui tres valors RGB (Vermell, Verd i Blau) i els converteixi en els valors YUV. També s'ha de crear una funció per fer la inversa.
He creat dues funcions anomenades **rgb_to_yuv** i **yuv_to_rgb**. Dins de la funció **main** es verifica si es selecciona adequadament aquest exercici. S'assignen valors R,G,B i es criden a les dues funcions. Per posar altres valors, s'ha d'editar la funció **main**.

```python
# Executa l'exercici 1
python3 rgb_yuv.py 1
```
## Exercici 2: Redimensionar i reduir la qualitat d'imatges
El proposit d'aquest exercici és crear una funció que faci servir FFmpeg per redimensionar una imatge a una nova amplada i alçada, així com per reduir la seva qualitat.
He creat una funció anomenada **resize_and_lower_quality** per redimensionar l'imatge d'entrada a una nova amplada i sortida, així com es redueix la seva qualitat. Aquesta funció utilitza la comanda **ffmpeg -i image_entrada -vf 'scale=amplada:alcada' -q:v qualitat -frames:v 1 image_sortida**, on -i imatge_entrada especifica la imatge d'entrada, -vf 'scale=amplada:alcada' utilitza el filtre de vídeo FFmpeg per redimensionar la imatge amb una nova amplada i alçada, -q:v qualitat controla la qualitat de sortida de la imatge i -frame:v 1 limita la sortida a un únic frame.

Dins la funció **main** es verifica si es selecciona adequadament aquest exxercici. Es defineix l'imatge d'entrada, l'imatge de sortida, l'amplada,l'alçada i la qualitat, paràmetres que es poden modifcar. Seguidament, es crida a la funció **resize_and_lower_quality**.

```python
# Executa l'exercici 2
python3 rgb_yuv.py 2
```

## Exercici 3: Llegir bytes d'una imatge amb patró serpentina
El proposit d'aquest exercici és crear una funció que llegueix els bytes d'una imatge en una patró serpertina, llegeix els bytes d'una imatge seguint un patró específic que serpenteja dreta i esquerra a travñes de les files i les columnes de la imatge.

```python
# Executa l'exercici 3
python3 rgb_yuv.py 3
````

## Exercici 4: Conversió d'imatges a blanc i negre i compressió extrema:
El proposit d'aquest exercici és crear una funció que utitzi FFmpeg per convertir una imatge a blanc i negre i aplicar una compressió extrema.

```python
# Executa l'exercici 4
python3 rgb_yuv.py 4
```

## Exercici 5: Aplicar Run-Length-Encoding (RLE) a una seqüència de bytes
El proposit d'aquest exercici és crear una funció que apliqui l¡algorisme RLE a una seqüència de bytes.

```python
# Executa l'exercici 5
python3 rgb_yuv.py 5
```

## Exercici 6: Conversió de la DCT
El proposit d'aquest exercici és crear una classe que realitza la DCT i la IDCT en una imatge.

```python
# Executa l'exercici 6
python3 rgb_yuv.py 6
```




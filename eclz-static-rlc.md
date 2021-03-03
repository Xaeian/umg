# Elektrolizer - Static + RLC

[Notobook python](./jupyter/eclz-static-rlc.ipynb)

## Charakterystyki statyczne

**Rodzina charakterystyk czasu osiągnięcia ciśnienia 0,2 Bara w funkcji napięcia**. Czas osiągnięcia ciśnienia jest powiązany z ilością wyprodukowanego wodoru i tlenu.

![time](./jupyter/png/eclz-static-time.png)

Widać, że stężenie nie ma wpływu na tę zależność — po prostu wraz ze zwiększaniem prądu przepływającego przez elektrolizer zwiększa się ilość wyprodukowanego wodoru.

**Rodzina charakterystyk rezystancji elektrolizera w funkcji napięcia**

![ohm](./jupyter/png/eclz-static-ohm.png)

Widzimy, że dla większych prądów elektrolizer posiada mniejszą rezystancję. Może to oznaczać, że bardziej wydajnie pracuje się na nim z wyższymi prądami. Obserwujemy też, że przy większym stężeniu rezystancja jest mniejsza.

**Rodzina charakterystyk prądowo-napięciowych elektrolizera w funkcji napięcia**

![ohm](./jupyter/png/eclz-static-volt.png)

## Charakterystyki RLC

**Rodzina charakterystyk modułu impedancji (lewo) oraz jej fazy (prawo) elektrolizera w funkcji częstotliwości**

![zfi](./jupyter/png/eclz-rlc-zfi.png)

**Rodzina charakterystyk indukcyjności (lewo) oraz rezystancji szeregowej (prawo) elektrolizera w funkcji częstotliwości**

![lsesr](./jupyter/png/eclz-rlc-lsesr.png)

## Spostrzerzenia

- Podczas zmiany punktu pracy prąd spada, a napięcie rośnie, co oznacza, że rezystancja elektrolizera również się zmienia.
- Ciekawą obserwacją jest, że podczas zwalniania zaworu prąd znacznie rośnie, a potem powoli spada. Może wyższe ciśnienie prowadzi, do zwiększenia rezystancji elektrolizera zmniejszając produkcję. Jednak podczas pomiaru przepływomierzem (bez zmiany ciśnienia) można było zaobserwować wahania przy zmianie punktu pracy. Tą zależność będzie można wyłapać za pomocą pomiarów rejestrowanych automatycznie w czasie rzeczywistym.

Dalej nie ma pomiarów, bo mostek się zacina — nie wiem do końca, z czego to wynika, ale jak trochę rozładowałem elektrolizer, to zaczął działać, ale tylko przez chwilę — i nie chciałem zmieniać stężenia roztowru, zanim będzie pewien pomiarów mostekm.

## Pomiary

### Stary roztwór KOH (nieznzne stężenie) 07.09.2020

**Pomiary mostkiem RLC**

| Freq[kHz] |  Z[Ω] | Fi[°] | Ls[uH] | ESR[Ω] |
| --------: | ----: | ----: | -----: | -----: |
|       0.1 | 0.030 | -56.3 |  -39.6 | 0.0166 |
|         1 | 0.032 |  64.6 |   4.66 | 0.0138 |
|        10 | 0.313 | 85.90 |   4.97 | 0.0701 |
|       100 | 3.023 | 88.67 |   4.81 |  0.119 |
|       200 |  5.98 | 88.86 |  4.764 |   0.12 |

**Pomiary statyczne**

|  I[A] | U[V] | Time |  R[Ω] |
| ----: | ---: | ---: | ----: |
|   4.9 | 2.27 | 8:57 | 0.463 |
|  7.97 | 2.46 | 5:10 | 0.309 |
|  11.9 | 2.86 | 3:27 |  0.24 |
| 16.46 | 3.22 | 2:36 | 0.196 |
| 20.15 | 3.45 |  2:2 | 0.171 |
| 25.03 | 3.75 | 1:39 |  0.15 |
| 29.96 | 3.86 | 1:13 | 0.129 |
| 35.03 | 3.93 |  1:0 | 0.112 |
| 39.58 | 4.02 | 0:50 | 0.102 |
| 44.79 | 4.15 | 0:42 | 0.093 |

### Woda destylowana (szczątkowe stężenie)

**Pomiary mostkiem RLC**

| Freq[kHz] | Z[Ω] |  Fi[°] | Ls[uH] | ESR[Ω] | Cp[uF] |  D[-] |
| --------: | ---: | -----: | -----: | -----: | -----: | ----: |
|       0.1 | 0.69 | -4.821 |    -94 |   0.69 |  192.5 | 11.85 |
|         1 | 0.68 |  1.688 |   3.22 |   0.69 |   -6.9 | 33.97 |
|        10 | 0.76 |  20.45 |    4.2 |   0.71 |  -7.28 |  2.69 |
|       100 | 2.51 |  39.91 |   2.56 |   1.92 | -0.407 | 1.194 |
|       200 |  3.4 |  26.64 |  1.217 |   3.05 | -0.105 | 1.991 |

**Pomiary statyczne**

|  I[A] |  U[V] |  Time |  R[Ω] |
| ----: | ----: | ----: | ----: |
|   3.9 |  6.53 | 11:10 | 1.674 |
|  5.01 |  7.33 | 08:30 | 1.463 |
| 6.979 | 8.919 | 05:52 | 1.278 |
| 7.599 | 9.129 | 05:11 | 1.201 |
| 8.679 | 9.699 | 04:20 | 1.118 |
| 10.23 | 10.32 | 03:46 | 1.009 |
| 12.13 | 11.38 | 03:09 | 0.938 |
|  13.7 | 12.11 | 02:38 | 0.884 |
| 15.16 | 12.49 | 02:31 | 0.824 |

W kolejnym pomiarze zostało odmierzone 20g KOH i zostało

### Roztwór KOH ~2‰

**Pomiary mostkiem RLC**

| Freq[kHz] |  Z[Ω] |  Fi[°] | Ls[uH] | ESR[Ω] | Cp[uF] |  D[-] |
| --------: | ----: | -----: | -----: | -----: | -----: | ----: |
|       0.1 | 0.121 | -10.44 | -48.12 | 0.0512 |  13660 | 1.678 |
|         1 | 0.050 |  29.93 |  3.946 | 0.0437 |  -1562 | 1.767 |
|        10 | 0.287 |  79.99 |    4.5 | 0.0506 | -54.52 | 0.179 |
|       100 | 2.736 |  87.96 |  4.352 | 0.0973 | -0.581 | 0.035 |
|       200 | 5.491 |  88.49 |  4.308 | 0.1446 | -0.147 | 0.026 |

**Pomiary statyczne**

|  I[A] | U[V] |  Time |  R[Ω] |
| ----: | ---: | ----: | ----: |
|  4.05 | 3.82 | 10:10 | 0.943 |
|  5.57 | 3.92 | 08:12 | 0.704 |
|  8.08 | 4.12 | 05:00 |  0.51 |
| 11.19 |  4.3 | 03:32 | 0.384 |
| 14.83 | 4.54 | 02:30 | 0.306 |
|  16.7 | 4.62 | 02:13 | 0.277 |
| 20.46 | 4.97 | 01:48 | 0.243 |
| 23.52 | 5.15 | 01:34 | 0.219 |
| 28.73 | 5.66 | 01:17 | 0.197 |
| 33.76 | 5.87 | 01:06 | 0.174 |
| 39.47 | 6.18 | 00:56 | 0.157 |
|  47.5 | 6.58 | 00:46 | 0.139 |
|  54.5 | 6.93 | 00:42 | 0.127 |
|  67.3 | 7.53 | 00:33 | 0.112 |
|  82.9 | 8.44 | 00:27 | 0.102 |

### Roztwór KOH ~5‰

**Pomiary mostkiem RLC**

| Freq[kHz] |  Z[Ω] |  Fi[°] | Ls[uH] | ESR[Ω] | Cp[uF] |  D[-] |
| --------: | ----: | -----: | -----: | -----: | -----: | ----: |
|       0.1 | 0.049 | -40.01 | -50.28 | 0.0382 |  20440 | 1.204 |
|         1 | 0.034 |  41.91 |  3.628 | 0.0254 |  -3115 | 1.116 |
|        10 | 0.287 |  83.83 |  4.559 | 0.0309 | -54.93 | 0.108 |
|       100 | 2.773 |  88.39 |  4.411 |  0.077 | -0.574 | 0.028 |
|       200 | 5.489 |  88.69 |  4.365 |  0.126 | -0.145 | 0.023 |

**Pomiary statyczne**

|  I[A] | U[V] |  Time |
| ----: | ---: | ----: |
|  0.08 | 1.83 |     - |
|  0.13 | 1.88 |     - |
|  0.20 | 1.96 |     - |
|  0.30 | 2.04 |     - |
|  0.50 | 2.21 |     - |
|  0.70 | 2.36 |     - |
|  0.90 | 2.49 |     - |
|  1.14 | 2.54 |     - |
|  1.49 |  2.8 |     - |
|  2.01 | 3.06 |     - |
|  2.93 | 3.57 |     - |
|  4.18 | 3.70 | 13:42 |
|  5.07 | 3.75 | 09.35 |
|  6.62 | 3.81 | 06:22 |
|  8.40 | 3.87 | 04:52 |
| 10.15 | 3.92 | 04:00 |
| 12.47 | 3.99 | 03:09 |
| 16.13 | 4.10 | 02:22 |
| 19.15 | 4.16 | 01:59 |
| 22.14 | 4.24 | 01:44 |
| 25.09 | 4.31 | 01:31 |
| 29.09 | 4.39 | 01:17 |
| 34.68 | 4.52 | 01:05 |
| 39.83 | 4.63 | 00:56 |
| 45.80 | 4.76 | 00:48 |
| 52.90 | 4.93 | 00:41 |
| 61.80 | 5.09 | 00:36 |
| 71.70 | 5.30 | 00:30 |
| 82.20 | 5.51 | 00:26 |

### Roztwór KOH ~10‰

**Pomiary mostkiem RLC**

| Freq[kHz] |  Z[Ω] |  Fi[°] | Ls[uH] | ESR[Ω] | Cp[uF] |   D[-] |
| --------: | ----: | -----: | -----: | -----: | -----: | -----: |
|       0.1 | 0.032 | -46.74 | -37.99 | 0.0223 |  35160 |  0.944 |
|         1 | 0.033 |  57.12 |  4.493 | 0.0181 |   3994 |  0.643 |
|        10 | 0.305 |  85.01 |  4.842 | 0.0265 | -51.93 |  0.087 |
|       100 | 2.933 |  88.41 |  4.666 | 0.0806 | -0.542 | 0.0275 |
|       200 | 5.800 |  88.67 |  4.615 | 0.1356 | -0.137 | 0.0232 |

**Pomiary statyczne**

|  I[A] | U[V] |  Time |
| ----: | ---: | ----: |
|  0.07 | 1.70 |     - |
|  0.10 | 1.77 |     - |
|  0.15 | 1.82 |     - |
|  0.20 | 1.85 |     - |
|  0.30 | 1.91 |     - |
|  0.50 | 1.98 |     - |
|  1.00 | 2.13 |     - |
|  1.51 | 2.30 |     - |
|  2.02 | 2.43 |     - |
|  2.55 | 2.55 |     - |
|  3.00 | 2.67 |     - |
|  3.51 | 2.80 |     - |
|  3.98 | 2.94 |     - |
|  4.35 | 3.47 | 15:54 |
|  5.36 | 3.59 | 09:59 |
|  6.63 | 3.67 | 07:26 |
|  7.99 | 3.74 | 05:48 |
| 10.38 | 3.81 | 04:15 |
| 12.09 | 3.85 | 03:32 |
| 14.02 | 3.91 | 03:02 |
| 17.00 | 3.97 | 02:25 |
| 20.79 | 4.06 | 01:57 |
| 25.60 | 4.15 | 01:34 |
| 30.30 | 4.23 | 01:17 |
| 36.09 | 4.33 | 01:04 |
| 41.60 | 4.42 | 00:54 |
| 50.50 | 4.57 | 00:44 |
|  61.7 | 4.74 | 00:36 |
|  61.7 | 4.84 | 00:36 |
|  73.5 | 4.90 | 00:28 |

class: middle, center, title-slide 
<br>
# Технології графічного процесінгу

Лекція 3: Вступ до CUDA C II

<br><br>
Кочура Юрій Петрович<br>
[iuriy.kochura@gmail.com](mailto:iuriy.kochura@gmail.com) <br>
<a href="https://t.me/y_kochura">@y_kochura</a> <br>

???
Прискорене обчислення на графічних процесорах (GPU) — це використання спеціалізованого комп’ютерного обладнання, графічного процесора, для виконання певних типів обчислень набагато швидше, ніж на центральному процесорі загального призначення (CPU).

У той час як центральні процесори розроблені для виконання широкого кола завдань, графічні процесори оптимізовані для обробки великих обсягів даних і виконання паралельних обчислень. Це робить графічні процесори ідеальними для таких завдань, як обробка графіки, наукове моделювання, машинне навчання та інші задачі, що потребують обробки великих даних.

У прискорених обчисленнях на графічному процесорі графічний процесор використовується для розвантаження частини обробки з центрального процесора з метою прискорення певних обчислень. Це робиться шляхом розбиття обчислення на безліч менших частин, які можуть оброблятися паралельно багатьма процесорними ядрами в GPU. Завдяки цьому обчислення, які могли тривати години або дні на центральному процесорі, можуть бути завершені за кілька хвилин або навіть секунд на графічному процесорі.

Загалом, прискорені обчислення на графічних процесорах дають змогу значно пришвидшити певні типи обчислень, за рахунок спеціалізованих можливостей графічних процесорів.

---

class: middle

# Сьогодні

- Координація паралельних потоків 
- Невідповідність розміру сітки
- Цикли: крок за сіткою

---


class: blue-slide, middle, center
count: false

.larger-xx[Координація паралельних потоків ]

---




class: middle

.center.width-110[![](figures/lec2/0.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c1.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c2.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c3.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c4.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c5.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c6.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c7.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c8.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c9.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c10.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c11.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c12.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c13.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c14.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c15.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c16.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c17.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c18.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c19.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c20.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/c21.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/c22.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---



class: middle

.center.width-100[![](figures/lec3/c23.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: blue-slide, middle, center
count: false

.larger-xx[Невідповідність розміру сітки]

---


class: middle

.center.width-100[![](figures/lec3/m1.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/m2.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/m3.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/m4.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/m6.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/m7.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/m8.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/m9.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/m10.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/m11.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/m12.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/m13.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---



class: blue-slide, middle, center
count: false

.larger-xx[Цикли: крок за сіткою]

---

class: middle

.center.width-100[![](figures/lec3/l1.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l2.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l3.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l4.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/l5.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l6.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l7.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/l8.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l9.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l10.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l11.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l12.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l13.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/l14.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class: middle

.center.width-100[![](figures/lec3/l15.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l16.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l17.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l18.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l19.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l20.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l21.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l22.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l23.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l24.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l25.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---

class: middle

.center.width-100[![](figures/lec3/l26.png)]

.footnote[Джерело слайду: NVIDIA, DLI]

---


class:  middle

## Приклад


```c++
__global__
void add(int n, float *x, float *y)
{
  int index = blockIdx.x * blockDim.x + threadIdx.x;
  int stride = blockDim.x * gridDim.x;
  for (int i = index; i < n; i += stride)
    y[i] = x[i] + y[i];
}

```
---


class: blue-slide, middle, center
count: false

.larger-xx[[Tesla K80 vs Tesla T4](https://technical.city/en/video/Tesla-K80-vs-Tesla-T4)]

.center.grid[
.smaller-x.kol-1-2[
<a href="https://colab.research.google.com/github/YKochura/ac-kpi/blob/main/tutor/lec2/DeviceQuery.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Colab: Tesla K80"/></a>
]

.smaller-x.kol-1-2[
<a href="https://colab.research.google.com/github/NVDLI/notebooks/blob/master/even-easier-cuda/An_Even_Easier_Introduction_to_CUDA.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
]
]

---


class: blue-slide, middle, center
count: false

.larger-xx[Глосарій]


---


# Глосарій


.smaller-xx[
- .bold[```cudaMallocManaged()```]: Функція CUDA для виділення пам'яті, доступної як для CPU, так і для GPUs. Пам’ять, виділена таким чином, називається уніфікованою пам’яттю (**unified memory**) і за потреби автоматично переміщується між CPU та GPUs.

- .bold[```cudaDeviceSynchronize()```]: Функція CUDA, яка змушує CPU чекати, поки GPU не закінчить роботу. 

- .bold[```Ядро (Kernel)```]: Функція CUDA, що виконується на GPU. 

- .bold[```Потік (Thread)```]: Одиниця виконання для ядер CUDA. 

- .bold[```Блок (Block)```]: Набір потоків. 

- .bold[```Сітка (Grid)```]: Набір блоків. 

]

---


class: end-slide, center
count: false

.larger-xx[Кінець 🏁]
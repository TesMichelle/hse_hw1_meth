### Сводная таблица

|  Sample  | 11347700-11367700 | 40185800-40195800 | Duplications |
|:--------:|:------------------|:------------------|:-------------|
| 8 cell   | 1090              | 464               | 18.3%        |
| Epiblast | 2328              | 1062              | 2.92%        |
| ICM      | 1456              | 630               | 9.08%        |

### Отличия данных метилирования и данных обычного секвенирования

Основные отличия в анализе прочтений видны в GC распределении и содержании
нуклеотидов. В данных метилирования эти показатели отклоняются от нормального
случая. Содержания тимина в данных метилирования заметно больше, а цитозина - меньше.
Это связано с тем, что метилированный цитозин прочитывается секвинатором как тимин.


Данные метилирования:
![Alt text](/imgs/gc_dist_methh.png?raw=true "Optional Title")
![Alt text](/imgs/sequence_content_meth.png?raw=true "Optional Title")
Обычные данные:
![Alt text](/imgs/gc_dist_normal.png?raw=true "Optional Title")
![Alt text](/imgs/sequence_content_normal.png?raw=true "Optional Title")

### M-bias plots

Графики m-bias используются для нахождения отклонений возникших из-за того, что
метилированный цитозин воспринимается секвинатором как тимин, или отклонения,
возникающего на 3' конце рида из-за особенностей секвинирования BS-seq.

На данных графиках мы наблюдаем как раз второй случай, где отклонение возникает на 3' конце (в начале второго рида).
![Alt text](/imgs/8_cell_m_bias_1.png?raw=true "Optional Title")
![Alt text](/imgs/8_cell_m_bias_2.png?raw=true "Optional Title")
![Alt text](/imgs/epiblast_m_bias_1.png?raw=true "Optional Title")
![Alt text](/imgs/epiblast_m_bias_2.png?raw=true "Optional Title")
![Alt text](/imgs/ICM_m_bias_1.png?raw=true "Optional Title")
![Alt text](/imgs/ICM_m_bias_2.png?raw=true "Optional Title")


### Уровень метилирования в образцах
Получившиеся гистограммы согласовываются с тем, что при раннем эмбриогенезе наблюдается
демитилирование (8 cell - 2.25 день => ICM - 3.5 день), затем в процесс имплантации происходит скачек метилирования (epiblast).
![Alt text](/imgs/histograms.png?raw=true "Optional Title")

### Google collab

https://colab.research.google.com/drive/1TambfUlhj37ByZWmyz2Xc9L7a8acSB_W?usp=sharing

### Сводная таблица

|  Sample  | 11347700-11367700 | 40185800-40195800 | Duplications |
|:--------:|:------------------|:------------------|:-------------|
| 8 cell   | 1090              | 464               | 18.3%        |
| Epiblast | 2328              | 1062              | 2.92%        |
| ICM      | 1456              | 630               | 9.08%        |

### Отличия данных метилирования от данных обычного секвенирования

Основные отличия в анализе прочтений видны в GC распределении и содержании
нуклеотидов. В данных метилирования эти показатели отклоняются от нормального
случая. Содержания тимина в данных метилирования заметно больше, а цитозина - меньше.
Это связано с тем, что метилированный цитозин прочитывается секвенатором как тимин.


Данные метилирования:
![Alt text](/imgs/gc_dist_methh.png?raw=true "Optional Title")
![Alt text](/imgs/sequence_content_meth.png?raw=true "Optional Title")
Обычные данные:
![Alt text](/imgs/gc_dist_normal.png?raw=true "Optional Title")
![Alt text](/imgs/sequence_content_normal.png?raw=true "Optional Title")

### M-bias plots

Графики m-bias могут быть использованы для нахождения отклонений, возникающих из-за того, что
метилированный цитозин воспринимается при выравнивании как тимин. Также на них можно обнаружить отклонения, возникающие из-за особенностей секвенирования BS-seq, на 3' конце рида.

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

Так в образцах 8 cell мы видим примерно симметричное распределение количества метилированных образцов с центром олоко 50%, затем в образцах ICM наблюдается сдвиг к ридам с более низким уровнем метилирования, а в epiblast наоборот - к ридам с более высоким.
![Alt text](/imgs/histograms.png?raw=true "Optional Title")


###Genome tracks
```
$ pyGenomeTracks --tracks bigwig.ini --region chr11:3800000-3850000 -o bigwig.png
```
![Alt text](/imgs/bigwig.png?raw=true "Optional Title")

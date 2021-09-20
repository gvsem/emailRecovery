# emailRecovery / Восстановление email

Со мной произошла поразительная история. Я сохранил черновик сообщения в Gmail Web, не отправил его. Возвращаюсь, а там текст следующего вида:

```
 ё ;  O  ? >  C ; 8 F 5  = 5 7 = 0 : > < > 9
   2 4 @ C 3  C A ; K H 0 ;  2 > @ > = 8 9  3 @ 0 9,
   7 2 > = K  ; N B = 8,  8  4 0 ; L = 8 5  3 @ > < K,
  5 @ 5 4 >  < = > N  ; 5 B 5 ;  B @ 0 < 2 0 9.
```

А ожидалось нечто подобное:

```
Шёл я по улице незнакомой
И вдруг услышал вороний грай,
И звоны лютни, и дальние громы,
Передо мною летел трамвай.
```

Чтобы исправить эту историю, я написал программу.

```
 ёл я по улице незнакомой
  вдруг услышал вороний грай,
  звоны лютни, и дальние громы,
 ередо мною летел трамвай.
```

К сожалению, восстановить заглавные буквы невозможно, но хотя бы можно уловить смысл сообщения. Usage:

```
python main.py sample2.txt
```

Если хотите прикольнуться и закодировать "в сторону зла", пожалуйста:

```
python main.py sample.txt --encode
```

## TODO

Это, на самом деле, оказался ASCII сдвиг на 176? символов.

Заглавные буквы потерялись из-за того, что они частично находились в области служебных символов.

В дальнейшем программу можно доработать именно на сдвиг символов.

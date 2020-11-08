# 3.2-Terminal.-Lesson-2

## 1. Cd

  Type cd - cd is a shell builtin
  Встроенная программа, которая выполняется непосредственно в оболочке

## 2. Pipe

  grep <some_string> <some_file> | wc -l
  
  обычно может быть переписан как что-то по линии
  something | grep -c .   # Notice that . is better than '..*'
  
  если все, что мы хотим сделать, это проверить, производятся ли какие-либо непустые         выходные линии) something
	something | grep . >/dev/null && ...
  
  ## 3. PID 1
  
  Init
  
  ## 4.

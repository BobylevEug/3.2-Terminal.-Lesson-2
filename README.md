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
  
  ## 4. Перенаправление
  
  Статья с перенаправлением https://www.opennet.ru/docs/RUS/bash_scripting_guide/c11620.html
  
  ls stderr > dev/pts/1 
  
  ## 5.
  
  echo 1234567890 0> File_In | File_In 1> File_Out 
  
  ## 6.
  
  
  ## 7.
  
  
  ## 8.
  
  
  ## 9. /proc/
  
  https://linux-faq.ru/page/specializirovannaya-fajlovaya-sistema-proc
  
  /proc/$$/environ
  файл, environ, содержащий информацию о переменных окружения процесса
  
  ## 10. /proc/
  
  - http://ashep.org/2011/nemnogo-ob-ispolzovanii-proc/#.X7LbAOVxfIU
  
  - /proc/<PID>/cmdline
  - В этом файле хранится командная строка, которой был запущен данный процесс;
  
  - /proc/<PID>/exe
  - представляет собой символическую ссылку на исполняемый файл, который инициировал запуск процесса;
  
  ## 11. cat /proc/cpuinfo | egrep "sse"
  
  https://habr.com/ru/post/109394/
  
  SSE 4.2
  https://dic.academic.ru/dic.nsf/ruwiki/746754

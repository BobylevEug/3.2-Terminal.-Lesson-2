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
  
  ls 2> dev/pts/1 
  
  ## 5.
  
  echo 456 > file546 | cat file456 > file654
    
  ## 6.
  
  по ssh работать не будет
  
  ## 7. bash 5>&1 echo netology > /proc/$$/fd/5
  
  Данными действиями мы перенаправляем все что в 5м дескрипторе bash в stdout, далее вывод команды echo перенаправляем в 5 дескриптор. результат netology на экране 
  
  ## 8.
  
  bash 50>&2 
  echo netology | /proc/$$/fd/50
  
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

  ## 12.
  
  Так как по умолчанию удаленный пользователь не является аутентифицированным, ssh сервер не запустит сразу shell (так как в этом случае любой мог бы получить доступ), а сначала вызовет login. ПОэтому и отображения на tty не будет.
  
  ## 13. reptyr
  
  https://codeby.net/threads/reptyr-vostanovlenie-utrachennoj-pty-ssh-sessii.72087/
  reptyr# ps -a
  reptyr# reptyr -T 28396
  
  ## 14. tee
  
  https://losst.ru/komanda-tee-linux
  https://zalinux.ru/?p=2333
  Служит для записи в один или несколько файлов. не работает перенапраление там, де нужны повышенные привилегии

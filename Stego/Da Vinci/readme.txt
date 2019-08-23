имеем monalisa.zip, Plans.jpg, Thepassword_is_the_small_name_of_the_actor_named_Hanks.jpg

1. steghide Thepassword_is_the_small_name_of_the_actor_named_Hanks.jpg (TOM) - получаем файл с паролем от архива (пароль это hash md5 - надо декодировать)
2. strings Plans.jpg - ссылка на YouTube (название видео без 3D)
3. binwalk monalisa.zip - видим, что это архив
4. unzip monalisa.zip - используем пароль из шага 1, получаем картинку
5. анализируем картинку из шага 4
6. steghide <картинка из шага 4> - пароль из шага 2, получаем файл
7. анализируем содержимое файла (base64)
8. декодируем содержимое, пока не получим флаг
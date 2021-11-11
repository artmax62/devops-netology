**/.terraform/*
будут игнорироваться все файлы в каталоге .terraform, в каких бы поддиректориях проекта он не располагался.

*.tfstate
*.tfstate.*
игнорируются все файлы с расширением tfstate, а так же файлы любых расширений, в названии которых встречается .tfstate

crash.log
игнорируется файл crash.log во всех вложенных подкаталогах

*.tfvars
Все файлы с расширением tfvars во всех вложенных каталогах

override.tf
override.tf.json
*_override.tf
*_override.tf.json
Игнорятся файлы с названиями override.tf и override.tf.json, а так же все файлы, название которых содержит _override.tf или _override.tf.json

.terraformrc
terraform.rc
Игнорятся вышеуказанные файлы во всех вложенных подкаталогах

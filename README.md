В файле docker-compose.yaml описано основное окружение из контейнеров необходимое для работы описанного проекта. 
Контейнеры для php и node.js собираются из своих собственных докерфайлов, в которых прописана установка всех необходимых зависимостей(composer для php, npm для Node.js и т.д.) 
Созданы сети для изоляции бека и остальное для фронта, так как для базы и редиса идет обращение только с помощью php, но все это должны быть доступно для веб-сервера так что ему доступны две сети.
В конейнер с nginx копируется все необходимое в том числе и файл конфига default.conf

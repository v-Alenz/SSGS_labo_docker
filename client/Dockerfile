#
#   DOCKERFILE - Scheduling App Client
# 
#   Programma sviluppato come parte del progetto su Docker
#   per il corso di SSGS dell'Universiota' degli Studi di Genova 
#
#   Copyright (C) <2023>  Andrea Valenzano 4548315
#   Copyright (C) <2023>  Nicola Incardona DAMETTERE
#
#   This program is free software: you can redistribute it and/or modify
#   it under the terms of the GNU Affero General Public License as
#   published by the Free Software Foundation, either version 3 of the
#   License, or (at your option) any later version.
#
#   This program is distributed in the hope that it will be useful,
#   but WITHOUT ANY WARRANTY; without even the implied warranty of
#   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#   GNU Affero General Public License for more details.
#
#   You should have received a copy of the GNU Affero General Public License
#   along with this program.  If not, see <https://www.gnu.org/licenses/>.
#

FROM node:19-bullseye

RUN bin/bash -c 'cd home/node/; \
git clone https://github.com/novuhq/blog.git; \
mv  blog/scheduling-app-with-react-nodejs-emailjs/client client_build; \
yes | rm -r blog/; \
cd client_build; \
npm install --loglevel info; \
npm run build  --loglevel info; \
npm install -g serve --loglevel info; \
echo -e "#!/bin/bash\nserve -s /home/node/client_build/build" > startup.sh; \ 
chmod +x startup.sh;'

ENTRYPOINT [ "/home/node/client_build/startup.sh" ]


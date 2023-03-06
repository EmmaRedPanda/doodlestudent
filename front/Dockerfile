FROM ubuntu As originelle

RUN apt-get update \
&& apt-get install -y git \
&& apt-get install -y nodejs \
&& apt-get install -y npm

RUN git clone https://github.com/EmmaRedPanda/doodlestudent.git

WORKDIR /doodlestudent/front

RUN npm install
RUN npm run build

FROM nginx As courant

COPY --from=originelle /doodlestudent/front/dist/tlcfront /usr/share/nginx/html


# Admitech

![Logo admmitech](https://user-images.githubusercontent.com/32480223/67026906-f68d5280-f108-11e9-8d42-b9a836db4a4b.png)

Recrutment platform for IG & DO courses in Polytech Montpellier

Team : Lucas Gonçalves, Inès Missoum, Fatima Machhouri, Thomas Falcone, Raphael
Luciano, Martin Cayuelas

# Deploy

For information:
```
apps:create mail-admitech
apps:create test-mail-admitech

docker-options:add mail-admitech build --build-arg "DD_API_KEY=<datadog api key>"
docker-options:add test-mail-admitech build --build-arg "DD_API_KEY=<datadog api key>"

config:set mail-admitech DD_API_KEY=<datadog api key>
config:set test-mail-admitech DD_API_KEY=<datadog api key>

proxy:ports-add mail-admitech http:80:3000
proxy:ports-add test-mail-admitech http:80:3000
```
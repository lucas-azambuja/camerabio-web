# CameraBio Web

Este projeto visa facilitar a implementação do frame de captura biométrica via JavaScript PURO. 

## Começando

Estas instruções farão com que você consiga implementar a câmera com engenharia biométrica pré-existente e obter/manipular os dados de retorno.
 
### Instalando

A instalação e implementação de nossa ferramente é muito simples e em poucos passos o seu frame está pronto para ser utilizado. 

- Adicione o nosso projeto a sua maquina através de um Git clone ou download do mesmo. 
- Escolha uma das versões que deseja implementar. 
  - web: para landscape e indicado para e dashboards. 
  - mob: para frame adaptado a dispositivos móveis.
- Forneça um caminho de pasta para o carregamento de nossos arquivos de modelos. Para isto, abra o arquivo frame.js e procure pela linha:

```javascript
  faceapi.nets.tinyFaceDetector.loadFromUri('{SEU_CAMINHO_DE_PASTAS_AQUI}/mob/models'),
````
 altere de acordo com a necessidade. Geralmente já funciona da forma padrão:
 ```
  faceapi.nets.tinyFaceDetector.loadFromUri('../mob/models'),
```

Pronto! O seu projeto já está pronto para o uso de nossa ferramenta. 

### Manuseio

Para manipular o base64 da imagem capturada, adicione ao seu arquivo os métodos:

  ```
    function onSuccessCapture(base64) {
      console.log(base64);
    }

    function onFailedCapture(err) {
      console.log(err);
    }
```
 - Deixamos exemplificados a implementação no arquivo index.html
 

## DEMO - Dispositivo móvel

* [Clique aqui para abrir a demonstração](https://crediariohomolog.acesso.io/camerabio-web/mob/)

## Construido com

* [face-api.js](https://github.com/justadudewhohacks/face-api.js) - Framework de análise bimétrica.


## Versionamento

Nós usamos [Github](https://github.com/) para versionar. Para as versões disponíveis, veja as [tags do repositório](https://github.com/acesso-io/camerabio-android/releases). 

## Autores

* **Matheus Domingos** - *Engenheiro Mobile* - [GitHub](https://github.com/MatheusDomingos)

Veja também nossa lista de [contribuidores](https://github.com/acesso-io/camerabio-android/graphs/contributors) que participaram deste projeto.

## Licença

Este proje é licenciado pela MIT License - veja [LICENSE.md](LICENSE.md) o arquivo para detalhes

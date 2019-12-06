# CameraBio Web

Este projeto visa facilitar a implementação do frame de captura biométrica via JavaScript nativo através de algoritimos de visão computacional. Ajudando desta forma no melhor enquadramento para captura e otimizando as imagens antes de serem enviadas ao motor de biometria.  

## Começando

Estas instruções farão com que você consiga implementar a câmera com engenharia biométrica pré-existente e obter/manipular os dados de retorno.
 
Esta biblioteca utiliza os recursos nativos do HTML 5 e funciona apenas em browsers modernos.


## Compatibilidade 

- A partir do iOS 11.0 e Android 5.0.
- Para a versão web, oferecemos suporte nativamente em navegadores modernos (Google Chrome, Firefox, Opera, Edge) e mobile Safari para iOS e Google Chrome para Android. 
- Browsers com suporte a WebRTC. 

#### Observação: Nosso algoritimo de visão computacional detecta em tempo real as caracteriscticas do devie o qual está sendo executado e coleta informacoes de memória e processamento afim de detectar a compatibidade adequada a ferramenta. Em casos de NÃO COMPATIBILIDADE identificada pelo algoritimo, a ferramenta irá retornar para o frame antigo, exibindo a silhueta do rosto.  


 ## Características

- Exibe um quadro azul ou vermelho, orientando o usuário a posicionar melhor o rosto para a captura da foto. Caso o browser do dispositivo não possua suporte (como descrito na sessão de compatibilidade), exibimos uma silhueta do rosto para indicar onde a pessoa deve posicionar a face durante a captura.
- Permite utilizar a câmera frontal de dispositivos móveis.

 
### Instalando

A instalação e implementação de nossa ferramente em seu projeto é muito simples e em poucos passos o seu frame estará pronto para ser utilizado. Segue abaixo: 

- Adicione o nosso projeto a sua maquina através de um Git clone ou download do mesmo. 
- Escolha uma das versões que deseja implementar. 
  - web: para landscape e indicado para e dashboards. 
  - mob: para frame adaptado a dispositivos móveis.
- Forneça um caminho de pasta para o carregamento de nossos arquivos de modelos. Para isto, abra o arquivo frame.js e procure pela linha:

```javascript
  faceapi.nets.tinyFaceDetector.loadFromUri('{SEU_CAMINHO_DE_PASTAS_AQUI}/mob/models'),
````
 altere de acordo com a necessidade. Geralmente já funciona da forma padrão:
 ```javascript
  faceapi.nets.tinyFaceDetector.loadFromUri('../mob/models'),
```

Pronto! O seu projeto já está pronto para o uso de nossa ferramenta. 

### Manuseio

Para manipular o base64 da imagem capturada, adicione ao seu arquivo os métodos e aponte desta forma:

  ```javascript
    onSuccessCaptureAtFrame = onSuccessCapture;

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

## DEMO - WebCam

* [Clique aqui para abrir a demonstração](https://crediariohomolog.acesso.io/camerabio-web/web/)

## Construido com

* [face-api.js](https://github.com/justadudewhohacks/face-api.js) - Framework de análise bimétrica.


## Versionamento

Nós usamos [Github](https://github.com/) para versionar. Para as versões disponíveis, veja as [tags do repositório](https://github.com/acesso-io/camerabio-android/releases). 

## Autores

* **Matheus Domingos** - *Engenheiro Mobile* - [GitHub](https://github.com/MatheusDomingos)

Veja também nossa lista de [contribuidores](https://github.com/acesso-io/camerabio-android/graphs/contributors) que participaram deste projeto.

## Licença

Este proje é licenciado pela MIT License - veja [LICENSE.md](LICENSE.md) o arquivo para detalhes

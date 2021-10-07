# # PRO-FUC-Criando_um_socket_java
# O que é um Socket? 
É um serviço de transporte que permite a comunicação através do protocolo TCP entre clientes e servidores. Cada cliente e servidor possuem seu socket que irá possibilitar uma conexão fim a fim. Podemos entender que sockets são terminais em uma conexão bidirecional, a mensagem sai de um computador ou aplicativo A e chega ao seu fim em um computador ou aplicativo B. Todo socket possui dois tipos de endereçamento: Endereço Local: Endereço da porta de comunicação para a camada de transporte. Endereço Global: Endereço do computador na rede.

## Então em cima desse conhecimento estarei simulando a conexão de cliente e servidor, criando assim um socket para prova de conceito.
Utilizarei linguagem Java e em outro repositorio estarei desenvolvendo o mesmo projeto em C.
será baseado nesse contexto, relacionado ao SOAP. Segue abaixo o exemplo.

## EXEMPLO
    Abaixo, temos um exemplo de requisição de um cliente a um servidor apenas iniciando uma
    simples comunicação:
    POST /EnviandoHelloWord/endpoint HTTP/1.1
    Host: (aqui irá o endereço do destinatário)
    Content-Type: text/XML; charset=”utf-8”
    Content-Length: 322
    Cabeçalho:
    <soapenv:Envelope xmlns:soapenv=http://schemas.xmlsoap.org/soap/envelope/
     xmlns:xsd=http://www.w3.org/2001/XMLSchema
     xmlns:ns1=http://hello>
    Corpo:
     <soapenv:Body>
     <ns1:sayHello>
     <ns1:name>Olá</ns1:name>
     </ns1:sayHello>
     </soapenv:Body>
     </soapenv:Envelope>
     
## Vejamos agora a resposta do Servidor:
    HTTP/1.1 200 OK
    Content-Type: text/XML; charset=”utf-8”
    Content-Length: 367
    Cabeçalho:
    <soapenv:Envelope xmlns:soapenv=http://schemas.xmlsoap.org/soap/envelope/
    xmlns:xsd=http://www.w3.org/2001/XMLSchema
    xmlns:ns1=http://hello>
    Corpo:
    <soapenv:Body>
    <ns1:sayHelloResponse>
    <ns1:return>Olá, Tudo bem?</ns1:return>
    </ns1:sayHelloResponse>
    </soapenv:Body>
    </soapenv:Envelope>


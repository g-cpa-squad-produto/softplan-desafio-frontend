# Desafio implementador front-end: React, HTML, CSS & JS

Seja parte da jornada de transformação digital no Brasil.

Esse é o nosso desafio para a vaga de implementador front-end na [Softplan](https://www.softplan.com.br/carreira/). Serão testadas as habilidades e qualidade de código ao transformar um layout em uma **SPA**.

Procuramos desenvolvedor versátil para resolver os mais diversos problemas, que impactam no negócio do cliente, utilizando conhecimento em tecnologias front-end como meio para isso. Sinta-se confortável com desafios e seja engajado com o que há de melhor no mercado e boas práticas para trabalhar com inovação, tecnologias modernas e emergentes na Softplan, empresa no Top 10 dos melhores lugares para se trabalhar em Santa Catarina (GPTW 2017).

### O que você traz?
- Perfil proativo, saber trabalhar em equipe , raciocínio lógico, responsabilidade e comprometimento são imprescindíveis para essa oportunidade.
- Fácil adaptação em projetos experimentais e complexos.
- Aprendizado rápido no uso de tecnologias de desenvolvimento de software
- Experiência em Desenvolvimento de software Web

### O que oferecemos
- Oportunidade de desenvolvimento profissional, meet ups, capacitação e treinamento in-company
- Apoio no seu crescimento e aprendizado com bolsas de graduação, pós-graduação e verba para cursos e eventos de aprendizado externos
- Plano de bonificação por atingimento de metas
- Biblioteca colaborativa
- Ginástica laboral
- No dress code
- Parcerias com desconto em academias, restaurantes, salão de beleza, etc.
- Espaço para refeições, com geladeira e microondas
- Vale alimentação/refeição, auxílio transporte, assistência médica e odontológica


### Instruções para o desafio

- **Fork** esse repositório e faça o desafio numa branch com o seu nome (exemplo: `nome-sobrenome`)
- Assim que concluir o seu desafio, abra um **pull request** com suas alterações


### Desafio
- O desafio consiste em implementar uma *SPA* a partir de um layout pré-estabelecido, conforme abaixo:
    - Realizar uma consulta de processos e visualizar o resultado
    - Visualizar os detalhes de processo
    - Inserir, editar e excluir um processo
- Siga os [protótipos](https://www.figma.com/proto/BTa9Vpz4S1XUscURxANvFH5Z/DESAFIO?node-id=19%3A70&scaling=scale-down&redirected=1) e o [guideline](https://www.figma.com/proto/BTa9Vpz4S1XUscURxANvFH5Z/DESAFIO?node-id=27%3A1&scaling=contain&redirected=1) disponibilizados ao máximo


### O que será avaliado
- O código será avaliado seguindo os seguintes critérios: manutenabilidade, clareza e limpeza de código; resultado funcional; entre outros fatores
- O histórico no `git` também está avaliado
- Não esqueça de documentar o processo necessário para rodar a aplicação
- Apesar de não ter uma limitação de tempo, recomendamos não investir mais de 16 horas de trabalho nesse desafio
- Se necessário explique as decisões técnicas tomadas, as escolhas por bibliotecas e ferrramentas, o uso de patterns etc. 


### Considerações 
- Considerar que os seguintes endpoints estão disponíveis (`docker run -p 3002:3002 gcpasquadproduto/softplan-desafio-frontend`)
```
$ curl -i -X POST http://localhost:3002/processo \
        -H 'accept: application/json' \
        -H 'content-type: application/json' \
        -d '{"descricao" : "Solicitação de licença-prêmio", "assunto" : "Licença", "interessados" : ["Edmilson Cherem"]}'

HTTP/1.1 201 
Location: http://localhost:3002/processo/04c7197f-c0fe-4dab-b27c-d69611eca40f
Content-Length: 0
Date: Tue, 07 Aug 2018 20:26:22 GMT
```

```
$ curl -i -X GET http://localhost:3002/processo/04c7197f-c0fe-4dab-b27c-d69611eca40f

HTTP/1.1 200 
Content-Type: application/json;charset=UTF-8
Transfer-Encoding: chunked
Date: Tue, 07 Aug 2018 20:32:59 GMT
{
    "id": "04c7197f-c0fe-4dab-b27c-d69611eca40f",
    "numero": "SOFT 2018/00008",
    "entrada": "07/08/2018",
    "descricao": "Solicitação de licença-prêmio",
    "assunto" : "Licença",
    "interessados": ["Edmilson Cherem"]
}
```

```
curl -i -X GET http://localhost:3002/processo?q=licenca \
  -H 'accept: application/json' \
  -H 'content-type: application/json'

HTTP/1.1 200 
Content-Type: application/json;charset=UTF-8
Transfer-Encoding: chunked
Date: Tue, 07 Aug 2018 20:29:43 GMT
[
    {
        "id": "04c7197f-c0fe-4dab-b27c-d69611eca40f",
        "numero": "SOFT 2018/00008",
        "entrada": "07/08/2018",
        "descricao": "Solicitação de licença-prêmio",
        "assunto" : "Licença",
    	"interessados": ["Edmilson Cherem"]
    }
]
```

```
$ curl -i -X DELETE http://localhost:3002/processo/04c7197f-c0fe-4dab-b27c-d69611eca40f

HTTP/1.1 200 
Content-Type: application/json;charset=UTF-8
Transfer-Encoding: chunked
Date: Tue, 07 Aug 2018 20:32:59 GMT
{
    "id": "04c7197f-c0fe-4dab-b27c-d69611eca40f",
    "numero": "SOFT 2018/00008",
    "entrada": "07/08/2018",
    "descricao": "Solicitação de licença-prêmio",
    "assunto" : "Licença",
    "interessados": ["Edmilson Cherem"]
}
```


### Diferenciais
- Adaptar a página para dispositivos móveis (torná-la responsiva).
- Liberação da aplicação utilizando Docker.
- Boa documentação.
- Teste do código.


---
Em caso de dúvidas, envie um email para [g_cpa_squad_produto@softplan.com.br](mailto:g_cpa_squad_produto@softplan.com.br).


**Um dos nossos pilares é a valorização das pessoas e temos orgulho de dizer que somos uma empresa que apoia a diversidade e inclusão. Sendo assim, consideramos todos os candidatos para as nossas oportunidades, independente de raça, cor, religião, gênero, identidade de gênero, nacionalidade, deficiência, ascendência ou idade.**


**Até breve**
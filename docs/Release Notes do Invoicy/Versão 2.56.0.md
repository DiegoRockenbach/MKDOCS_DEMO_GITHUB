# Versão 2.56.0
<div class="data_Artigo">
    <b>3 de novembro de 2022</b>
</div>
Olá pessoal!
Confiram as novidades da versão 2.56.0 do Invoicy em detalhes:

## Mensagem Informativa ao habilitar um novo parâmetro no Modelo do DANFE Personalizado `(BETA)`:

No modelo de impressão Personalizado `(BETA)` é possível ativar vários parâmetros para constar no DANFE, porém ao ativar uma certa quantidade de opções, pode desorganizar o layout do DANFE. Com isso, foi adicionada uma mensagem informativa que será exibida quando o usuário ativar a opção `Personalizar tabela de produtos` ou habilitar um novo parâmetro.

A inclusão desta mensagem informativa, sugerindo a pré-visualização da impressão antes de salvar, irá evitar que ocorra algum tipo de problema nos dados dos produtos e serviços na impressão do DANFE. O popup abaixo será aberto quando clicar em *Salvar*.

<img class="img_ReleaseNotes" alt="IMG1"  src="img/2.56.0/IMG1.png">

Caso o usuário deseje realizar a pré-visualização antes de salvar, basta clicar em *Ok*. Se porventura o mesmo queira pular a pré-visualização, poderá clicar em *Salvar*.

## Inclusão do campo DocNumeroPedido no retorno do envio da Prévia de NF-e:

Com a nova versão do InvoiCy foi incluído um novo campo no retorno do envio da Prévia de NF-e, trata-se do campo `<DocNumeroPedido>`, que será alimentado com a informação que será enviada na tag `<NumeroPedido>`.

Lembrando que este campo será devolvido apenas no retorno do envio da prévia de NF-e, e para isso será necessário passar junto aos parâmetros de emissão a tag `<RetornaNumPedido>` como *S*.

[Clique aqui](/Integra%C3%A7%C3%B5es/NFe/){:target="_blank"} para baixar um exemplo de envio com o parâmetro `<RetornaNumPedido>` e também de retorno do envio da Prévia de NF-e, via Web Service através do SOAP UI com o novo campo `<DocNumeroPedido>` incluído.
Observação: Será possível enviar este novo parâmetro somente via API SOAP e e InvoiCy Conector, nas próximas versões estará sendo liberada a possibilidade de informá-lo no envio da prévia via API REST.

## Inclusão do campo DocIeEmitente no retorno do envio da NF-e:

Foi realizada a inclusão do campo `<DocIeEmitente>` no retorno do envio da NF-e via Web Service e também no retorno do envio da prévia de NF-e. Este campo será alimentado com a informação enviada na tag `<IE>`.
Para que seja retornado este campo, será necessário passar junto aos parâmetros de emissão a tag `<RetornaIeEmitente>` como *S*.

[Clique aqui](/Integra%C3%A7%C3%B5es/NFe/){:target="_blank"} para baixar um exemplo de envio com o parâmetro `<RetornaIeEmitente>` e também do retorno de envio da NF-e, via Web Service através do SOAP UI com o novo campo incluído.

!!!abstract "Observação:"

    Será possível enviar este novo parâmetro somente via API SOAP e InvoiCy Conector, nas próximas versões estará sendo liberada a possibilidade de informá-lo no envio da NF-e e também da prévia de NF-e via API REST.

## Novos parâmetros de configuração para impressão da NF-e:

Essa versão do InvoiCy conta com novos parâmetros nas configurações de impressão da NF-e! Logo abaixo do parâmetro já existente *Imprimir valor total da AFRMM*, foi criado o novo parâmetro *Somar os valores AFRMM dos itens*.

<img class="img_ReleaseNotes" alt="IMG2"  src="img/2.56.0/IMG2.png">

Configurando este parâmetro como *Sim*, será somado o valor AFRMM de cada item da NF-e, e impresso no DANFE quando o parâmetro *Imprimir valor total da AFRMM* também estiver configurado como *Sim*. Veja na imagem abaixo um DANFE apresentando a soma dos valores AFRMM de uma NF-e.

<img class="img_ReleaseNotes" alt="IMG3"  src="img/2.56.0/IMG3.png">

**Mas atenção!** Este parâmetro está disponível apenas para o DANFE no modelo Personalizado.

Para atender o ajuste Sinief 17/22, onde fica a critério de cada UF desobrigar o contribuinte em informar o valor total da NF-e no DANFE Simplificado Etiqueta, foi criado o novo parâmetro *Imprimir valor total NF-e*, que permite definir se o valor total da NF-e será impresso ou não no DANFE Etiqueta.

<img class="img_ReleaseNotes" alt="IMG4"  src="img/2.56.0/IMG4.png">

**Mas atenção!** Este parâmetro está disponível apenas para o DANFE Etiqueta, conforme demonstra a imagem a seguir.

<img class="img_ReleaseNotes" alt="IMG5"  src="img/2.56.0/IMG5.png">

## Agendamento de Exportação Recorrente via API:

Nesta versão do InvoiCy, estamos liberando a integração de mais um padrão de NFS-e, trata-se do padrão Tributos Municipais WS, que atende o município de Escada do estado de Pernambuco. Com isso, permitimos aos prestadores de serviço que utilizam esse padrão emitir e gerenciar suas NFS-e em nossa plataforma.

Para mais informações acesse o artigo do padrão [clicando aqui](https://desenvolvedores.migrate.info/2022/10/particularidades-padrao-tributos-municipais-ws/){:target="_blank"}.

Faça as alterações necessárias e desfrute de todo o potencial da Plataforma InvoiCy!
Ficou com alguma dúvida? Encaminhe para `atendimento@migrate.info` que nossa equipe de atendimento te ajuda!

Aqui o movimento não para!

<div class="autor">
    <img alt="Avatar do autor" src="/img/img_autor.png">
    <div class="publi_Por">
        <h2>Publicado por: <a href="https://desenvolvedores.migrate.info/author/brunakalschne/" target="_blank"  title="Posts de brunakalschne">brunakalschne</a></h2>
    </div>
<span>Postado em <a>Invoicy </a>com as tags <a>Release Notes</a>, <a>Versão 2.56.0</a></span>
</div>
<div class="comentarios">
    <form class="form_comentarios">
        <span class="form_comentarios_comment">
            <label for="comment">Comentário </label>
            <textarea id="comment" name="comment" cols="45" rows="8" maxlength="65525" required="required"></textarea>
        </span>
        <p class="form_comentarios_nome">
            <label for="name">Nome <span class="required">*</span></label>
            <input id="name" name="name" type="text" value="" maxlength="245" required="required">
        </p>
        <p class="form_comentarios_email">
            <label for="email">E-mail <span class="required">*</span></label>
            <input id="email" name="email" type="email" value="" maxlength="100" aria-describedby="email-notes" required="required">
        </p>
        <div class="form_comentarios_cookie_checkbox">
            <input id="wp-comment-cookies-consent" name="wp-comment-cookies-consent" type="checkbox" value="yes">
            <label for="wp-comment-cookies-consent">Salvar meus dados neste navegador para a próxima vez que eu comentar.</label>
        </div>
        <div class="form_comentarios_submit">
            <input name="submit" type="submit" id="submit" class="submit btn btn-primary btn-sm btn-invoicy rounded-pill" value="Publicar comentário">
        </div>
    </form>
</div>
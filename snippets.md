# Snippets para ajudar responder perguntas e violações de regras

## Perguntas comuns
* [Não é possível acessar o painel](#não-é-possível-acessar-o-painel)
* [Erro relacionado a plugin ou conflito de tema](#erro-relacionado-a-plugin-ou-conflito-de-tema)
* [Erro relacionado a arquivos do próprio WordPress que estão faltando ou corrompidos](#erro-relacionado-a-arquivos-do-próprio-wordpress-que-estão-faltando-ou-corrompidos)
* [Erros de falta de memória](#erros-de-falta-de-memória)
* [Erro 500: Erro interno do servidor (Internal Server Error)](#erro-500-erro-interno-do-servidor-internal-server-error)
* [Hackeado/Invadido?](#hackeadoinvadido)
* [Limite de Upload de Arquivo](#limite-de-upload-de-arquivo)
* [Downgrading/Reversão de atualização de versão](#downgradingreversão-de-atualização-de-versão)
* [Blog do WordPress.com](#blog-do-wordpresscom)
* [Alterar o número de posts por página](#alterar-o-número-de-posts-por-página)
* [Suporte de Plugin/Tema em um fórum não específico do Plugin/Tema](#suporte-de-plugintema-em-um-fórum-não-específico-do-plugintema)
* [Pedindo Suporte para um Produto Comercial](#pedindo-suporte-para-um-produto-comercial)
* [Serviço de Hospedagem Grátis](#serviço-de-hospedagem-grátis)
* [Recomendações de Hospedagem](#recomendações-de-hospedagem)
* [Oferecendo Pagamento/Contratação](#oferecendo-pagamentocontratação)
* [Chegando aos Limites do Suporte Grátis](#chegando-aos-limites-do-suporte-grátis)
* [Pedindo Acesso Administrativo](#pedindo-acesso-administrativo)
* [Pedido de Feedback para Site](#pedido-de-feedback-para-site)
* [Discussão sobre GPL](#discussão-sobre-gpl)
* [Pedido de Suporte Não-GPL](#pedido-de-suporte-não-gpl)
* [Quando pessoas reclamam que ‘WordPress está hospedando um site’](#quando-pessoas-reclamam-que-wordpress-está-hospedando-um-site)
* [Quando pessoas querem que suas contas no WordPress.org sejam excluídas](#quando-pessoas-querem-que-suas-contas-no-wordpressorg-sejam-excluídas)
* [Quando você quer avisar o usuário para não editar a folha de estilo do seu tema diretamente](#quando-você-quer-avisar-o-usuário-para-não-editar-a-folha-de-estilo-do-seu-tema-diretamente)
* [Quando um usuário precisa fazer mudanças mais significativas e um plugin de CSS personalizado não vai adiantar - é hora de usar um tema filho.](#quando-um-usuário-precisa-fazer-mudanças-mais-significativas-e-um-plugin-de-css-personalizado-não-vai-adiantar---é-hora-de-usar-um-tema-filho)
* [Quando você quer que um usuário marque seu próprio tópico como resolvido](#quando-você-quer-que-um-usuário-marque-seu-próprio-tópico-como-resolvido)
* [Quando você quer que um usuário compartilhe a solução que ele mesmo encontrou para o seu problema](#quando-você-quer-que-um-usuário-compartilhe-a-solução-que-ele-mesmo-encontrou-para-o-seu-problema)

## Respostas predefinidas para Multisite
* [Problemas criando subsites](#problemas-criando-subsites)
* [Eu quero que todos os meus subsites sejam idênticos em conteúdo exceto por [uma coisa qualquer]](#eu-quero-que-todos-os-meus-subsites-sejam-idênticos-em-conteúdo-exceto-por-uma-coisa-qualquer)
* [Como usar multisite para uma rede multi-idioma](#como-usar-multisite-para-uma-rede-multi-idioma)

## Violações de regras
* [Não tente furar a fila](#não-tente-furar-a-fila)

## Perguntas Comuns

### Não é possível acessar o painel
Tente [desabilitar manualmente todos os seus plugins](https://codex.wordpress.org/pt-br:FAQ_Resolvendo_Problemas#Como_desativar_todos_os_plugins_quando_n.C3.A3o_poder_acessar_os_menus_administrativos.3F) (não é preciso acesso ao painel). Se isso resolver, reative-os um a um até saber qual deles está causando o problema.

Se isso não resolver, acesse seu servidor via [SFTP ou FTP](https://codex.wordpress.org/pt-br:Clientes_FTP), ou por algum gerenciador de arquivos que a sua empresa de hospedagem forneça, navegue até ‘wp-content/themes/’ e renomeie o diretório do tema atualmente ativo. Isso forçará a ativação do tema padrão e, com alguma sorte, verificar um problema específico do tema (funções do tema também podem interferir, assim como os plugins).

### Erro relacionado a plugin ou conflito de tema
Tente desativar todos os plugins. Se isso resolver, reative-os um a um até saber qual deles está causando o problema.

Se isso não resolver, tente ativar um tema padrão da sua versão do WordPress para verificar se é um erro específico do tema (funções do tema também podem interferir, assim como os plugins).

### Erro relacionado a arquivos do próprio WordPress que estão faltando ou corrompidos
Tente fazer o [download do WordPress](https://br.wordpress.org/) novamente, acesse seu servidor via [SFTP ou FTP](https://codex.wordpress.org/pt-br:Clientes_FTP), ou por algum gerenciador de arquivos que a sua empresa de hospedagem forneça, exclua e então substitua sua cópia de tudo com os arquivos que você baixou, exceto o arquivo ‘wp-config.php’ e o diretório ‘/wp-content/’. Isso irá substituir todos os seus arquivos do Wordpress sem nenhum prejuízo ao seu conteúdo ou configurações.

Em alguns programas não são confiáveis quando se tenta sobrescrever arquivos, então não esqueça de excluir os arquivos originais antes de fazer o upload.

### Erros de falta de memória
Mesmo que você esteja vendo esse erro de repente (nenhuma tarefa específica foi executada para causar o erro) ou frequentemente, tente desativar todos os plugins para verificar se o erro é de algum plugin específico e trocar de tema pelo mesmo motivo.

Caso contrário, aqui estão três formas de aumentar a alocação de memória para o PHP:

1. Se você pode editar ou sobrescrever o arquivo `php.ini` do sistema, aumente o limite de memória. Por exemplo `memory_limit = 128M`

2. Se você não pode editar ou sobrescrever o arquivo `php.ini` do sistema, adicione `php_value memory_limit 128M` no seu arquivo `.htaccess`.

3. Se nada disso funcionar, você precisará pedir para a sua empresa de hospedagem que aumente temporariamente a alocação de memória da sua conta.

(nos exemplos acima o limite está configurado para 128MB).


### Erro 500: Erro interno do servidor (Internal Server Error)
Erros internos do servidor (erro 500) são frequentemente causados por conflitos de plugin ou funções do tema, então se você consegue acessar o painel do WordPress e tente desativar todos os plugins. Se você não tem acesso ao painel, tente [desabilitar manualmente todos os seus plugins](https://codex.wordpress.org/pt-br:FAQ_Resolvendo_Problemas#Como_desativar_todos_os_plugins_quando_n.C3.A3o_poder_acessar_os_menus_administrativos.3F) (não é preciso acesso ao painel). Se isso resolver, reative-os um a um até saber qual deles está causando o problema.

Se isso não resolver, acesse seu servidor via SFTP ou FTP, ou por algum gerenciador de arquivos que a sua empresa de hospedagem forneça, navegue até ‘wp-content/themes/’ e renomeie o diretório do tema atualmente ativo. Isso forçará a ativação do tema padrão e, com alguma sorte, verificar um problema específico do tema (funções do tema também podem interferir, assim como os plugins).


Se isso não resolver, é possível que uma regra no `.htaccess` possa ser a origem do problema. Para verificar, acesse seu servidor via SFTP ou FTP, ou por algum gerenciador de arquivos que a sua empresa de hospedagem forneça, e renomeie o arquivo `.htaccess`. Se você não pude encontrar o arquivo `.htaccess` tenha certeza de que configuou seu cliente de SFTP ou FTP para visualizar arquivos ocultos.


Se você não conseguiu resolver o problema nem desabilitando seus plugins e tema, ou renomeando seu arquivo .htaccess, nós ainda podemos ajudar, mas serão necessárias mensagens de erro mais detalhadas. Erros internos do servidor são frequentemente mais detalhados nos logs de erro do servidor. Se você tem acesso aos logs de erro do servidor, gere o erro novamente, anote o dia e a hora e então imediatamente verifique o arquivo de log por qualquer erro ocorrido naquele período. Se você não tem acesso aos logs, peça ao seu serviço de hospedagem que procure-os por você.


### Hackeado/Invadido?
Mantenha-se calmo e siga cuidadosamente [esse guia](https://codex.wordpress.org/pt-br:Site_Invadido). Quando você tiver terminado talvez você queira implementar algumas (se não todas) as [medidas de segurança recomendadas](https://codex.wordpress.org/pt-br:Blindando_o_WordPress).

### Limite de Upload de Arquivo
O tamanho máximo de upload é controlado pelo servidor, não pelo WordPress. Aqui estão três formas de aumentar o limite de upload:
1. Se você pode editar ou sobrescrever o arquivo `php.ini`, aumente o tamanho máximo de post e de upload de arquivo. Por exemplo: `upload_max_filesize = 100M ;` and `post_max_size = 100M ;`
2. Se você não pode editar ou sobrescrever o arquivo `php.ini`, adicione `php_value upload_max_filesize 100M` e `php_value post_max_size = 100M` ao seu arquivo `.htaccess`
3. Se não funcionar de nenhuma forma, é hora de pedir que seu serviço de hospedagem aumente o limite de upload da sua conta. Tenha em mente que a maioria dos prestadores deste serviço permitem esse aumento, e se seu serviço de hospedagem já não atende mais as suas necessidades, talvez seja a hora de achar outro.
(nos exemplos acima, o limite está configurado para 100MB)


### Downgrading/Reversão de atualização de versão
A não ser que você tenha um backup que possa restaurar, voltar para uma versão anterior é um processo perigoso, motivo pelo qual é recomendada a realização do backup tanto nas instrução de upgrade quanto na tela de atualização automática.

Seria melhor resolver o seu problema atual. Você poderia descrever o que está dando errado?


### Blog do WordPress.com
O WordPress.ORG não fornece hospedagem para sites, ele fornece o software para que outras pessoas o usem em seus próprios sites e em suas próprias hospedagens. Nesse fórum é prestado suporte ao software WordPress.

Pelo o que você descreveu, o seu problema deve ser com o WordPress.COM. Assim, você provavelmente deveria perguntar no [Suporte do WordPress.com](https://br.support.wordpress.com/).

### Alterar o número de posts por página
Você pode alterar o número máximo de posts por página por meio do menu “Configurações >> Leitura” no campo “As páginas do blog mostram no máximo”.

### Suporte de Plugin/Tema em um fórum não específico do Plugin/Tema
Recomendo que você pergunte no [URL do fórum do plugin/tema] para que os desenvolvedores do plugin/tema e a comunidade de suporte possam lhe ajudar com isso.


### Pedindo Suporte para um Produto Comercial
Se você está usando um tema ou plugin comercializados e precisa de suporte, por favor vá até o fórum oficial do produto. Para ajudarmos a comunidade WordPress, e encorajarmos a inovação e o progresso, achamos importante direcionar as pessoas para estes locais.

[URL do suporte do produto, se for fácil de encontrar]


Voluntários do fórum não recebem acesso a produtos comercializados, então eles não saberiam o porquê do seu plugin ou tema não funcionar corretamente. Existe outra razão pela qual os voluntários lhe encaminham para os canais de atendimento dos produtos comercializados: os vendedores são responsáveis por prestar suporte de seus produtos.

### Serviço de Hospedagem Grátis
(para recomendações de serviços de hospedagem grátis e/ou problemas encontrados em hospedagens grátis)

Nós normalmente não recomendamos serviços de hospedagem grátis por aqui, por eles frequentemente oferecerem servidores com poucos recursos, que impedem que o WordPress funcione corretamente.

Se você quer um blog grátis, tente o WordPress.com como alternativa. Se você não se importa em pagar, a equipe do WordPress fornece [uma lista de recomendações de serviços de hospedagem](https://wordpress.org/hosting/) [em inglês].


### Recomendações de Hospedagem
Por favor coloque a tag “modlook” no tópico para que um moderador possa fechá-lo.


Como dito no [artigo de Boas Vindas do Fórum](https://codex.wordpress.org/pt-br:Bem-vindos_ao_F%C3%B3rum_de_Suporte#Fechando_t.C3.B3picos), tópicos como este são fechados devido a quantidade de spam que eles atraem.

A equipe do WordPress fornece [uma lista de recomendações de serviços de hospedagem](https://wordpress.org/hosting/). Para mais detalhes ou outras recomendações, por favor pesquise nos fóruns ou via Google (ou por seu buscador favorito).


### Oferecendo Pagamento/Contratação
O WordPress é um software gratuito e este fórum é gratuito também, então não encorajamos a utilização dos fóruns para oferecer pagamentos.

Por favor tente sites especializados como o http://jobs.wordpress.net/ e o https://hangarwp.com/. Você também podem procurar um desenvolvedor em um [meetup](https://br.wordpress.org/2017/05/01/wordpress-meetups-o-que-sao-estes-encontros-da-comunidade-wordpress/).

Este tópico será fechado seguindo as Regras do Fórum.


### Chegando aos Limites do Suporte Grátis
Neste ponto chegamos aos limites do que a maioria da comunidade aqui tem a intenção de oferecer em seu tempo livre (todos aqui são voluntários). Considere contratar alguém para quem você possa dar acesso direto ao seu site a fim de um conserto mais eficiente do que podemos oferecer aqui.

Por favor tente http://jobs.wordpress.net/ ou https://hangarwp.com/ e não aceite qualquer oferta de contratação publicada neste fórum. Você também podem procurar um desenvolvedor em um [meetup](https://br.wordpress.org/2017/05/01/wordpress-meetups-o-que-sao-estes-encontros-da-comunidade-wordpress/).

Nós manteremos este tópico aberto, a não ser que ele se distancie muito do assunto, para o caso de alguém da comunidade querer oferecer maior ajuda de graça.


### Pedindo Acesso Administrativo
Por favor não faça isso: quando você pedir acesso ao painel e/ou FTP você estará indo longe demais e isso não é legal.

https://codex.wordpress.org/pt-br:Bem-vindos_ao_F%C3%B3rum_de_Suporte#Coisas_para_evitar_e_mau_comportamento

Se você recebeu credenciais administrativas, você estará potencialmente sujeito a qualquer dano possível que possa ser causado, não só por você mesmo mas por qualquer um que acesse o sistema. Mesmo que você não forneça garantias.

A menos que você deseje se responsabilizar por aquela instalação do usuário a partir de agora (e eles NÃO deveriam deixar você fazer isso) então por favor não peça ou sugira que alguém forneça os dados de acesso ao painel ou FTP.

Você pode fornecer assistência aqui, pedir dados de log, fazer recomendações ou mesmo sugerir mudanças. Mas não peça acesso à administração ou FTP. Isso é ir longe demais.


### Pedido de Feedback para Site
Por favor coloque a tag “modlook” no tópico para que um moderador possa fechá-lo.


Este fórum existe para ajudar aqueles com problemas em seus sites WordPress. Por favor peça opiniões para amigos ou família de modo que os voluntários aqui possam investir seu tempo ajudando aqueles que estão com dificuldades.

Este tópico será fechado segundo as [regras do fórum](https://codex.wordpress.org/pt-br:Bem-vindos_ao_F%C3%B3rum_de_Suporte#Coisas_para_evitar_e_mau_comportamento), e se você precisar de ajuda com qualquer coisa específica, nós o encorajamos a abrir um novo tópico.

### Discussão sobre GPL
Por favor coloque a tag “modlook” no tópico para que um moderador possa fechá-lo.

A discussão se o WordPress e seus temas e plugins são GPL não é algo que consideremos adequado para debater aqui. Com certeza o WordPress é licenciado sob GPLv2 [em inglês], e todos os temas e plugins hospedados no WordPress.org são obrigados a ser compatíveis integralmente com a GPLv2, de modo que você é livre para editar e redistribuir como quiser. Se o código não é licenciado como compatível com GPLv2 (ou posterior), nós pedimos que você não traga essa discussão para cá.


### Pedido de Suporte Não-GPL
Por favor coloque a tag “modlook” no tópico para que um moderador possa fechá-lo.

Desculpe, mas o tema que você escolheu não foi liberado sob a GPL. Produtos assim não são bem-vindos na comunidade WordPress. A Política Oficial do WordPress afirma que todos os plugins e temas que são liberados publicamente são obrigados a aderir a https://wordpress.org/about/gpl/ . Qualquer pedido de suporte para produtos não-GPL são normalmente ignorados, pelo bem da comunidade e de sua liberdade.


### Quando pessoas reclamam que ‘WordPress está hospedando um site’
Por favor coloque a tag “modlook” no tópico para que um moderador possa fechá-lo.

WordPress.org não fornece hospedagem para sites, ele fornece o software para que outras pessoas o usem em seus próprios sites e em suas próprias hospedagens. A [Filosofia do WordPress](https://wordpress.org/about/philosophy/) [em inglês] e declaração de direitos permite que as pessoas usem o programa WordPress para qualquer razão que elas queiram, sem analisar nenhuma aplicação sobre legalidade ou ilegalidade. Nós deixamos isso para os serviços de hospedagem. Em casos de roubo, abuso, assédio ou qualquer outro comportamento deste tipo, o melhor é entrar em contato diretamente com o serviço de hospedagem. Você pode usar o WHOIS para determinar onde um site está hospedado, ou recursos como o http://www.whoishostingthis.com para encontrar informações relevantes.

### Quando pessoas querem que suas contas no WordPress.org sejam excluídas
Por favor coloque a tag “modlook” no tópico para que um moderador possa fechá-lo.


Nesse momento, contas não podem ser excluídas no WordPress.org, atualmente é uma impossibilidade técnica. Você pode editar seu perfil para remover todas as informações, e nós podemos até bloquear sua conta se você quiser, mas não podemos excluí-la.

(Por favor não mencione qualquer lei ou aspectos legais, independente do país, deixe isso para os profissionais)


### Quando você quer avisar o usuário para não editar a folha de estilo do seu tema diretamente
Não edite arquivos do tema diretamente, caso contrário suas mudanças serão sobrescritas quando o tema for atualizado.

Se você estiver utilizando o WordPress 4.7+, no menu Aparência > Personalizar > “CSS adicional”, você pode adicionar CSS no seu tema de forma mais fácil.

Como alternativas você pode tanto instalar um plugin de CSS personalizado quanto criar um tema filho.

### Quando um usuário precisa fazer mudanças mais significativas e um plugin de CSS personalizado não vai adiantar - é hora de usar um tema filho.

O melhor modo de realizar mudanças como esta em um tema é usar um [tema filho](https://codex.wordpress.org/pt-br:Temas_Filhos), de modo que seus ajustes não sejam sobrescritos quando o tema for atualizado.

### Quando você quer que um usuário marque seu próprio tópico como resolvido
Se sua questão foi resolvida, nós adoraríamos que você marcasse este tópico como resolvido na barra lateral direita. Isso ajuda os voluntários a encontrar tópicos que ainda precisam de atenção e mais pessoas receberão ajuda, assim como você possivelmente recebeu.

### Quando você quer que um usuário compartilhe a solução que ele mesmo encontrou para o seu problema
Você marcou o tópico como resolvido antes de alguém responder. Acredito que você achou a solução para o problema que estava enfrentando. Por isso, seria interessante seria você compartilhar o que fez. Dessa forma, outras pessoas com o mesmo problema podem encontrar ajuda no seu tópico.

## Respostas predefinidas para Multisite
### Problemas criando subsites
Para criar um subsite no WP Multisite, simplesmente vá até Sites -> Adicionar novo no painel administrativo da Rede. Se você está usando multisite do tipo subdomínio, você NÃO precisa criar o subdominio na sua hospedagem. O multisite fará isso por você usando o curinga de domínio que você configurou na sua conta de hospedagem.

### Eu quero que todos os meus subsites sejam idênticos em conteúdo exceto por [uma coisa qualquer]
Uma coisa a ser entendida sobre multisites é que por padrão cada subsite funciona como um site completamente separado inclusive em seus conteúdos. Dito isso, existem alguns plugins com o quais você pode duplicar o conteúdo entre os sites. Procure no repositório por “multiste duplicar conteúdo”. PORÉM, você deverá atentar-se que o Google o penalizará por duplicar conteúdos desta forma.

### Como usar multisite para uma rede multi-idioma
Multisite pode ser um modo útil para configurar sites multi-idioma. No entanto, multisite é mais complicado que um site WP simples, então você terá que verificar as habilidades necessárias para criar e gerenciar uma rede multisite antes de mergulhar nisso. Existem [instruções passo-a-passo](https://codex.wordpress.org/pt-br:Crie_uma_Rede) para configurar um multisite no codex do WP, mas você pode achar útil este artigo sobre [como configurar uma rede multi-idioma](http://wplang.org/wordpress-multisite-multilingual/) [em inglês].



## Violações de regras
### Não tente furar a fila
Não tente trazer seu tópico de volta para o topo da lista, isto não ajuda seu tópico a ser notado. Os voluntários que tentam responder as perguntas olham primeiro aquelas que não tem nenhuma resposta. Se você cria uma resposta tentando trazê-lo de volta, isso faz com que ele desapareça da lista de “Tópicos sem resposta”.

Em algumas horas vou excluir sua resposta e a minha para que seu tópico volte para a lista de Sem Resposta, onde há uma chance maior de você receber ajuda.

Tenha em mente que esse fórum é mantido por voluntários e que estes vão te ajudar assim que puder.


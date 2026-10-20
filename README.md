Quintal das Descobertas
Uma aventura educativa para aprender, brincar e explorar.

Quintal das Descobertas é um jogo educacional para crianças de 5 a 6 anos, da Educação Infantil — Pré-escola II. A aplicação reúne 24 atividades em seis trilhas temáticas, com ilustrações, leitura dos enunciados, dicas e acompanhamento para educadores.

O projeto foi desenvolvido a partir do escopo do Projeto de Curricularização da Extensão do curso de Sistemas de Informação da UNIFEBE, realizado em parceria com a Secretaria Municipal de Educação de Brusque.
Estágio atual: versão funcional inicial, com fluxo completo de jogo e testes automatizados registrados. A publicação no GitHub Pages, os testes nos navegadores e equipamentos das escolas e a validação com educadores e crianças ainda precisam ser concluídos.

Objetivo
Oferecer uma experiência lúdica e acolhedora que estimule a exploração de cores, formas, quantidades, relações espaciais, animais, sons e letras. O acompanhamento das atividades serve como apoio à observação do educador durante a brincadeira.

No contexto acadêmico, a proposta aproxima os estudantes de requisitos reais de um cliente institucional e das etapas de pesquisa, design, desenvolvimento, testes e validação de uma solução com finalidade social e educacional.
Trilhas de aprendizagem
Cada trilha possui quatro desafios, com três alternativas por questão, dica e retorno após a resposta.
Trilha	Conteúdos abordados
Cores e formas	Identificação de cores, correspondência de formas e sequência visual
Vamos contar	Contagem de elementos e associação entre quantidade e numeral
Aqui e ali	Comparação de alturas e relações espaciais: dentro, embaixo e acima
Bichos e lugares	Animais, características, ambientes e ninhos
Sons e palminhas	Rimas, percepção de sílabas e compreensão de uma narrativa breve
Letras curiosas	Letras iniciais e comparação dos sons no início de palavras


As atividades de oralidade podem ser mediadas pelo educador. As respostas são selecionadas na tela; o jogo não grava a voz nem reconhece palmas.
Funcionalidades
- Escolha de companheiro: Lupi, o coelho; Mimi, a gata; ou Pipo, o passarinho.
- Mapa com livre escolha: as seis trilhas ficam disponíveis para exploração.
- Instruções em voz alta: leitura das perguntas e controle da narração automática.
- Dicas e novas tentativas: retorno acolhedor, sem cronômetro, vidas ou ranking.
- Progresso local: retomada da aventura no mesmo navegador quando o armazenamento está disponível.
- Repetição das trilhas: possibilidade de brincar novamente após concluir uma trilha.
- Área para educadores: consulta de atividades concluídas, respostas selecionadas e dicas solicitadas.
- Exportação em CSV: download das observações da primeira exploração.
- Conclusão da aventura: celebração de cada trilha e conquista final após as seis trilhas.
- Interface responsiva: adaptação a diferentes tamanhos de tela, com indicadores de foco e respeito à preferência de movimento reduzido.
Como jogar
1. Na tela inicial, selecione Vamos brincar!.
2. Escolha um companheiro e clique em Vamos explorar!.
3. Em Meu quintal, selecione uma das seis trilhas.
4. Escute ou leia a pergunta e escolha uma resposta. Use a dica quando precisar.
5. Conclua os quatro desafios para chegar à celebração da trilha.
6. Explore as demais trilhas até alcançar a conquista final.
A criança pode voltar ao mapa e fazer pausas. Quando houver uma aventura salva, o botão Continuar aventura permite retomá-la.
Tecnologias
Tecnologia	Uso no projeto
HTML5	Estrutura da aplicação
CSS3	Estilos, estados visuais e adaptação às telas
JavaScript	Navegação, regras do jogo, respostas e acompanhamento
SVG	Ilustrações e ícones vetoriais
Web Speech API — SpeechSynthesis	Leitura dos enunciados e retornos
localStorage	Salvamento do progresso no navegador
GitHub Pages	Destino previsto para a publicação estática


A aplicação utiliza arquivos estáticos. Para jogar ou publicar, não é necessário instalar pacotes, executar uma compilação ou configurar um backend. O jsdom é uma dependência opcional utilizada somente nos testes de desenvolvimento.
Executar localmente
Abertura direta
1. Baixe ou clone o repositório.
2. Caso utilize um arquivo ZIP, extraia seu conteúdo.
3. Mantenha a estrutura de arquivos e abra index.html no navegador, com JavaScript habilitado.
Servidor local
Para desenvolver e verificar a retomada por um endereço HTTP, execute este comando na pasta do projeto, se o Python 3 estiver instalado:
python3 -m http.server 8000
Em seguida, abra http://localhost:8000.

O salvamento depende do navegador, do perfil utilizado e da permissão para armazenar dados. A abertura direta por file: pode apresentar diferenças de persistência; para validar esse comportamento, use sempre o mesmo endereço HTTP/HTTPS. Consulte a documentação de localStorage.
Publicar no GitHub Pages
1. Envie os arquivos do projeto para a raiz de um repositório no GitHub, incluindo index.html e .nojekyll.
2. Acesse Settings → Pages.
3. Em Build and deployment, escolha Deploy from a branch.
4. Selecione a branch que contém os arquivos, por exemplo, main, e a pasta /(root). Salve a configuração.
5. Aguarde a implantação e abra o endereço exibido pelo GitHub.
6. Verifique o percurso completo do jogo pelo endereço publicado antes de entregar o link.
Os caminhos relativos dos arquivos permitem a publicação em uma página de projeto. O procedimento detalhado está no [guia de publicação](./docs/PUBLICACAO_GITHUB_PAGES.md) e na documentação oficial do GitHub Pages.
Acompanhamento para educadores
O botão Para educadores abre um resumo das atividades e a opção Exportar observações (CSV).
Registro	Significado
Atividade concluída	A alternativa esperada foi selecionada, possivelmente com ajuda ou após novas tentativas
Respostas selecionadas	Quantidade de escolhas aceitas na primeira exploração; um erro seguido de acerto conta como duas respostas
Dica solicitada	Indica se o botão de dica foi utilizado ao menos uma vez naquela atividade
Repetição de trilha	Permite brincar novamente sem aumentar os registros da primeira exploração


Esses registros apoiam a observação e a mediação pedagógica. Sua interpretação deve considerar as condições da atividade e a ajuda recebida pela criança; eles não constituem uma nota ou um diagnóstico de aprendizagem.
Progresso e uso compartilhado
A aplicação mantém uma aventura por navegador e perfil. Progresso, companheiro escolhido, preferência de narração e datas da aventura ficam no armazenamento local. O jogo não solicita nome, e-mail, matrícula ou login, e o CSV é gerado no próprio dispositivo quando o educador solicita a exportação.

As informações não são sincronizadas entre computadores ou navegadores. A remoção dos dados do site pode apagar o progresso. Se o armazenamento falhar, o jogo apresenta um aviso e permite continuar durante a sessão.

Antes de outra criança utilizar a mesma aventura em um equipamento compartilhado:
1. Consulte ou exporte as observações que deseja guardar.
2. Em Para educadores, selecione Iniciar uma nova aventura.
3. Confirme em Apagar e recomeçar.
O reinício limpa os registros desta aventura e preserva a escolha do companheiro e a preferência de narração. Como não há identificação individual, compartilhar uma aventura sem reiniciá-la mistura as observações de seus participantes.
Narração e mediação
O botão Ouvir a pergunta solicita a leitura do enunciado completo. O controle no cabeçalho liga ou desliga a narração automática; a leitura solicitada explicitamente continua disponível quando a narração automática está desligada.

A aplicação procura uma voz em português do Brasil (pt-BR) e, quando necessário, outra voz em português. As vozes disponíveis, a pronúncia e a necessidade de conexão dependem do navegador e do dispositivo. Quando a leitura não está disponível ou falha, a interface apresenta o enunciado completo para apoio do educador. Consulte a documentação de vozes da Web Speech API.

A conferência do áudio no equipamento da escola é especialmente relevante nas atividades de rimas, sílabas e sons iniciais.
Testes e validação
Na preparação da versão inicial, foram registrados 15 testes automatizados aprovados:
Suíte	Quantidade	Cobertura principal
Núcleo do jogo	8	Estado da aventura, respostas, dicas, repetição, restauração e resumo
Integração do DOM	7	Percurso das 24 atividades, conclusões, retomada, CSV, reinício e alternativas à narração


O ambiente registrado utilizou Node.js 24.19.0 e jsdom 30.1.3. Também foi realizada a conferência dos arquivos estáticos, dos caminhos relativos e das 24 questões.
Executar as verificações
Na pasta do projeto, com Node.js instalado:
node tests/core.test.cjs
node tests/check_assets.cjs
Para executar a suíte de integração, instale a dependência de teste:
npm install --no-save jsdom@30.1.3
node tests/ui.test.cjs
Os testes com DOM simulado verificam comportamento e conteúdo. A renderização visual, a saída de áudio e a interação em dispositivos físicos precisam ser conferidas nos navegadores reais.
Próximas etapas de validação
- Testar o fluxo completo em Chrome, Firefox e Edge, conforme os requisitos da entrega.
- Conferir layout, teclado, toque, áudio e retomada nos equipamentos das escolas.
- Revisar os conteúdos com os educadores responsáveis.
- Observar a compreensão das instruções e a navegação das crianças durante o uso acompanhado.
- Publicar no GitHub Pages e confirmar o funcionamento pelo endereço público.
O [roteiro de validação](./docs/ROTEIRO_VALIDACAO.md) detalha os cenários de verificação.
Estrutura do projeto
Arquivo ou pasta	Responsabilidade
index.html	Entrada da aplicação e carregamento dos arquivos
styles.css	Aparência, estados visuais e responsividade
art.js	Ilustrações e ícones vetoriais
content.js	Conteúdo das seis trilhas e das 24 atividades
core.js	Regras e estado da aventura
app.js	Telas, interações, narração, persistência e exportação CSV
favicon.svg	Ícone da aba do navegador
.nojekyll	Configuração para servir os arquivos estáticos sem processamento Jekyll
docs/	Guias de uso pedagógico, publicação e validação
tests/	Testes do núcleo, integração e conferência de arquivos
tools/criar_html_unico.py	Utilitário para gerar uma versão em um único arquivo HTML


Gerar a versão em HTML único
Com Python 3, execute na pasta do projeto:
python3 tools/criar_html_unico.py ../Quintal_das_Descobertas.html
O utilitário incorpora os estilos, scripts, ilustrações e os dois guias acessíveis dentro do jogo. A versão com arquivos separados pode ser publicada diretamente, sem executar essa etapa.
Documentação complementar
- [Guia pedagógico](./docs/GUIA_PEDAGOGICO.md): conteúdos, objetivos e sugestões de mediação para revisão com os educadores.
- [Guia de publicação no GitHub Pages](./docs/PUBLICACAO_GITHUB_PAGES.md): configuração e conferência do endereço público.
- [Roteiro de validação](./docs/ROTEIRO_VALIDACAO.md): cenários para avaliar navegação, acessibilidade, áudio e progresso.
- [Entrega e validação](./docs/ENTREGA_E_VALIDACAO.md): relação entre funcionalidades implementadas e verificações necessárias.
Referência de design
O protótipo Curricularização 2, no Figma foi fornecido como referência do projeto.

A versão atual utiliza uma proposta visual original, com ilustrações vetoriais próprias. A correspondência com o protótipo ainda precisa ser conferida.

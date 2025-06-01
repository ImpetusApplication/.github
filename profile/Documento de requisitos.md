# Documento de Requisitos de Software (DRS)

## 1. Introdução

### 1.1 Objetivo  
Este documento tem como objetivo definir os requisitos funcionais e não funcionais para o desenvolvimento do Aplicativo de Apoio a Atividades Físicas e Saúde Mental, uma rede social privada para grupos focados em vida fitness, saúde e bem-estar, promovendo apoio mútuo, compartilhamento e motivação. Também é focado em facilitar o dia-a-dia do usuário idealizando hábitos saudáveis para promover uma vida mais confortável e saudável.  

### 1.2 Escopo  
O aplicativo permitirá a criação e gestão de grupos privados (competições), compartilhamento de treinos e refeições no feed do grupo, acompanhamento pessoal com planejador de refeições e treinos, organizador de leituras, além de lembretes de hidratação e alimentação. Será uma ferramenta para usuários iniciantes e experientes, incluindo profissionais da saúde.

Fora do escopo neste momento: funcionalidades relacionadas a gestão financeira e leitura, que podem ser implementadas em versões futuras.

### 1.3 Definições, Acrônimos e Abreviações  
- **Grupo / Competição**: Espaço privado criado por usuário para interação entre membros.  
- **Feed do Grupo**: Área para compartilhar posts de treino e alimentação.  
- **Planejador de Refeições**: Ferramenta para organização individual de refeições diárias.  
- **Organizador de Treinos**: Ferramenta privada para criação e gerenciamento de treinos pessoais.
- **Organizador de Leitura**: Ferramenta privada para gerenciamento de leituras pessoais. 

### 1.4 Referências  
- Diretrizes de acessibilidade móvel  
- Padrões de notificações push em sistemas móveis  

### 1.5 Visão Geral do Documento  
O documento está organizado em seções que abordam a descrição geral do sistema, requisitos funcionais e não funcionais, modelo de dados, critérios de aceitação e considerações adicionais.

---

## 2. Descrição Geral

### 2.1 Perspectiva do Produto  
O aplicativo será uma plataforma móvel, com back-end e front-end integrados, funcionando como uma rede social privada focada em grupos de saúde e fitness, mas também funcionando com ferramentas privadas com foco em promover os hábitos saudáveis menos abordados por outros aplicativos, por exemplo: leitura e tempo de descanso.

### 2.2 Funções do Produto  
- Criação e gerenciamento de grupos privados (competições).  
- Compartilhamento de posts no feed do grupo (treinos, refeições, textos, fotos, vídeos).  
- Planejador de refeições e organizador de treinos pessoais, privados.  
- Envio de notificações para hidratação e alimentação.  
- Cadastro e gerenciamento de perfil de usuário.  

### 2.3 Usuários e Características  
- Usuários comuns: interessados em saúde, fitness e bem-estar, iniciantes ou avançados, interessados em hábitos saudáveis que buscam conforto e facilidade na rotina.  
- Profissionais da saúde: podem criar grupos para seus pacientes/clientes.  
- Desenvolvedores e administradores: manter e atualizar o sistema.  

### 2.4 Restrições  
- Aplicativo deve ser responsivo e acessível para dispositivos móveis variados.  
- Privacidade dos dados pessoais e dos grupos deve ser garantida.  
- Notificações devem ser configuráveis e não invasivas.  

### 2.5 Suposições e Dependências  
- Os usuários terão smartphones compatíveis com o app.  
- O aplicativo terá acesso a notificações e sensores básicos do celular.  
- Conexão à internet será necessária para interação social e sincronização de dados.  

---

## 3. Requisitos Específicos

### 3.1 Requisitos Funcionais  

**3.1.1 Gerenciamento de Usuários**  
- RF001: O sistema deve permitir cadastro de usuário com e-mail, senha, nome e perfil.  
- RF002: O usuário pode fazer login e logout no aplicativo.  

**3.1.2 Grupos e Competições**  
- RF003: Usuário pode criar grupos privados (competições).  
- RF004: O criador do grupo pode convidar outros usuários para participar.  
- RF005: Usuário pode navegar entre grupos que participa.  
- RF006: Cada grupo terá um feed para compartilhamento de posts relacionados a treinos e alimentação.  

**3.1.3 Compartilhamento no Feed**  
- RF007: Usuários podem postar fotos, vídeos, textos e localização sobre treinos.  
- RF008: Usuários podem postar fotos e descrições de refeições.  
- RF009: Posts exibem data e horário.  

**3.1.4 Acompanhamento Pessoal**  
- RF010: Usuário pode criar e editar planejador de refeições diárias (café, almoço, jantar, lanches) com horários e cardápios personalizados.  
- RF011: Usuário pode criar e gerenciar planos de treino privados (exercícios, séries, repetições).  
- RF012: Usuário pode compartilhar o plano de treino em posts no feed, se desejar.  

**3.1.5 Notificações**  
- RF013: O aplicativo envia lembretes para hidratação em intervalos configuráveis.  
- RF014: O aplicativo envia lembretes para refeições nos horários definidos pelo usuário.  

**3.1.6 Avaliações e Métricas**  
- RF015: Usuário pode cadastrar avaliações físicas e métricas para acompanhar progresso.  

**3.1.7 Outros**  
- RF016: Usuário pode adicionar fotos para comprovar participação nas competições.  

### 3.2 Requisitos Não Funcionais  

- RNF001: O aplicativo deve ser responsivo, adaptando-se a diferentes tamanhos de telas de dispositivos móveis.  
- RNF002: Deve atender critérios básicos de acessibilidade, garantindo uso por pessoas com deficiências visuais e motoras.  
- RNF003: A privacidade dos dados deve ser preservada com autenticação segura e acesso restrito aos grupos privados.  
- RNF004: O aplicativo deve possuir tempo de resposta inferior a 3 segundos para ações principais.  
- RNF005: O sistema deve ter alta disponibilidade, com mínimas interrupções.  
- RNF006: O aplicativo deve integrar com sensores do celular para recursos futuros (exemplo: monitoramento de atividades).  

### 3.3 Requisitos de Interface  

- RI001: Tela de login e cadastro simples e intuitiva.  
- RI002: Feed do grupo deve exibir posts em ordem cronológica, com visualização fácil de fotos e vídeos.  
- RI003: Planejador de refeições e organizador de treinos devem ser acessíveis via menus claros e organizar informações de forma prática.  
- RI004: Notificações do sistema devem ser claras, personalizáveis e não intrusivas.  

### 3.4 Regras de Negócio  

- RN001: Apenas o criador do grupo pode convidar novos membros.  
- RN002: Usuários só podem visualizar conteúdos de grupos dos quais participam.  
- RN003: Posts e dados pessoais não podem ser acessados publicamente.  

---

## 4. Modelos e Diagramas  

- [Diagrama de Casos de Uso e Diagrama de classes para modelagem de dados](https://www.canva.com/design/DAGnQzlDgCQ/2OQ3NgsN1MA9wy3Vq5TteA/view?utm_content=DAGnQzlDgCQ&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h4859d73653#3)  
- [Protótipos de telas](https://www.figma.com/proto/qPLWnMVyUlS4DlqEVupjgn/IMPECTUS?node-id=36-3&t=cypSRQvQKIBYUWyA-0&scaling=scale-down&content-scaling=fixed&page-id=36%3A2&starting-point-node-id=36%3A3&show-proto-sidebar=1) (Login, Cadastro, Feed)  

---

## 5. Critérios de Aceitação  

- CA001: Usuário consegue criar, acessar e sair de grupos privados.  
- CA002: Posts no feed aparecem corretamente com fotos, vídeos e textos.  
- CA003: Planejador de refeições permite criação, edição e visualização de refeições diárias.  
- CA004: Notificações de hidratação e refeições são enviadas nos horários configurados.  
- CA005: Aplicativo funciona corretamente em dispositivos com diferentes tamanhos de tela.  
- CA006: Apenas membros autorizados visualizam conteúdos dos seus grupos.  

---

## 6. Apêndices  

- Backlog inicial com histórias de usuário:
1. Como usuário, quero cadastrar meu perfil, entrar no meu perfil e sair do meu perfil para criar o meu acesso ao aplicativo.
2. Como usuário, quero cadastrar meus treinos, sessão por sessão, para poder utilizar durante as competições.
3. Como usuário, quero cadastrar minha rotina alimentar, com horários, descrição e lembretes para não deixar de realizar a minha refeição.
4. Como usuário, quero criar competições e convidar outros usuários para participar destas competições para gerar um ranking com a data determinada por mim.
5. Como usuário, quero adicionar fotos na competição com os meus treinos já criados marcando a conclusão do treino para comprovar minha participação diária.
6. Como usuário, quero adicionar fotos das minhas refeições com seus respectivos horários e descrições para comprovar que estou realizando tudo que foi proposto na minha rotina alimentar.
7. Como usuário, quero que o aplicativo bombardeie notificações ao longo do dia com lembretes de beber água para me manter hidratado durante o dia.
8. Como usuário, quero cadastrar avaliações físicas e métricas para poder comparar com o meu futuro progresso.
9. Como usuário, quero navegar entre competições para poder visualizar como está indo cada competição que estou participando.
10. Como desenvolvedor, quero que o aplicativo seja responsivo e acessível para todas as pessoas conseguir utilizar em qualquer celular.  
- Documentos de visão e planejamento das sprints estão nessa organization, no README.md e em projects, sprint's, respectivamente.  

# Documento de Requisitos de Software (DRS)

## 1. Introdução

### 1.1 Objetivo  
Este documento tem como objetivo definir os requisitos funcionais e não funcionais para o desenvolvimento do Aplicativo de Apoio a Atividades Físicas e Saúde Mental, uma rede social privada para grupos focados em vida fitness, saúde e bem-estar, promovendo apoio mútuo, compartilhamento e motivação.

### 1.2 Escopo  
O aplicativo permitirá a criação e gestão de grupos privados (competições), compartilhamento de treinos e refeições no feed do grupo, acompanhamento pessoal com planejador de refeições e treinos, além de lembretes de hidratação e alimentação. Será uma ferramenta para usuários iniciantes e experientes, incluindo profissionais da saúde.

Fora do escopo neste momento: funcionalidades relacionadas a gestão financeira e leitura, que podem ser implementadas em versões futuras.

### 1.3 Definições, Acrônimos e Abreviações  
- **Grupo / Competição**: Espaço privado criado por usuário para interação entre membros.  
- **Feed do Grupo**: Área para compartilhar posts de treino e alimentação.  
- **Planejador de Refeições**: Ferramenta para organização individual de refeições diárias.  
- **Organizador de Treinos**: Ferramenta privada para criação e gerenciamento de treinos pessoais.  

### 1.4 Referências  
- Documentação Notion com backlog e sprints: [Link do Notion]  
- Diretrizes de acessibilidade móvel  
- Padrões de notificações push em sistemas móveis  

### 1.5 Visão Geral do Documento  
O documento está organizado em seções que abordam a descrição geral do sistema, requisitos funcionais e não funcionais, modelo de dados, critérios de aceitação e considerações adicionais.

---

## 2. Descrição Geral

### 2.1 Perspectiva do Produto  
O aplicativo será uma plataforma móvel, com back-end e front-end integrados, funcionando como uma rede social privada focada em grupos de saúde e fitness.

### 2.2 Funções do Produto  
- Criação e gerenciamento de grupos privados (competições).  
- Compartilhamento de posts no feed do grupo (treinos, refeições, textos, fotos, vídeos).  
- Planejador de refeições e organizador de treinos pessoais, privados.  
- Envio de notificações para hidratação e alimentação.  
- Cadastro e gerenciamento de perfil de usuário.  

### 2.3 Usuários e Características  
- Usuários comuns: interessados em saúde, fitness e bem-estar, iniciantes ou avançados.  
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

- Diagrama de Casos de Uso (em anexo ou link para PlantUML/draw.io)  
- Diagramas de classes para modelagem de dados (a ser desenvolvido na Sprint 2)  
- Protótipos de telas (Login, Cadastro, Feed, Perfil, Planejador de Refeições, Organizador de Treinos)  

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

- Backlog detalhado com histórias de usuário (fornecido via Notion).  
- Link para repositório Git do projeto.  
- Documentos de visão e planejamento das sprints.  

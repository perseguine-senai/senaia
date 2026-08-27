# SenaIA

Assistente virtual conversacional para tirar dúvidas sobre a Escola SENAI São Carlos - "Antonio A. Lobbe" (Unidade 601).

## Objetivo

Centralizar, em um único canal conversacional, as informações da Escola SENAI São Carlos - cursos, processo seletivo, datas de eventos, localização, história da unidade, parcerias e demais dados institucionais - garantindo respostas rápidas, personalizadas e com direcionamento exato (links, prazos e passos) para os estudantes.

## Motivação

As informações da Unidade 601 estão fragmentadas em múltiplos canais: o site institucional do SENAI-SP, a página da unidade, redes sociais e conhecimento informal repassado entre alunos. Não existe um canal único, conversacional e imediato que centralize essas respostas.

Essa dispersão gera perda de prazos de processo seletivo, desconhecimento de oportunidades (Mural de Estágio/Emprego), dificuldade para localizar serviços básicos (2ª via de boleto, horários) e confusão entre as diferentes modalidades de curso oferecidas. Resolver esse problema reduz o retrabalho do atendimento presencial e da secretaria da escola e substitui a espera por um canal humano por uma resposta imediata, disponível a qualquer hora.

## Estado da arte

Chatbots educacionais já são uma tendência consolidada, usados para responder dúvidas 24 horas por dia e reduzir a sobrecarga de secretarias. Dentro do próprio Sistema SENAI já existem iniciativas nesse sentido: o Cadu (SENAI-RN), integrado ao Google Assistente; o Cadu do app Estante Virtual Meu SENAI, focado em quizzes e apoio ao estudo; e o TECH (SESI/SENAI-ES), via WhatsApp, para segunda via de boleto. Em outras instituições, exemplos incluem o Téo (Estácio) e o Paul (Saint Paul), além de trabalhos acadêmicos recentes como o Sabiá e o MICA, chatbots de IA generativa criados justamente para resolver a dispersão de informações institucionais.

A maioria dessas soluções é genérica (matrícula, boletos, notas) ou não é personalizada por curso. O SenaIA se diferencia por ser hiperlocal (exclusivo da Unidade 601), ter uma persona de atendimento própria (a Carla) e personalizar as respostas pela trilha de curso de cada aluno.

## Descrição

Sistema web responsivo (Mobile e Desktop) com login via Google, no qual o aluno informa seu curso ou área de atuação dentro do SENAI. Essa informação é usada como contexto persistente pela assistente virtual Carla, integrada a uma API de IA, para personalizar as respostas em cada conversa. A Carla tem personalidade gentil, simpática e acolhedora, priorizando bondade e conexão entre alunos, professores e funcionários da Unidade 601.

O escopo do projeto é propositalmente enxuto: o esforço de desenvolvimento é concentrado no que sustenta o valor real do produto, o chat com IA e a personalização por curso, enquanto o restante da interface é reduzido ao essencial, com visual limpo e direto.

Requisitos funcionais principais:
- Autenticação via Google (OAuth), implementada de forma real, sem cadastro manual
- Perfil do usuário com curso/área de atuação, capturado no primeiro acesso
- Personalização contextual: o perfil é usado em todas as interações da Carla
- Chat conversacional com respostas sobre cursos, vagas, processo seletivo, eventos, localização, história e parcerias
- Direcionamento com links diretos e instruções passo a passo
- Lista simplificada das últimas conversas, acessível pelo menu lateral

Requisitos não-funcionais principais:
- Interface responsiva entre Mobile e Desktop
- Performance com resposta em tempo real
- Resiliência da API de IA (fallback em caso de indisponibilidade ou limite de uso)

## Persona

Beatriz, 17 anos, estudante do SENAI São Carlos.

"Eu não sei onde encontrar as informações que preciso sobre o SENAI, tudo tá espalhado e eu perco tempo procurando."

Estudante de curso técnico, superior ou de outra modalidade oferecida pela Unidade 601. Busca se desenvolver na escola, não quer perder oportunidades e quer se manter conectada com tudo o que o SENAI oferece.

Desafios diários: dificuldade em achar datas de processo seletivo e editais, confusão entre os tipos de curso, dificuldade de navegação no site institucional, desconhecimento sobre eventos e oportunidades.

Objetivos com o sistema: tirar dúvidas rapidamente, não perder prazos ou oportunidades, sentir que a escola está acessível mesmo fora do horário de atendimento.

## Wireframe

Fluxo de telas definido (4 telas), com a tela de Chat como núcleo da experiência:

1. Login - autenticação via Google (OAuth)
2. Boas-vindas / Setup - apresentação da Carla e captura do curso/área do aluno (primeiro acesso)
3. Chat - tela principal de conversa com a Carla, com sugestões rápidas e menu lateral com acesso às últimas conversas e ao perfil
4. Perfil / Configurações - nome, foto, curso/área e preferências básicas

Wireframes de alta fidelidade já desenhados para Desktop e Mobile. A primeira versão do produto, no entanto, será voltada apenas para Desktop - a versão Mobile fica definida como próxima etapa de desenvolvimento.

## Design

Paleta de cores: branco como cor principal, com o vermelho institucional do SENAI-SP (#C00D0D) como cor de destaque/apoio.

Identidade visual aplicada nas telas: logotipo SenaIA, tela de login com bloco de destaque em vermelho, chat com bolhas de conversa e sugestões rápidas (Cursos, Processo Seletivo, Boletos, Localização), e perfil com dados do aluno e curso vindos do login com Google.

Tecnologias de front-end: HTML5 semântico e CSS3 (Flexbox e Grid).

## Equipe

- Ariani Almeida
- Bryan Perseguine
- Paloma Oliveira

Execução: 2026 / 2º Semestre - Início: 30/07/2026

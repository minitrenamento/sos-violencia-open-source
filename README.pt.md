# SOS Violência — versão pública para revisão de código sob Apache-2.0

[English](README.md) | **Português**

Copyright 2026 **LANDI CONSULTORES, SU, LDA**.
As contribuições próprias são licenciadas sob a [Licença Apache 2.0](LICENSE); consulte também o [NOTICE](NOTICE) e os [avisos de terceiros](THIRD_PARTY_NOTICES.md).

**Não publicada nem implementada em produção. Não é um serviço de emergência. Não introduza casos reais nem credenciais.**
Esta versão foi preparada para apoiar a revisão de uma candidatura de financiamento à UNICEF; não reivindica endosso, parceria, elegibilidade, financiamento ou acordo operacional com a UNICEF ou com entidades governamentais.

SOS Violência é um projeto orientado para Moçambique, criado para apoiar alertas e denúncias de violência por cidadãos através de uma aplicação móvel e de um painel para operadores. Inclui funcionalidades de acessibilidade e apoio opcional à decisão assistido por IA. O projeto destina-se a apoiar mulheres, raparigas e outras pessoas em situação de risco, mantendo responsabilidades humanas de proteção e salvaguarda.

## Distribuição
Código existente da aplicação Expo: `artifacts/sos-mozambique/`; painel React: `artifacts/dashboard/`; API Express: `artifacts/api-server/`; contratos e bibliotecas partilhadas: `lib/`; referências SQL históricas: `migrations/` e `supabase/migrations/`. Os nomes técnicos das pastas foram mantidos.

Este é um **pacote bloqueado para revisão de código-fonte**, e não uma demonstração funcional da aplicação móvel ou do painel operacional. Inclui apenas dados fictícios, recursos de exemplo e configurações não operacionais. Os pontos de integração e autenticação estão bloqueados; simplesmente definir variáveis de ambiente não os ativa. A ferramenta de revisão não fornece despacho real, recolha de GPS, criação de contas, upload, notificações push, IA ativa ou USSD. Não se afirma que exista build completo, implementação ou validação em campo.

## Revisão rápida (Node.js 22+)
```sh
node tools/verify-release.mjs
node tools/review.mjs
```
Não é necessário instalar dependências, iniciar servidores, fornecer credenciais ou usar a rede para executar estes comandos.
Nunca copie o histórico do repositório privado original. Publique apenas este diretório num novo repositório, conforme autorizado em `PUBLICATION_APPROVAL.md`. Nunca publique o projeto original nem o seu histórico.

## Estado
- **Implementado no código histórico:** seis módulos SOS, relatórios/média, histórico e persistência local, perfis/contactos, acessibilidade, notificações, gestão de operadores e triagem opcional por IA.
- **Desativado na versão pública:** integrações reais, autenticação, migrações, ações de comunicação, arranque/build da aplicação e geração de código. Apenas dados estáticos de revisão.
- **Planeado, não implementado:** USSD para telefones básicos ou utilização com acesso limitado à Internet; depende de acordos com operadores e requisitos regulatórios. Este pacote não contém um shortcode real nem reivindica parceria.
- **IA:** apenas apoio à decisão, exigindo revisão humana qualificada; não existe despacho autónomo nem recusa automática de ajuda, e não se afirma que já exista um fluxo obrigatório de aprovação humana implementado.

## Documentos
[Arquitetura](docs/ARCHITECTURE.md) · [Funcionalidades](docs/FEATURES.md) · [Configuração](docs/SETUP.md) · [Segurança](SECURITY.md) · [Privacidade](PRIVACY.md) · [Salvaguarda](SAFEGUARDING.md) · [Contribuição](CONTRIBUTING.md) · [Roadmap](ROADMAP.md) · [Revisão de segurança](docs/SECURITY_REVIEW.md) · [Decisões resolvidas](MANUAL_REVIEW.md) · [Autorização de publicação](PUBLICATION_APPROVAL.md) · [Verificação](VERIFICATION.md)

## Autorização de publicação e âmbito de redistribuição
O mantenedor aprova **apenas este pacote sanitizado e não executável** para um novo repositório público com histórico limpo. Consulte `PUBLICATION_APPROVAL.md`. Foram removidas cópias genéricas de templates sem proveniência exata e ferramentas não utilizadas; duas superfícies mínimas de interface substituem imports necessários. Esta versão não é uma cópia executável completa da aplicação privada. Vulnerabilidades de dependências ainda existentes são divulgadas, e não consideradas aprovadas para utilização em produção.

Contacto privado para vulnerabilidades: `security@landiconsultores.co.mz`.
Nenhuma implementação de dependências nem ficheiros binários de fontes/ícones de terceiros é incluída; as respetivas licenças permanecem propriedade dos seus titulares.

## Supabase preservado e estado final das dependências
O Supabase continua a ser a plataforma principal prevista para backend, dados e armazenamento; não foi removido nem substituído. Consulte `docs/SUPABASE_SECURITY_REVIEW.md` para placeholders públicos, segredos exclusivos do servidor, RLS obrigatório em tabelas sensíveis, limites de sessão/autorização e requisitos de evidência privada.

A revisão mais recente reduziu as ocorrências de dependências para **0 críticas, 2 altas e 2 moderadas**. As ocorrências restantes pertencem ao toolchain legado desativado, e não ao conjunto auditado do SDK do Supabase. Algumas atualizações de versões principais foram aceites após verificações offline de interfaces, e não após um build completo da aplicação.

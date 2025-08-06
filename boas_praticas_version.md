# Boas práticas de versionamento
Aqui está um compilado de melhores práticas de versionamento com Git, reunindo recomendações de fontes especializadas, fóruns técnicos e comunidades de desenvolvedores. O objetivo é oferecer conteúdo útil, claro e aplicável que ajude pessoas a adotarem um fluxo eficiente e confiável de trabalho com código:
## 🧠 Melhores Práticas de Versionamento com GIT
### 1. Commits pequenos, atômicos e frequentes
- Faça alterações mínimas por commit — cada um deve ser uma unidade lógica isolada (bug fix, feature, refatoração)
- Commits menores facilitam revisões e reverts. Mesmo commits grandes!
---
### 2. Mensagens de forma estratégica
- Comece com verbo no imperativo (“Fix login bug”, “Add payment API”) e mantenha o título curto (<50 caracteres) seguido de um corpo explicativo se necessário.
- Evite mensagens vagas como “changes” ou “update”.
---
### 3. Use branches de forma estratégica
- Trabalhe sempre em branches separadas: `feature/`, `bugfix/`, `hotfix/`, mantendo main sempre estável 
- Utilize workflows como GitHub Flow ou GitFlow, conforme o tamanho do time e tipo de projeto 
---
### 4. Sincronize e compartilhe frequentemente
- Dê push das suas alterações regularmente; o remoto deve ser a **fonte oficial da verdade** 
- Sempre faça pull antes de começar a desenvolver, para evitar conflitos 
---
### 5. Mantenha o repositório limpo com `.gitignore`
- Não versionar arquivos gerados automaticamente (build, logs, binários, `.env`) evita inflar o repositório e conflitos inúteis
- Atualize sempre o .`gitignore` conforme novas ferramentas e dependências são adicionadas.
---
### 6. Use tags e releases para marcar versões estáveis
- Ao lançar uma versão, crie uma tag (`git tag v1.0.0 -m "Release inicial`") e faça git push origin v1.0.0 para marcação formal.
- Facilita rollback e busca por versões em ambientes de produção.
---
### 7. Adote revisão de código via Pull Requestes
- Em equipes, evite mesclagem direta na branch principal. Use PRs para discutir o código e garantir qualidade antes de integrar
---
### 8. Nunca reescreva histórico compartilhado
- Evite `git rebase` ou `git push --force` em branches que já foram compartilhadas—isso pode causar conflitos graves nos repositórios dos colegas.
---
### 9. Gerencie segredos e credenciais com cuidado
- Nunca versionar senhas ou chaves diretamente no código. Use `.env`, services de secret management ou variáveis de ambiente seguras
- Utilize scanners automáticos (ex: GitGuardian) para evitar commits acidentais com dados sensíveis.
---
### 10. Conheça e cuida das ferramentas de merge
- Aprenda a usar um merge tool confiável (GUI ou terminal) e pratique resolução de conflitos antes que surgem estresse real em prazos apertados.
---
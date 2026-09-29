 Laboratório CI/CD - Entrega

## 1. As 3 Histórias do Pedido

**User Story (História do Usuário):**
Como aluno desenvolvedor, quero publicar um site estático no GitHub Pages de forma automática, para que eu não precise fazer o upload manual toda vez que eu alterar o código.

**Test Story (História de Teste):**
Como robô de verificação (GitHub Actions), quero checar se o arquivo index.html existe, se ele contém a tag <title> e se o código está completo (terminando com </html>), para que eu impeça a publicação de um site quebrado ou fora do ar.

**Ops Story (História de Operações):**
Como responsável pela infraestrutura, quero que o robô execute os testes em uma aba separada (Actions) e só faça o deploy (publicação) se todas as verificações passarem, para que o site em produção esteja sempre na sua versão mais estável e correta.

---

## 2. Respostas às Perguntas

**1. Qual foi a User Story, a Test Story e a Ops Story do seu pedido?**
R: São as três histórias descritas acima. A User Story foca na minha necessidade de publicar sem trabalho manual. A Test Story foca no que o robô precisa verificar para garantir a qualidade. E a Ops Story foca na regra de que só publica se passar no teste.

**2. O checklist da Test Story pegou algum problema antes da publicação?**
R: Sim. Quando enviamos o arquivo "2-quebrado" (que estava incompleto), o checklist do robô pegou o problema. Ele detectou que faltava o fechamento correto do HTML e bloqueou a publicação, evitando que o site ficasse fora do ar.

**3. O que a Ops Story previu que a aba Actions confirmou (ou não)?**
R: A Ops Story previu que o deploy só aconteceria se os testes passassem. A aba Actions confirmou isso na prática: quando o arquivo estava quebrado, o robô marcou a verificação como falha (❌) e não executou o passo de publicação, mantendo a última versão boa do site no ar.

**4. O que mudaria se vocês só tivessem escrito a User Story?**
R: Se tivéssemos apenas a User Story, não teríamos os testes automatizados (Test Story) nem as regras de bloqueio (Ops Story). O arquivo quebrado teria sido publicado diretamente, e o site teria ficado corrompido ou fora do ar, sem que ninguém percebesse a tempo.

**5. Qual das 3 histórias foi mais difícil de escrever e por quê?**
R: A Ops Story foi a mais difícil, porque exige pensar na infraestrutura e no comportamento do robô em situações de falha (o que fazer se o teste não passar?). É mais fácil pensar na User Story (que é a necessidade do usuário) do que nas regras técnicas de operação.

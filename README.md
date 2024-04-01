# DataGlowUP32
Minha inscrição no desafio 32 do Data Glow UP

Analisei os dados do SUS relacionados a notificações de síndrome gripal para o Estado de São Paulo (https://opendatasus.saude.gov.br/dataset/notificacoes-de-sindrome-gripal-leve-2023) e identifiquei melhorias que poderiam ser aplicadas no formulário utilizado nessas notificações.

O formulário utilizado possui somente 10 opções que podem ser assinaladas. Mais de uma opção pode ser marcada:
 - Assintomático
 - Febre
 - Dor de Garganta
 - Dispneia
 - Tosse
 - Coriza
 - Dor de Cabeça
 - Distúrbios gustativos
 - Distúrbios olfativos
 - Outros

Ao compilar esses dados, verifiquei que a opção "Outros" foi assinalada mais de 1 milhão de vezes, ficando na 6ª colocação.

Achei muito. Decidi explorar o que foi marcado nessa opção.

Foi aí que identifiquei que tinham sintomas relevantes marcados ali. Mialgia foi bastante frequente.

Só foi necessário tratar um pouco esses dados, pois mialgia, por exemplo, estava escrito em grafias diferentes, além de ser descrito com outros termos (ex: dor no corpo, dor no peito, dor no tórax, etc...)

Também identifiquei que foi assinalada a opção "Outros" para sintomas como Dor de Cabeça, Dispneia e Coriza, apesar de já existir uma opção padrão para isso no formulário.

Fiz a tratativa nos principais itens, criei novas categorias de sintomas e adicionei num DataFrame para apresentá-los num gráfico e o resultado foi esse:

A opção "Outros" reduziu significativamente, mas ainda representa um volume grande em relação aos demais sintomas.

As novas categorias não possuem tantas ocorrências assim (especialmente Fadiga, Espirro e Diarréia), mas talvez isso seja assim porque:
- É necessário tratar ainda mais esses dados para categorizá-los
- A ausência de sintomas como opção padrão no formulário pode causar uma subnotificação desses sintomas (o paciente possui o sintoma mas não o comunica se não for indagado diretamente)

Isso são apenas hipóteses. Somente uma análise mais aprofundada da rotina dos profissionais responsáveis por essa notificação poderia cravar isso.

A partir da análise das notificações de síndrome gripal no Estado de São Paulo, chego na conclusão de que essa base de dados ficaria mais rica se:
- Novas opções de sintomas comuns como Dor no Corpo (Mialgia), Fadiga, Espirro e Diarréia forem adicionadas no formulário/sistema
- Opções com termos não tão conhecidos tiverem outras denominações para exemplificar para quem está preenchendo, de modo a evitar o uso sem necessidade da opção "Outros" (ex: Falta de Ar (Dispneia), Congestão Nasal (Coriza))
- Treinar os responsáveis para que utilizem a opção "Outros" somente se o sintoma não estiver listado nas opções padrão (esse é um pouco mais difícil de fazer, considerando o SUS e a quantidade de pessoas envolvidas, mas contribuiria para melhorar os dados)

Tá aí! Gostei de fazer, melhorei bastante nas habilidades com Python e Pandas.

Aguardandando o próximo desafio!

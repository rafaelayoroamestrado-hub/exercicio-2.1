Esta é a V3 do Mapeamento de Atores, revisada para sanar as inconsistências factuais, conceituais e de evidência apontadas na Auditoria V2. O relatório agora diferencia rigorosamente fatos documentados de inferências técnicas e hipóteses operacionais.Relatório de Mapeamento V3: Ecossistema do Seguro-Desemprego (URA Caixa)1. Matriz de Atores (Revisada e Validada)\[C] Corrige Falhas 7, 13, 14, 15, 27, 28, 29 da Auditoria V2





AtorPapel e Vínculo FuncionalTipologiaVisibilidadeCidadãoRequerente do benefício; usuário do canal de consulta.DemandanteLinha de FrenteAtendente HumanoSuporte operacional para dúvidas de pagamento e PIS.ExecutorLinha de FrenteCaixa EconômicaAgente Pagador: Opera o 0800 e paga o benefício.IntermediárioBackstageMTE (Ministério do Trabalho)Gestor da Política: Define regras e opera o 158.ReguladorBackstageDataprevProcessador: Gere o sistema de análise de direito.Executor TécnicoBackstageEmpresa de BPOOperadora do Call Center (Contrato de Terceirização).FornecedorBackstageFiscal do Contrato (Caixa)Monitora SLAs e conformidade da prestadora de BPO.Auditor/GestorBackstageEncarregado (DPO)Ponto de contato para governança de dados (LGPD).GovernançaBackstageICOM / IntérpretesProvedor de intermediação em Libras por videochamada.FornecedorLinha de Frente2. Jornada Operacional e Canais de Entrada\[C] Corrige Falhas 1, 3, 4, 5, 8, 9, 10, 31, 33, 34 e Erros Factuais 1, 2, 5, 10 da Auditoria V2A jornada do Seguro-Desemprego é fragmentada entre dois órgãos distintos, o que exige cautela na atribuição de responsabilidades:

Entrada e Agendamento: \[C-Erro 2, 5] Ao contrário da V2, o agendamento para atendimento presencial nas Superintendências Regionais do Trabalho ocorre via Central Alô Trabalho 158 (MTE), e não pela URA da Caixa. A Caixa atua na consulta de parcelas já liberadas.

Consulta de Pagamento (0800 726 0207): Canal oficial da Caixa para informações sobre PIS e Benefícios Sociais.

Horário de Atendimento Humano: \[C-Erro 1] O atendimento humano na Caixa ocorre de segunda a sexta, das 8h às 21h, e aos sábados, das 10h às 16h, conforme dados oficiais do portal de atendimento da instituição.

Transbordo Humano: \[D-Falha 10] O transbordo é acionado quando o CPF/NIS não é reconhecido ou quando o cidadão solicita falar com um atendente para esclarecer bloqueios de pagamento. \[C-Erro 4] O termo "Malha Fina" é corrigido para "Divergência Cadastral ou Notificação de Recurso", conforme nomenclatura do MTE.

Governança de Conteúdo: \[P-Falha 31] A existência de um Product Owner (PO) específico para os scripts da URA é uma hipótese organizacional pendente de confirmação via organograma interno da Caixa.

3\. Infraestrutura Técnica e Dados\[C] Corrige Falhas 6, 12, 30 e Erros Factuais 3, 8, 11, 12 da Auditoria V2

Integração Sistêmica: \[C-Erro 3] A Lei nº 7.998/1990 fundamenta o direito ao benefício, mas a arquitetura técnica é regida por Acordos de Cooperação Técnica entre MTE, Caixa e Dataprev. A URA consome dados da Dataprev para informar o status do requerimento.

Fornecedor de BPO: \[C-Erro 8] O nome da empresa prestadora é pendente de verificação no Portal da Transparência, uma vez que contratos de Call Center são renovados periodicamente.

Acessibilidade: \[C-Erro 9] O atendimento para surdos é realizado via videochamada com intérpretes de Libras (parceria ICOM), substituindo a nomenclatura "CAS" utilizada erroneamente na versão anterior.

Tecnologia de Voz: \[P-Falha 6] O uso de ASR (Reconhecimento de Voz) ou TTS (Síntese) é uma inferência baseada em padrões de mercado para URAs bancárias de grande porte, mas carece de memorial descritivo técnico oficial.

4\. Controle, Regulação e Omissões\[C] Corrige Falhas 15, 16, 26 e Erros Factuais 6, 7, 13, 14 da Auditoria V2

Órgãos de Controle: \[C-Erro 6] TCU e CGU fiscalizam a regularidade dos pagamentos e a gestão do FAT, não necessariamente a "eficiência da árvore de voz" da URA, a menos que haja auditoria de desempenho específica.

Regulação Setorial: A ANATEL regula as operadoras que fornecem os links E1/SIP para a Caixa, garantindo a continuidade do serviço telefônico.

Proteção de Dados: \[C-Erro 7] O DPO (Encarregado) coordena a conformidade. A ANPD (Autoridade Nacional de Proteção de Dados) é o ator regulador externo em caso de incidentes com dados dos beneficiários.

5\. Conclusão e Síntese de Interdependência\[C] Corrige Falhas 20, 22 e Erros Factuais 14 da Auditoria V2A jornada do Seguro-Desemprego via URA é um serviço de interface compartilhada. A Caixa provê a infraestrutura de atendimento (0800/URA), mas a "inteligência" (decisão de quem recebe) pertence ao MTE, processada tecnicamente pela Dataprev.Ponto Crítico de Falha: O maior risco operacional reside no delay de atualização entre o sistema de concessão (MTE/Dataprev) e o sistema de pagamento (Caixa). Quando o cidadão ouve na URA que "não há parcelas", a falha pode estar no fluxo de dados entre esses atores, e não necessariamente no canal telefônico.\[C] Falha 2, 24, 35: As fontes utilizadas para esta revisão incluem o portal oficial da Caixa (Atendimento e Seguro-Desemprego) e o portal Gov.br (MTE/Alô Trabalho). Este relatório v3 adota um tom de cautela técnica, marcando explicitamente o que é dado oficial e o que é inferência.


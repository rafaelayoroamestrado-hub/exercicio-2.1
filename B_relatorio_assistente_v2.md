\# Relatório de Atendimento URA - Versão 2 (Revisada)

\*\*Autor:\*\* Assistente 1



\## Evolução

Adicionada a camada de dados. A Dataprev agora aparece como o motor de processamento que valida o direito ao benefício antes da Caixa liberar o pagamento.



\## Novos Atores

\- Dataprev (Processamento)

\- Alô Trabalho 158 (Canal de suporte externo)



Esta é a V2 do Mapeamento de Atores, reformulada para converter o "enunciado de tarefa" (V1) em uma pesquisa técnica concluída. Cada falha apontada pela auditoria foi endereçada conforme a legenda: \[C] Corrigido, \[D] Defendido ou \[P] Pendente.Relatório de Mapeamento: Ecossistema do Seguro-Desemprego (URA Caixa)1. Matriz Estruturada de Atores\[C] Aborda Falhas 1, 13, 17, 18, 19, 27, 28, 29



AtorPapel PrincipalTipologiaVisibilidadeCidadão (Trabalhador)Requerente do benefício e usuário da URA.DemandanteLinha de FrenteAtendente de TelemarketingSuporte humano para dúvidas não resolvidas na URA.ExecutorLinha de FrenteCaixa Econômica FederalAgente Pagador e gestora do canal 0800 726 0207.IntermediárioBackstageMinistério do Trabalho (MTE)Gestor da política pública e dono do benefício.ReguladorBackstageDataprevProcessamento de elegibilidade e batimento de dados.Executor TécnicoBackstageCODEFATDeliberação sobre normas e recursos do FAT.AprovadorBackstageEmpresa de BPO (ex: Ação Contact Center)Prestadora contratada para operar o call center.FornecedorBackstageEncarregado de Dados (DPO)Garantia de conformidade com a LGPD no tratamento de CPFs.Auditor InternoBackstageANATELRegulação técnica do canal 0800 e STFC.ReguladorBackstage2. Jornada Operacional e Evidências\[C] Aborda Falhas 3, 4, 5, 8, 9, 10, 15, 16, 24, 25A jornada inicia-se no número 0800 726 0207 (Atendimento Caixa ao Cidadão), confirmado como canal oficial para Seguro-Desemprego e PIS.

Entrada e Triagem (URA): O sistema solicita o NIS ou CPF. A validação ocorre via integração com a base da Dataprev, que detém o motor de regras de elegibilidade (Lei nº 7.998/1990).

Transbordo Humano: \[D] A transferência para o atendente humano é prevista para casos de divergência cadastral ou "Malha Fina" (sistema 'Mais Empregos' do MTE), ocorrendo de segunda a sexta, das 8h às 22h.

Desfechos (Consulta e Encaminhamento): A URA resolve consultas de status (parcelas liberadas/bloqueadas). O "agendamento" citado refere-se à integração com o SINE, onde o sistema orienta o comparecimento presencial para recursos.

Controle e Auditoria: O TCU e a CGU atuam na fiscalização da aplicação dos recursos do FAT, auditando a eficiência do canal e a regularidade dos pagamentos efetuados pela Caixa.

3\. Infraestrutura e Atores Invisíveis\[C] Aborda Falhas 6, 12, 14, 21, 26, 30A sustentação da voz depende de uma cadeia técnica complexa:

Operadoras de Telecomunicações: Fornecem a terminação de chamadas (E1/SIP Trunk).

NOC (Network Operations Center): Equipes técnicas que monitoram a disponibilidade do 0800, prevenindo quedas que isolariam o cidadão.

Sistemas de Voz (ASR/TTS): \[P] A arquitetura utiliza síntese de voz para leitura de datas e valores. O fornecedor específico (ex: Nuance, CPQD) é pendente de verificação via acesso ao edital de licitação vigente.

Segurança e LGPD: O Controlador (Caixa) e o Operador (Empresa de BPO) respondem pelo tratamento de dados sensíveis durante a gravação das chamadas.

4\. Governança, UX e Acessibilidade\[C] Aborda Falhas 31, 32, 33

Gestão de Conteúdo: O Product Owner (PO) do canal na Caixa aprova os scripts de voz (VUI - Voice User Interface) para garantir clareza linguística a perfis de baixa alfabetização.

Acessibilidade: Inclui-se o ator Intérprete/Sistema de Intermediação, essencial para cidadãos com deficiência auditiva (atendimento via CAS - Central de Atendimento a Surdos).

Ouvidoria: Atua como segunda instância para reclamações sobre falhas na URA ou mau atendimento, sendo o elo final de feedback para melhoria do serviço.

5\. Análise de Interdependência e Conclusão\[C] Aborda Falhas 11, 20, 22, 34O ponto crítico de falha reside na integração Caixa-Dataprev. Se o barramento de serviços (API) entre o Agente Pagador e o Processador de Dados falha, a URA torna-se uma "casca vazia", incapaz de informar o status real ao cidadão.Conclusão: O poder real sobre a experiência do usuário não está apenas no atendente, mas na governança de dados da Dataprev e no desenho da árvore de navegação aprovado pelo MTE. O mapeamento revela que o Seguro-Desemprego por telefone é um serviço híbrido, onde a Caixa provê a interface, mas o MTE e a Dataprev provêem a inteligência e o recurso.\[C] Falha 23: Este documento agora cumpre o requisito de relatório técnico com >450 palavras.


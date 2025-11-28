# Desafio-de-Ciberseguran-a-Ransomware-e-Keylogger-em-Python
Projeto educacional desenvolvido para o desafio da DIO, com foco em entender o funcionamento de malwares simulados (Ransomware + Keylogger), boas práticas de defesa e documentação técnica.

Objetivos do Projeto: Entender como um Ransomware funciona na prática (criptografia + “resgate”), implementar um Keylogger simples (captura de teclas + envio por e-mail), aprender sobre riscos, prevenção, detecção e mitigação, documentar o processo como um profissional de cibersegurança, utilizar o GitHub como portfólio técnico.

Ransomware Simulado:Este ransomware NÃO causa danos reais, apenas criptografa arquivos dentro da pasta /arquivos, a descriptografia só ocorre com chave.key, gera uma mensagem simulando um “resgate”.

Criptografia – criptografar.py
Este script: Gera uma chave única (chave.key), criptografa todos os arquivos da pasta arquivos, sobrescreve os arquivos com sua versão criptografada.

Descriptografia – descriptografar.py
Este script:Lê a chave usada na criptografia, restaura todos os arquivos à sua forma original.
Mensagem de “resgate”

Arquivo: LEIA_IMPORTANTE.txt
Simula o comportamento de ransomware:
"Seus arquivos foram criptografados! Use a chave para recuperar."

Keylogger Simulado
O keylogger implementado aqui é educacional e funciona apenas no computador local.
Ele: Captura teclas digitadas, salva em log_teclas.txt, pode enviar o log automaticamente por e-mail.

Keylogger – keylogger.py
Captura pressionamentos de teclas usando pynput.

Envio Automático – enviar_email.py

Envia o conteúdo do log por e-mail usando Gmail com senha de app.
Requer configurar “senha de app” no Gmail

Reflexão sobre Defesa e Prevenção
Como detectar malware? Comportamento anômalo (CPU alta, processos desconhecidos), arquivos alterados repentinamente, acesso suspeito ao teclado, tráfego de rede incomum

Como se proteger: Antivírus atualizado, firewall ativo, monitoramento de integridade de arquivos, não baixar anexos desconhecidos, controles de acessos.
Conscientização: A maior parte dos ataques explora FALHAS HUMANAS, treinamento e boas práticas são essenciais.

Executando o projeto:
pip install cryptography
pip install pynput

Testar o ransomware:
Coloque arquivos na pasta /arquivos
Execute:
python criptografar.py

python descriptografar.py

log será salvo em: log_teclas.txt

Para enviar por e-mail: python enviar_email.py

Este projeto demonstra, de forma controlada e educacional, como malwares operam e como profissionais de cibersegurança podem:
Detectar, entender, mitigar, proteger usuários e sistemas.
Ele serve como base para estudos mais avançados em segurança ofensiva e defensiva.
(ainda são minhas primeiras experiências no Github, se fiz algo errado, quero corrigir o erro, aceito trocas e sugestões)

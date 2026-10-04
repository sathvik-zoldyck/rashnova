<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova, a caixa-preta do seu notebook, da Alcyone Secure" width="100%">

# Rashnova

### Um gravador de atividade para Windows que deixa qualquer adulteração à vista

**Entregue o seu PC. Receba-o de volta com um registro selado do que foi feito com ele.**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**Baixar**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**Site**](https://www.alcyonesecure.com) ·
[**Limites conhecidos**](KNOWN_LIMITS.md) ·
[**Privacidade**](#privacy) ·
[**Segurança**](SECURITY.md)

</div>

> **Idiomas** &nbsp;·&nbsp; [English](README.md) · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · **Português** · [日本語](README.ja.md) · [Bahasa Indonesia](README.id.md) · [עברית](README.he.md)

---
> [!NOTE]
> Esta página foi traduzida do inglês. O aplicativo Rashnova está em inglês, por isso os nomes de botões e telas aparecem
> aqui em inglês. Se esta página e a [versão em inglês](README.md) forem diferentes, vale a versão em inglês.


O Rashnova registra o que acontece em um PC com Windows enquanto outra pessoa está com ele: na assistência técnica,
no suporte de TI ou com qualquer pessoa a quem você o entregue. Inicie uma **Repair session** antes de entregá-lo. Quando
o PC voltar, encerre-a, e o Rashnova lhe dá um veredito e um relatório do que foi aberto, copiado, renomeado e excluído,
quais programas foram executados e quais pendrives foram conectados.

Cada entrada é selada à anterior, então o registro mostra se algo nele foi alterado ou removido, e mostra cada
intervalo em que nada pôde ser registrado. Tudo fica no seu computador. Sem conta, sem nuvem, sem telemetria.


> [!NOTE]
> Este repositório é onde o Rashnova é **publicado**: instaladores, notas de versão, limites conhecidos e política
> de segurança. O Rashnova é software proprietário da [Alcyone Secure](https://www.alcyonesecure.com); o código-fonte não é
> publicado aqui.


## Conteúdo

- [Por que o Rashnova existe](#why)
- [O que ele faz](#what-it-does)
- [O que ele nunca registra](#never)
- [Como funciona](#how)
- [Download e instalação](#download)
- [Requisitos do sistema](#requirements)
- [Privacidade](#privacy)
- [Limites conhecidos](#limits)
- [Atualizações](#updates)
- [Ajuda e segurança](#support)
- [Licença](#licence)

<a name="why"></a>
## Por que o Rashnova existe

Aviões, trens e navios têm caixa-preta. Um computador que sai das suas mãos não tem nada, e quem está com ele tem
acesso a tudo o que há nele.

E esse acesso é usado. Em um [estudo de 2022 de pesquisadores da Universidade de Guelph](https://arxiv.org/abs/2211.05824)
(publicado no IEEE Symposium on Security and Privacy 2023), notebooks foram deixados durante uma noite em 12 assistências
técnicas, com o registro ativado. Técnicos de seis delas acessaram os dados pessoais que havia neles, e dois copiaram
dados do notebook. Antivírus e ferramentas de endpoint nunca foram feitos para perceber isso: a essa pessoa foram
entregues as chaves.

O Rashnova não é prevenção. É evidência, para que o que aconteceu possa ser verificado em vez de discutido.

> *Confiar é bom. Provar é melhor.*

<a name="what-it-does"></a>
## O que ele faz

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode (modo reparo).** Uma sessão vigiada, iniciada com o seu PIN antes da entrega e encerrada com o seu
PIN quando você recebe o PC de volta. Registra arquivos abertos, criados, renomeados, copiados e excluídos, programas
iniciados, comandos do PowerShell executados, logins e armazenamento USB conectado, incluindo cada arquivo gravado nele.
Reiniciar, desligar ou suspender nunca encerra a sessão: o relatório mostra cada interrupção e quanto ela durou.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="Resumo da sessão: um veredito, os eventos mais notáveis e a verificação da cadeia">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="Explorador da sessão: cada evento ao longo do tempo, por programa e por pasta">

</td>
<td width="50%" valign="top">

**Um registro que você pode verificar.** Cada sessão termina com um veredito e um relatório que você pode salvar
como PDF, página web ou planilha. O explorador da sessão mostra cada evento ao longo do tempo, por programa e por pasta,
e a verificação da cadeia diz se o registro está íntegro. O que você salva é uma cópia; o original fica onde o Rashnova
o guarda.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**O Readout semanal.** A sua semana em um veredito, com no máximo algumas coisas que vale a pena olhar. Marque
cada uma como "that was me" (fui eu) ou "that wasn't me" (não fui eu). Ele também diz, em palavras simples, o que o
Rashnova consegue e não consegue ver.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="O Readout semanal: um veredito da semana, coisas que vale a pena olhar, atividade por dia">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="A escolha entre gravar só em sessões ou sempre">

</td>
<td width="50%" valign="top">

**Gravação contínua (always-on), só se você escolher.** Desligada até você ligar. Guarda o irreversível e o
alarmante (exclusões permanentes, arquivos de aparência sensível, qualquer coisa que entre ou saia de uma unidade
removível), não o seu uso diário dos seus próprios arquivos. Desligá-la é um clique na bandeja ou em Settings, e nunca
pede o seu PIN.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Pela bandeja.** Veja que uma sessão está gravando, encerre-a, faça uma verificação de 30 segundos da atividade
de arquivos ao vivo (Monitor Now) ou abra o último relatório.

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="O painel rápido na bandeja do Windows" width="70%">

</td>
</tr>
</table>

<sub>As capturas mostram o Rashnova com uma sessão de exemplo (uma usuária fictícia, "Riya").</sub>

<a name="never"></a>
## O que ele nunca registra

O Rashnova registra **que** algo aconteceu, não o que estava na tela. Ele não registra:

- teclas digitadas
- o conteúdo da área de transferência
- a sua tela, em imagens ou vídeo
- a sua câmera ou o seu microfone
- o conteúdo dos seus documentos, fotos, e-mails ou mensagens
- as páginas web que você visita, nem o que há nelas

Vale saber duas coisas que ele registra. Durante uma Repair session, os comandos do PowerShell são registrados ao
serem executados, assim como a linha de inicialização completa de cada programa que uma pessoa inicia; por isso, um
navegador aberto a partir de um link mostra esse link.

Um relatório diz, por exemplo, que `Bank_Statement_Aug2026.pdf` foi aberto de `Documents\Finance` pelo
Microsoft Edge às 15:01:16. Não diz o que havia no extrato.

<a name="how"></a>
## Como funciona

1. **Instale.** O Setup instala o Rashnova e o seu gravador em segundo plano.
2. **Defina um PIN.** O PIN é verificado pelo gravador, não pela janela do aplicativo.
3. **Antes de entregar:** **Repair Mode > Activate**, depois o seu PIN.
4. **Entregue.** Tudo em "O que ele faz" é gravado em um registro selado.
5. **Ao receber de volta:** **Deactivate**, depois o seu PIN. Você recebe um veredito, um relatório e a verificação da cadeia.

O gravador funciona como um serviço do Windows, então continua gravando quer alguém abra a janela do Rashnova ou
não, e volta a iniciar sozinho depois de uma reinicialização.

**Cada sessão termina com um de quatro vereditos:**

| Veredito | Significa |
| --- | --- |
| **Quiet** | O registro é verificado, está completo e nada de alta importância aconteceu. |
| **Notable** | Pelo menos um evento alto (high) ou crítico (critical): vale a leitura. |
| **Compromised** | O registro tem uma lacuna dentro da sessão (o computador estava desligado, suspenso ou reiniciando, ou a vigilância foi interrompida) ou mostra interferência, então não pode responder pela sessão inteira. |
| **Chain broken** | O registro não se verifica. Tudo continua sendo mostrado, marcado como não verificado. |

<a name="download"></a>
## Download e instalação

| Arquivo | Para quem |
| --- | --- |
| **`Rashnova-Setup-1.1.0.exe`** | Para todos. Instala primeiro o .NET 8 Desktop Runtime da Microsoft, se o seu PC não tiver, e depois o Rashnova. |
| `Rashnova-1.1.0.msi` | Para administradores que implantam com as próprias ferramentas. Exige o .NET 8 Desktop Runtime já instalado. |
| `SHA256SUMS.txt` | O SHA-256 de cada arquivo, para verificar o seu download. |

1. Baixe `Rashnova-Setup-1.1.0.exe` da [versão mais recente](https://github.com/sathvik-zoldyck/rashnova/releases/latest).
2. **Verifique o arquivo** (recomendado). No PowerShell:
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-Setup-1.1.0.exe"
   ```
   O hash deve ser exatamente igual ao de `SHA256SUMS.txt` e ao das notas de versão.
3. Execute-o. O Windows SmartScreen mostra **"Windows protected your PC"** com um editor desconhecido, porque o
   instalador ainda não tem assinatura digital (veja os [limites conhecidos](KNOWN_LIMITS.md)). Escolha
   **More info** e depois **Run anyway**.
4. Aceite os [termos de licença](https://www.alcyonesecure.com/terms), instale e abra o Rashnova.
5. Defina um PIN e escolha se mantém a gravação só em sessões (o padrão) ou se liga a gravação contínua.


> [!IMPORTANT]
> Um PIN esquecido não pode ser recuperado, nem por nós nem por ninguém. Anote-o em um lugar seguro.
> Desligar a gravação contínua nunca pede o PIN.


**Vem do BlackBox 1.0.1?** Rashnova é o novo nome do BlackBox. Baixe e instale o 1.1.0.

<a name="requirements"></a>
## Requisitos do sistema

- Windows 10 ou Windows 11, 64 bits (testado no Windows 10)
- Microsoft .NET 8 Desktop Runtime (o Setup instala se estiver faltando)
- Permissão de administrador para instalar, porque o gravador funciona como um serviço do Windows

<a name="privacy"></a>
## Privacidade

- **Só local.** O registro é gravado e guardado no seu computador. No 1.1.0 não há conta nem nuvem, e o Rashnova não
  envia dados de uso.
- **Duas pequenas solicitações,** nenhuma com nada do seu registro: uma verificação diária em alcyonesecure.com de uma
  versão nova e, durante uma Repair session, uma verificação da hora com o servidor de hora da Microsoft.
- **Quem pode ler o registro.** A conta do Windows que definiu o PIN e os administradores do computador. A segunda
  cópia é criptografada, e o Rashnova só a abre depois que o seu PIN é verificado. Os administradores do computador ainda
  podem lê-la.
- **Avise quem usa o seu PC.** A gravação contínua cobre o computador inteiro, inclusive pessoas que nunca abrem o
  Rashnova.
- **Uma configuração do Windows, dita com clareza.** Na primeira vez que a gravação é ligada, o Rashnova liga o registro
  de scripts do PowerShell do Windows e anota como a configuração estava antes. Nunca desliga uma configuração que outra
  pessoa ligou.

<a name="limits"></a>
## Limites conhecidos

Publicamos o que o Rashnova não faz, para que você decida com os fatos. O mais importante:

- **Nada pode ser registrado enquanto o computador está desligado, suspenso ou reiniciando.** A sessão continua, e o
  relatório mostra cada interrupção e a sua duração.
- **Administradores podem ler o registro.** Nenhum programa consegue esconder os seus arquivos de um administrador do Windows.
- **O instalador ainda não tem assinatura digital,** por isso o Windows SmartScreen avisa antes de executá-lo.
- **O bloqueio de armazenamento USB não está no 1.1.0.** Cada pendrive e cada arquivo copiado para ele é registrado;
  o bloqueio chega em uma atualização.

A lista completa, com o motivo de cada limite e o que está planejado (em inglês): **[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**.

<a name="updates"></a>
## Atualizações

Uma vez por dia o Rashnova verifica em alcyonesecure.com se há uma versão nova e avisa você. Você mesmo baixa e
instala; o seu registro, o seu PIN e as suas configurações são mantidos. Cada versão é publicada aqui com as suas notas e
o seu SHA-256. Veja o [histórico de alterações](CHANGELOG.md).

<a name="support"></a>
## Ajuda e segurança

- **Ajuda:** veja [SUPPORT.md](SUPPORT.md) ou escreva para **support@alcyonesecure.com**.
- **Bugs:** [abra um issue](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose). Nunca publique o seu
  registro, nomes de arquivos ou nada pessoal em um issue.
- **Vulnerabilidades de segurança:** não abra um issue público. Siga o [SECURITY.md](SECURITY.md).

<a name="licence"></a>
## Licença

O Rashnova é software proprietário, gratuito para uso em dispositivos que são seus ou que você está autorizado a
monitorar. Veja [LICENSE](LICENSE) e os [termos](https://www.alcyonesecure.com/terms) (em inglês; são eles que valem).
Os documentos e imagens deste repositório são © Alcyone Secure.

---

<div align="center">

<img src="assets/alcyone-owl.png" alt="Alcyone Secure" width="40">

**Alcyone Secure** · Feito em Bengaluru, Índia · [alcyonesecure.com](https://www.alcyonesecure.com)

*Segurança não é só prevenção. Segurança é responsabilidade.*

</div>

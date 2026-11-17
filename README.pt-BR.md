# Assembly Studio Desktop

**Planejamento de montagem de DNA, desenho de oligonucleotídeos e verificação de construções em um aplicativo local.**

Desenvolvido por Diego Bonatto · LBCM · Universidade Federal do Rio Grande do Sul (UFRGS).

[Baixar instaladores](https://github.com/bonattod/assembly-studio-desktop/releases/latest) · [English](README.md) · [Guia de instalação](LEIA-ME-Assembly-Studio-Desktop.txt)

## Downloads

**Apple Silicon / M1:** utilize o pacote macOS corrigido 1.14.1 e consulte o [guia específico de instalação](INSTALL-MACOS.pt-BR.md), que explica o aviso “Apple could not verify…” e a opção **Abrir Mesmo Assim**. Em 17/11/2026, o envio da versão 1.14.1 ao GitHub Releases ainda está pendente. Os pacotes macOS 1.14.0 permanecem no histórico da release e apresentaram um problema de assinatura. Windows e Linux continuam disponíveis na versão 1.14.0.

| Computador | Arquivo |
| --- | --- |
| Windows x64 | [Instalador .exe](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.0/Assembly-Studio-Desktop-1.14.0-win-x64.exe) |
| Linux Debian/Ubuntu x64 | [Pacote .deb](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.0/Assembly-Studio-Desktop-1.14.0-linux-amd64.deb) |
| Outras distribuições Linux compatíveis, x64 | [Arquivo .tar.gz](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.0/Assembly-Studio-Desktop-1.14.0-linux-x64.tar.gz) |
| Mac com Apple Silicon / M1 | DMG ARM64 1.14.1 — [instalação e disponibilidade](INSTALL-MACOS.pt-BR.md) |
| Mac com processador Intel | DMG x64 1.14.1 — publicação pendente; consulte as [notas da versão](RELEASE-NOTES-1.14.1.md) |

Não é necessário solicitar acesso à versão web para usar os instaladores publicados. Os arquivos **Source code** gerados automaticamente pelo GitHub contêm a documentação deste repositório de distribuição; escolha o pacote da sua plataforma conforme a disponibilidade indicada acima.

## Funcionalidades

O programa reúne técnicas de montagem **in vitro**, incluindo Gibson e TPA; montagem e edição de plasmídeos **in vivo**; e técnicas **Golden Gate/Tipo IIS**. Também inclui avaliação de vetores, análise de oligos nas duas fitas, exportações combinadas para síntese, consolidação de sequências idênticas, preservação de anotações, verificação por PCR/restrição e sequenciamento, montagem combinatória e exportação SnapGene.

A interface do aplicativo está em inglês. Os motores de cálculo e os componentes científicos estão incluídos: o usuário não precisa instalar Python ou Node.js. Consultas explícitas ao NEB e páginas externas exigem internet.

## Instalação e uso

Consulte o [guia geral](LEIA-ME-Assembly-Studio-Desktop.txt) ou o [passo a passo para Apple Silicon/M1](INSTALL-MACOS.pt-BR.md). Confira o SHA-256 correspondente: [Windows/Linux 1.14.0](SHA256SUMS-Assembly-Studio-Desktop-1.14.0.txt) ou [macOS 1.14.1](SHA256SUMS-Assembly-Studio-Desktop-1.14.1.txt).

Use **Open project** para abrir um projeto e **Save project** para salvar o arquivo `.assembly.json`, compatível com a versão web. **Não há salvamento automático.** As atualizações também são manuais.

O pacote macOS 1.14.1 possui assinatura ad hoc e continua sem assinatura Apple Developer ID ou notarização. Os testes nativos de inicialização em macOS passaram; a aprovação inicial em um Mac de usuário com instalação limpa continua sem verificação. O instalador Windows também não possui certificado do publicador. Os detalhes estão em [VALIDATION.md](VALIDATION.md).

As verificações computacionais não equivalem à validação experimental. Fidelidade de ligação, rendimento e proporção de clones corretos devem ser interpretados como medidas distintas.

A [versão web](https://assembly-studio-lbcm.diegobonatto.chatgpt.site) permanece disponível com suas permissões atuais. A distribuição pública desktop é independente desses acessos.

## Colaboração e citação

Relate problemas ou sugestões em [Issues](https://github.com/bonattod/assembly-studio-desktop/issues), informando versão, sistema operacional e passos para reproduzir. Prefira exemplos sintéticos mínimos, pois os relatos e anexos são públicos.

Citação sugerida: **Bonatto, D. (2026). Assembly Studio Desktop (Version 1.14.0) [Computer software]. LBCM, UFRGS. https://github.com/bonattod/assembly-studio-desktop**

Cite também os artigos das técnicas científicas utilizadas.

## Licença e contato

O código original do Assembly Studio e a documentação adotam a [licença MIT](LICENSE). Os componentes de terceiros mantêm suas próprias licenças e avisos. Consulte o [escopo da licença](THIRD_PARTY_NOTICES.md).

Este repositório público contém instaladores e documentação. O repositório de desenvolvimento permanece privado: adicionar a licença MIT não publica automaticamente o código-fonte.

Contato: [diego.bonatto@ufrgs.br](mailto:diego.bonatto@ufrgs.br).

# Instalação em Apple Silicon / M1

[English](INSTALL-MACOS.md) · [Página principal](README.pt-BR.md) · [Notas da versão](RELEASE-NOTES-1.14.1.md)

## Pacote e disponibilidade

Para o MacBook Air M1 ou outro Mac com Apple Silicon, use **`Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg`**. O pacote `mac-x64` é destinado aos Macs Intel.

Os instaladores corrigidos para macOS estão publicados na [release 1.14.1](https://github.com/bonattod/assembly-studio-desktop/releases/tag/v1.14.1). Os pacotes macOS 1.14.0 apresentaram um problema de assinatura; este guia se aplica à **1.14.1**. Windows e Linux permanecem na 1.14.0.

Baixe o [instalador para Apple Silicon / M1](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.1/Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg) ou, se o seu Mac tiver processador Intel, o [instalador para Intel](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.1/Assembly-Studio-Desktop-1.14.1-mac-x64.dmg). O ZIP “Source code” gerado automaticamente pelo GitHub não é um instalador. Para suporte, entre em contato com [diego.bonatto@ufrgs.br](mailto:diego.bonatto@ufrgs.br).

## Conferir e instalar o pacote M1

1. Salve os projetos abertos em JSON, preserve os arquivos dos seus projetos e feche a versão antiga do aplicativo.
2. Confira o DMG usando os [checksums da versão 1.14.1](SHA256SUMS-Assembly-Studio-Desktop-1.14.1.txt). No Terminal, dentro da pasta do download, execute:

   ```sh
   shasum -a 256 Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg
   ```

   SHA-256 esperado:

   ```text
   e508e3e3bab922617935fb90788acd0e0546c3c4fd3197eb5aadfcf78844157f
   ```

   A coincidência identifica os mesmos bytes do instalador conferido; não constitui análise de malware nem certificação Apple. Se houver diferença, obtenha uma nova cópia antes de instalar.
3. Abra o DMG e copie **Assembly Studio Desktop** para **Aplicativos**, substituindo a versão anterior quando solicitado.
4. Abra **Assembly Studio Desktop** a partir de **Aplicativos**.

## Aviso “Apple could not verify…”

O macOS pode exibir a seguinte mensagem:

> Apple could not verify “Assembly Studio Desktop” is free of malware that may harm your Mac or compromise your privacy.

A versão 1.14.1 usa **assinatura ad hoc** e ainda **não possui assinatura Apple Developer ID nem notarização Apple**. A correção do empacotamento mantém essa limitação. O aviso isolado não comprova que malware tenha sido detectado.

Depois de tentar abrir, prossiga apenas se confiar na origem e o checksum coincidir:

1. Acesse **Ajustes do Sistema → Privacidade e Segurança** (*System Settings → Privacy & Security*) e role até **Segurança**.
2. Localize **Assembly Studio Desktop** e clique em **Abrir Mesmo Assim** (*Open Anyway*).
3. Confirme em **Abrir** (*Open*) e autentique-se no próprio Mac, se solicitado.

A autorização vale para esse aplicativo. Mantenha o Gatekeeper ativado. Consulte as [instruções oficiais da Apple](https://support.apple.com/en-us/102445).

## Se o aplicativo continuar sem abrir

Se **Abrir Mesmo Assim** não aparecer, ou o aviso disser que o aplicativo está **danificado** ou **danificará o computador**, interrompa a tentativa e informe a mensagem exata, em vez de aplicar indiscriminadamente o procedimento acima. Inclua a versão do macOS em **menu Apple → Sobre Este Mac**, o processador, o nome do DMG e o resultado SHA-256. Não publique senhas nem dados pessoais dos projetos.

Envie o relato por [GitHub Issues](https://github.com/bonattod/assembly-studio-desktop/issues) ou pelo e-mail do mantenedor indicado acima.

Os testes nativos em Apple Silicon conferiram a integridade do DMG, as assinaturas, a inicialização e um exemplo sintético de montagem com leitura e gravação de projeto. A aprovação inicial pelo Gatekeeper em um Mac de usuário com instalação limpa continua sem verificação; consulte os [detalhes da validação](VALIDATION.md).

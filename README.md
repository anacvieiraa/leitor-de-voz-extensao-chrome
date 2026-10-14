# Leitor de Voz — extensão para Google Chrome

Lê em voz alta o texto da página (ou só o trecho selecionado), com escolha de **país/voz**,
**velocidade**, e continua lendo em **segundo plano** (pode trocar de aba, fechar o popup ou minimizar o Chrome).

## Instalação (modo desenvolvedor)

1. Descompacte o arquivo `leitor-de-voz.zip` em uma pasta que você NÃO vá apagar
   (ex.: `C:\Extensoes\leitor-de-voz` ou `~/Extensoes/leitor-de-voz`). O Chrome lê os arquivos dessa pasta.
2. No Chrome, abra `chrome://extensions` (digite na barra de endereços).
3. Ative **Modo do desenvolvedor** (canto superior direito).
4. Clique em **Carregar sem compactação** e selecione a pasta `leitor-de-voz` (a que contém o `manifest.json`).
5. Clique no ícone de quebra-cabeça 🧩 da barra do Chrome e no **alfinete 📌** ao lado de "Leitor de Voz" para fixá-lo.
6. (Opcional) Em `chrome://extensions/shortcuts` confira/altere os atalhos de teclado.

Para atualizar depois de mexer nos arquivos: em `chrome://extensions`, clique no botão ⟳ do cartão da extensão.

## Como usar

- Abra uma página, clique no ícone e aperte **▶**. Se houver texto selecionado, lê só a seleção; senão, lê o artigo da página.
- **Ler página / Ler seleção / Ler da tela** (a partir do que está visível no topo da janela).
- **Botão direito** → "Ler seleção em voz alta" / "Ler esta página em voz alta".
- **Alt+clique** (Option+clique no Mac) em qualquer trecho, durante a leitura, para continuar dali.
- **País/idioma**: "Automático" detecta o idioma da página; ou escolha fixo (Português — Brasil, Portugal, Inglês — Reino Unido, etc.).
- **Voz**: lista as vozes disponíveis para o país escolhido (a escolha é lembrada por país).
- **Velocidade** 0,5× a 3×, tom e volume; mudanças valem na hora, durante a leitura.
- **Parar sozinho em** X minutos (timer para dormir).
- **Avançado**: dicionário de pronúncia (`ONU=O nu`), tom, volume e atalhos.

## Atalhos padrão

| Atalho | Ação |
|---|---|
| Alt+Shift+P | Ler / pausar / retomar |
| Alt+Shift+S | Parar |
| Alt+Shift+→ | Próximo parágrafo |
| Alt+Shift+← | Parágrafo anterior |

## Vozes

A extensão usa as vozes do Chrome/sistema operacional. No Chrome desktop costumam existir as vozes "Google …"
(online, naturais, por país) além das do Windows/macOS. Para mais vozes: Windows → Configurações › Hora e idioma › Fala;
macOS → Ajustes › Acessibilidade › Conteúdo falado.

## Limitações

- Não funciona em páginas internas (`chrome://`), Chrome Web Store e no visualizador de PDF do Chrome.
- Lê o frame principal da página (não o conteúdo de iframes) e não entra em Shadow DOM.
- Vozes "Google" precisam de internet; algumas ignoram tom/volume.
- Se a página recarregar ou você fechar a aba, a leitura é encerrada.

## Privacidade

Tudo roda localmente. A extensão não envia dados a servidor nenhum e não tem acesso permanente a nenhum site
(só à aba em que você aciona a leitura — permissão `activeTab`). As configurações ficam no `chrome.storage.sync` da sua conta Chrome.
(Observação: as vozes "Google" online enviam o texto lido ao serviço de voz do Google, como qualquer síntese online do Chrome.)

# Tracer — mesa de luz

App web instalável (PWA), feito sem frameworks, Android Studio, emulador ou dependências. Funciona em Android e iPhone pelo navegador; usa a galeria/arquivos do próprio celular.

## Como usar no celular

1. Publique a pasta `tracer-app` em qualquer hospedagem estática com HTTPS (por exemplo, GitHub Pages, Netlify ou Cloudflare Pages).
2. Abra o endereço no navegador do celular e escolha **Adicionar à tela inicial** / **Instalar app**.
3. Abra o Tracer, toque em **Escolher imagem**, selecione seu desenho e ajuste com pinça, arraste ou os botões +/−.
4. Toque no cadeado para travar. O cabeçalho e os controles somem, a imagem se ajusta ao espaço total da tela e um pequeno cadeado no canto inferior permite destravar.

Depois da primeira abertura, o app pode carregar offline. A busca de imagens precisa de internet. O bloqueio impede os gestos na imagem e tenta manter a tela ligada (suportado por navegadores compatíveis). Para maior praticidade, deixe o brilho do telefone no nível desejado antes de travar.

## Rodar com Node.js

Se Node.js estiver instalado, abra o terminal nesta pasta e execute:

```powershell
node server.js
```

No computador, acesse `http://localhost:8080`. Para abrir no celular, conecte-o à mesma rede Wi-Fi e acesse `http://IP-DO-PC:8080` (o IP local do PC pode ser consultado com `ipconfig`). Se o Windows perguntar, permita o acesso na rede privada.

O Node.js serve o app sem dependências adicionais. No endereço HTTP da rede local, os recursos básicos funcionam; porém, instalação como PWA, cache offline e manter a tela ligada podem exigir HTTPS no celular. Para isso, publique a pasta em uma hospedagem estática com HTTPS. Não é necessário instalar Android Studio nem compilar APK.

## Recursos

- Seleção de imagens da galeria/arquivos, sem enviar fotos para servidor.
- Zoom por pinça e controles, arraste para reposicionar, rotação livre com gesto de pinça/torção e botões de giro.
- Filtro local de contorno para transformar fotos em um desenho simplificado; toque no ícone ✧ para ativar/desativar.
- Busca integrada no Wikimedia Commons: toque numa imagem para abri-la direto no Tracer, sem baixar. A busca precisa de internet e apresenta imagens com licenças livres.
- Trava de interação e tentativa de manter a tela ativa.
- PWA instalável e cache offline.

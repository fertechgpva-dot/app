# Gestão FERTECH (versão desktop)

Sistema de gestão (clientes, pedidos, estoque, serviços, agenda, financeiro e etiquetas 5x3 cm) empacotado como programa para Windows com Electron.

## Gerar o instalador .exe pelo GitHub (sem instalar nada no seu PC)
1. Crie um repositório no GitHub e envie todos os arquivos desta pasta (incluindo a pasta `.github`).
2. Abra a aba **Actions** do repositório. O workflow "Gerar instalador Windows" roda sozinho a cada envio para a branch `main`. Para rodar na hora, use **Run workflow**.
3. Quando terminar (alguns minutos), abra a execução e baixe o arquivo **instalador-windows** na seção *Artifacts*. Dentro dele está o `.exe`.
4. Para publicar uma versão fixa, crie uma tag, por exemplo `v1.0.0`. O instalador aparece na aba **Releases**.

## Gerar no seu computador (opcional)
Precisa do Node.js 20 ou superior:
```
npm install
npm run dist
```
O instalador sai na pasta `dist/`. Para só testar a janela: `npm start`.

## Onde ficam os dados
Os dados ficam salvos no computador onde o programa está instalado (armazenamento local do aplicativo). Desinstalar ou apagar os dados do aplicativo remove os cadastros. Use **Conta > Baixar backup dos dados** com frequência.

## Ícone próprio
Coloque um arquivo `icon.ico` (256x256) em uma pasta `build/` e rode o build de novo.

## Observação
O Windows pode exibir o aviso do SmartScreen ao instalar, porque o instalador não é assinado digitalmente. Clique em "Mais informações" e depois em "Executar assim mesmo".

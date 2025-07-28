# 📱 WhatsApp Version Fix Tool

Uma ferramenta simples para corrigir problemas de versão do WhatsApp no Whaticket, ajudando a manter a compatibilidade e evitar bloqueios.

## 🚀 Como Usar

### 1. Instalação

1. **Baixe o arquivo `fix-version.js`**
2. **Coloque o arquivo na pasta `/backend` do seu projeto Whaticket**

```
seu-projeto/
├── frontend/
├── backend/          ← Coloque o fix-version.js aqui
│   ├── src/
│   ├── fix-version.js ← Arquivo deve ficar aqui
│   └── ...
└── ...
```

### 2. Executando o Fix

Abra o terminal na pasta `/backend` e execute:

```bash
node fix-version.js latest
```

## 📋 Comandos Disponíveis

### Aplicar versão mais recente (recomendado)
```bash
node fix-version.js latest
```

### Ver versão atual
```bash
node fix-version.js --current
```

### Aplicar versão customizada
```bash
node fix-version.js 2 3000 1025200398
```

## 🔍 Como Encontrar Versões Funcionais

Para encontrar versões do WhatsApp que estão funcionando:

1. **Visite o site oficial:** https://wppconnect.io/pt-BR/whatsapp-versions/

2. **Você verá uma lista como esta:**
   ```
   Todas as Versões do WhatsApp
   
   2.3000.1025200398-alpha estável atual
   Lançado em 28/07/2025, 12:25:17 AM, expira em 28/09/2025, 12:25:17 AM
   
   2.3000.1025190524-alpha estável
   Lançado em 26/07/2025, 7:43:09 PM, expira em 26/09/2025, 7:43:09 PM
   ```

3. **Como extrair a versão:**
   
   Da versão `2.3000.1025200398-alpha`, você precisa extrair os números:
   - **Major:** `2`
   - **Minor:** `3000` 
   - **Patch:** `1025200398`

4. **Para aplicar essa versão:**
   ```bash
   node fix-version.js 2 3000 1025200398
   ```

## 📝 Exemplo Prático Passo a Passo

### Cenário: Seu WhatsApp parou de funcionar

1. **Vá para a pasta backend:**
   ```bash
   cd /caminho/para/seu/projeto/backend
   ```

2. **Verifique a versão atual:**
   ```bash
   node fix-version.js --current
   ```
   
   Resultado:
   ```
   📱 Versão atual: [2, 2413, 1]
   ```

3. **Visite:** https://wppconnect.io/pt-BR/whatsapp-versions/

4. **Escolha uma versão estável (exemplo: `2.3000.1025200398-alpha`)**

5. **Aplique a nova versão:**
   ```bash
   node fix-version.js 2 3000 1025200398
   ```
   
   Resultado:
   ```
   🔄 Usando versão customizada: [2, 3000, 1025200398]
   📱 Versão atual: [2, 2413, 1]
   ✅ Versão atualizada com sucesso para: [2, 3000, 1025200398]
   
   💡 Dicas:
     - Reinicie o servidor para aplicar as mudanças
     - Teste a conexão após a mudança
     - Se houver problemas, use uma versão mais estável
   ```

6. **Reinicie seu servidor Whaticket**

## ⚠️ Dicas Importantes

### ✅ Faça Sempre
- ✅ Use versões marcadas como **"estável"**
- ✅ Verifique se a versão não está expirada
- ✅ Reinicie o servidor após aplicar a correção
- ✅ Teste a conexão depois da mudança
- ✅ Mantenha um backup do arquivo original

### ❌ Evite
- ❌ Usar versões muito antigas
- ❌ Usar versões que estão prestes a expirar
- ❌ Aplicar múltiplas mudanças rapidamente
- ❌ Esquecer de reiniciar o servidor

## 🐛 Solução de Problemas

### Erro: "Arquivo wbot.ts não encontrado"
```bash
❌ Arquivo wbot.ts não encontrado em: /caminho/src/libs/wbot.ts
   Certifique-se de estar executando o script na pasta /backend do projeto.
```

**Solução:** Certifique-se de que:
1. Está executando o comando na pasta `/backend`
2. O arquivo `wbot.ts` existe em `backend/src/libs/wbot.ts`
3. A estrutura do projeto está correta

### WhatsApp ainda não conecta após a mudança
1. **Tente uma versão diferente** do site wppconnect.io
2. **Aguarde alguns minutos** antes de testar
3. **Reinicie completamente** o servidor
4. **Limpe o cache** do navegador
5. **Verifique os logs** do servidor para outros erros

### Versão não aceita pelo WhatsApp
1. **Use uma versão mais recente** do site
2. **Evite versões muito antigas** (mais de 2 meses)
3. **Prefira versões marcadas como "estável atual"**

## 📞 Suporte

Se você continuar tendo problemas:

1. **Verifique o site oficial:** https://wppconnect.io/pt-BR/whatsapp-versions/
2. **Use sempre versões marcadas como estáveis**
3. **Aguarde lançamento de novas versões** se todas estiverem com problema

## 🔄 Atualizações Automáticas

O arquivo já vem com a versão mais recente configurada como `latest`. Para facilitar o uso futuro:

```bash
# Sempre use este comando para aplicar a versão mais atual
node fix-version.js latest
```

---

**⭐ Dica Pro:** Salve este README e o arquivo `fix-version.js` em um local seguro para usar sempre que precisar! 🚀
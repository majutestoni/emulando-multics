# 💻 Emulando o Multics

Este guia descreve o processo para instalar e executar o sistema operacional **Multics** utilizando o simulador **DPS8M**.

---

## 🧩 1. Instalar o Simulador

O **DPS8M** é um simulador open source dos computadores mainframe de 36 bits da série **GE Large Systems / Honeywell / Bull 600/6000**, como os modelos *Honeywell 6180*, *Series-60/Level-68* e *DPS-8/M*.  
Esses sistemas são descendentes do **GE-645**, projetado originalmente para suportar o **Multics (Multiplexed Information and Computing Service)**.

> 🔗 **Site oficial do DPS8M:**  
> [https://dps8m.gitlab.io/dps8m/Releases/](https://dps8m.gitlab.io/dps8m/Releases/)

**Passos:**
1. Acesse o link acima e baixe a versão correspondente ao seu sistema operacional (por exemplo, *Windows*).  
2. Consulte também a página do Multics Wiki para obter detalhes sobre a versão **MR12.8**:  
   [https://multics-wiki.swenson.org/index.php/MR12.8#Release_Artifacts](https://multics-wiki.swenson.org/index.php/MR12.8#Release_Artifacts)

---

## 📀 2. Obter os Arquivos Bootáveis

Para inicializar o Multics, são necessários os arquivos bootáveis oficiais.

**Acesse:**  
[https://multics-wiki.swenson.org/index.php/MR12.8#Release_Artifacts](https://multics-wiki.swenson.org/index.php/MR12.8#Release_Artifacts)

Em seguida, localize e siga as instruções da seção **MR12.8 QuickStart**  
ou, alternativamente, **Installing MR12.8 as a New System (QuickStart)**.

---

## ⚙️ 3. Configuração do Ambiente

1. Crie uma pasta na raiz do seu disco, chamada `multics`.  
2. Extraia o conteúdo do pacote do Multics dentro dessa pasta.  
3. Copie também os arquivos do simulador **DPS8M** para a mesma pasta.  
4. Abra o arquivo `MR12.8_boot.ini` e adicione a seguinte linha ao final:

   ```ini
   attach fnp g.000 telnet=localhost:6180

## ▶️ 4. Executando o Multics

1. Abra um terminal e navegue até a pasta `multics`.  
2. Execute o simulador com o comando:

   ```bash
   .\dps8 MR12.8_boot.ini
   
3. Abra uma nova aba ou janela do terminal.
4. Conecte-se ao sistema via Telnet:
      ```bash
   telnet localhost 6180


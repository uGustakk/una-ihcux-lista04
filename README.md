## ⚠️ Tratamento de Erros com try-catch

Em C#, o bloco `try-catch` é utilizado para **capturar e tratar exceções** (erros) que podem ocorrer durante a execução do programa.

### 🧠 Como funciona

* `try`: contém o código que pode gerar um erro
* `catch`: captura o erro e define como o sistema deve reagir
* `finally` (opcional): executa sempre, independentemente de erro ou não

### 💡 Exemplo simples

```csharp
try
{
    int numero = int.Parse("abc"); // gera erro
}
catch (FormatException)
{
    Console.WriteLine("Erro: valor inválido.");
}
```

---

## 🎯 Relação com a Heurística: Prevenção de Erros

A heurística de **Prevenção de Erros** (de Nielsen) diz que:

> O sistema deve evitar que erros aconteçam ou, quando inevitáveis, tratá-los de forma adequada.

### 🔗 Conexão com o projeto

O uso de `try-catch` contribui diretamente para essa heurística porque:

* 🛑 **Evita falhas inesperadas** (como o programa travar)
* 💬 **Fornece mensagens claras ao usuário**
* 🔄 **Permite que o sistema continue funcionando**, mesmo após um erro
* 🧭 **Guia o usuário para corrigir o problema**

### ✅ Exemplo aplicado ao ScannerExpert

Caso alguma etapa do “scan” falhe (ex: erro ao acessar memória), o sistema pode:

* Capturar o erro com `catch`
* Exibir uma mensagem amigável
* Continuar ou encerrar de forma controlada

---

## 🧩 Conclusão

O `try-catch` é uma ferramenta essencial para criar sistemas mais **robustos e confiáveis**, alinhando-se diretamente com a heurística de **Prevenção de Erros**, ao minimizar impactos negativos e melhorar a experiência do usuário.

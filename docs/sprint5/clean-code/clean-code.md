
# Clean code

Clean code é um conjunto de práticas e princípios de desenvolvimento de software que visam criar código claro, legível e fácil de manter. Um código considerado "limpo" é aquele que, além de funcionar corretamente, é escrito de forma que outros desenvolvedores possam entendê-lo facilmente, fazendo com que a manutenção e a evolução do software sejam mais simples e menos propensas a erros. Entre os princípios de clean code estão a escolha de nomes descritivos para variáveis, funções e classes, a redução da complexidade, a modularização do código em funções pequenas e específicas, e a eliminação de duplicações. 
No contexto da tarefa, sugerimos mudanças baseadas nesses princípios para melhorar a clareza e a qualidade do código, tornando-o mais intuitivo e de fácil compreensão para qualquer desenvolvedor que precise trabalhar com ele no futuro.

## OWASP
### Bruno
### Igor 
## MEC-ENERGIA API
### Leonardo

### Mylena
Para essa atividade, foi utilizado o código do projeto [mec-energia-api](https://gitlab.com/lappis-unb/projetos-energia/mec-energia/mec-energia-api). Realizei uma análise utilizando a ferramenta `Code Climate` e, a partir dos resultados obtidos, decidi quais aspectos seriam abordados para refatoração. A sugestão de melhoria foi implementada no código do arquivo `utils/energy_bill_util.py`, no qual a  complexidade cognitiva  seguindo os princípios de _Clean Code_

![Sugestão Clean Code](code-climate-mylena.png)

## Refatoração proposta
 

        class EnergyBillValidator:
      
     @staticmethod
     def is_valid_consumption(consumption, measured_demand):
     return consumption > 0 and measured_demand > 0
     @classmethod
     def check_valid_consumption_demand(cls, energy_bill): 
     off_peak_consumption = energy_bill.off_peak_consumption_in_kwh
     off_peak_measured_demand  = energy_bill.off_peak_measured_demand_in_kw
     peak_consumption = energy_bill.peak_consumption_in_kwh
     peak_measured_demand = energy_bill.peak_measured_demand_in_kw
      
     ## retomar essa lógica quando retirar valores zerados do seed
     off_peak_valid = cls.is_valid_consumption(
     energy_bill.off_peak_consumption_in_kwh, 
     energy_bill.off_peak_measured_demand_in_kw
     )
     peak_valid = cls.is_valid_consumption(
     energy_bill.peak_consumption_in_kwh, 
     energy_bill.peak_measured_demand_in_kw
     )
     ## retomar essa lógica quando retirar valores zerados do seed
     return True
      
     if (off_peak_consumption and off_peak_consumption == 0) or (off_peak_measured_demand and off_peak_consumption == 0) or (peak_consumption and  peak_consumption == 0) or (peak_measured_demand and peak_measured_demand == 0):
     return False
     return True
     return True

### Justificativas


#### 1. ****Modularização e Clareza**:**

-   **Modularidade**: A lógica de validação foi extraída para um método estático separado (`is_valid_consumption`), que encapsula a verificação se o consumo e a demanda medida são válidos. Isso melhora a clareza e a reutilização do código.
-   **Clareza**: A nova implementação é mais direta ao verificar a validade dos consumos e demandas. Usar o método `is_valid_consumption` melhora a legibilidade e reduz a complexidade cognitiva, alinhando-se ao princípio de clareza do Clean Code.


####  2. **Redução da Complexidade Cognitiva**

**Simplicidade**: A versão original da função possui múltiplas condições e verificações que aumentam a complexidade cognitiva. A nova versão simplifica a lógica ao utilizar o resultado das verificações feitas pelo método `is_valid_consumption`, reduzindo a complexidade cognitiva e tornando o código mais fácil de entender e manter.


## MR
No meu repositório, o pipeline falhou após eu adicionar um novo código, pois a parte de testes não funcionou devido às mudanças que fiz. Foram mais de cinco arquivos que precisavam ser alterados para corrigir os problemas. No entanto, uma [issue](https://gitlab.com/lappis-unb/projetos-energia/mec-energia/mec-energia-api/-/issues/199) foi criada com uma sugestão de refatoração, incluindo trechos de código para melhorar a implementação.

![Erro Pipeline](pipeline-mylena.png)
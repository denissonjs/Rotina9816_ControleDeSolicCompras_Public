# Rotina9816_ControleDeSolicCompras_Public

# Sumário
- [Descrição do Projeto](#descrição-do-projeto)
    - [Objetivo do Projeto](#objetivo-do-sistema)
    - [Funcionalidades](#funcionalidades-principais)
    - [Flexibilidade](#flexibilidade-do-sistema)
    - [Befefícios Esperados](#benefícios-do-sistema)
    - [Resumo](#em-resumo)
- [Requisitos do Sistema](#requisitos-do-sistema)
    - [Usuário](#usuário)
    - [Desenvolvedor](#desenvolvedor)
- [Detalhes Técnicos](#detalhes-técnicos)
    - [Arquitetura](#arquiterura)
    - [Controle de Versões](#controle-de-versões)
- [Instruções de Instalação](#instruções-de-instalação)

# Descrição do Projeto
## Objetivo do Sistema
O objetivo principal deste sistema é simplificar e agilizar o processo de compra de itens, garantindo que todas as solicitações sejam adequadamente revisadas e autorizadas por pessoal autorizado. Além disso, o sistema permitirá rastrear a documentação relacionada a cada compra, garantindo a conformidade fiscal e a exatidão do pedido em relação à entrega.

## Funcionalidades Principais
O sistema terá as seguintes funcionalidades principais:
1.	Solicitação de Compras: Os usuários terão a capacidade de criar solicitações de compras de vários tipos de itens por meio do sistema. Eles especificarão os detalhes da compra, como quantidade, descrição, categoria, e outros dados relevantes.
2.	Gerenciamento de Alçadas de Autorizações: O sistema implementará um processo de autorização em várias etapas. O usuário solicitante será o aprovador de nível 1. O gestor do solicitante será o aprovador de nível 2. Após a aprovação do nível 2, a solicitação será encaminhada ao comprador, que realizará a cotação. Após a cotação, a solicitação será enviada ao gerente geral para a última aprovação. Em casos excepcionais, a solicitação pode ser encaminhada ao nível 4, que é o diretor da empresa. Esses níveis de autorização são parametrizáveis, permitindo a adição ou redução de níveis, conforme necessário.
3.	Parametrização de Valores Autorizáveis: O sistema permitirá que a organização configure os valores máximos que cada nível de autorização pode aprovar. Isso garante que compras de maior valor sejam aprovadas por níveis apropriados de autoridade.
4.	Anexação de Documentação: Após a conclusão das autorizações e a realização da compra, o sistema permitirá que os usuários anexem documentos fiscais, recibos e outros comprovantes relacionados à compra. Isso facilita a conformidade fiscal e a auditoria.

## Flexibilidade do Sistema
Este sistema foi projetado com a flexibilidade em mente. Os níveis de autorização podem ser ajustados conforme necessário, permitindo que a empresa se adapte às suas próprias políticas internas de compras. Além disso, os valores autorizáveis podem ser facilmente configurados, garantindo que o processo seja ajustado para acomodar compras de diferentes valores.

## Benefícios do Sistema
A implementação deste sistema trará diversos benefícios para a organização:
- Eficiência: O processo de compra será mais rápido e eficiente, reduzindo a burocracia.
- Transparência: O sistema oferece total visibilidade sobre o status de cada solicitação de compra, facilitando o acompanhamento.
- Conformidade Fiscal: O sistema ajuda a garantir que todas as compras estejam em conformidade com as leis fiscais.
- Controle de Despesas: O controle rigoroso dos valores autorizáveis ajuda a manter o controle de despesas.
- Auditoria Simplificada: A documentação anexada facilita a auditoria de compras.

## Em resumo
O sistema de Solicitação e Autorização de Compras proposto tem o objetivo de otimizar o processo de compra de materiais de escritório, suprimentos, peças veiculares, serviços e outros. Sua flexibilidade e capacidade de adaptação às necessidades da organização garantem que as políticas internas sejam respeitadas, ao mesmo tempo em que simplificam e agilizam o processo. A implementação desse sistema trará benefícios significativos em termos de eficiência, transparência, conformidade fiscal, controle de despesas e auditoria.

# Requisitos do Sistema
## Usuário
### Requisitos Hardware
- Processador: Processador dual-core de 2,0 GHz ou superior.
- Memória RAM: Mínimo de 4 GB de RAM.
- Espaço em Disco: Não aplicável.
- Resolução de Tela: Recomendada resolução mínima de 1280x800 pixels.
### Requisitos de Software
- Sistema Operacional: Windows 10 (64 bits) ou posterior.
- Banco de dados: Oracle 12C ou superior.

## Desenvolvedor
### Requisitos de Software
- Sistema Operacional: Windows 10 (64 bits) ou posterior.
- Framework: Microsoft .NET Framework 4.8 ou superior.
- Banco de dados: Oracle 12C ou superior.
- Ambiente de Desenvolvimento: Visual Studio 2022 ou superior.

### Requisitos Hardware
- Processador: Processador dual-core de 2,0 GHz ou superior.
- Memória RAM: Mínimo de 8 GB de RAM.
- Espaço em Disco: Entre 10MB e 50MB disponível.
- Resolução de Tela: Recomendada resolução mínima de 1280x800 pixels.

### Dependências Externas (de projeto)
- Biblioteca de Banco de dados: Oracle.ManagedDataAccess
    - A biblioteca `Oracle Data Access` usada em projetos anteriores não será mais utilizado. O pacote se tornou obsoleto, sem mais suporte e assim não recomendado pela IDE utilizada no projeto.
- Biblioteca de exportação de arquivo: EPPlus
    - Parte dos usuários não possuem os Microsoft Office instalado por utilizarem versão web, por esse motivo o pacote `Microsoft.Office.Interop.Excel` usado em projetos anteriores não será mais utilizado. Arquivos do tipo XSLS serão exportados permitindo a abertura em qualquer ferramenta de office sendo microsoft ou não.

- Instalação: Projeto - Gerenciar pacotes do nuget - Buscar e instalar o pacote.

# Detalhes Técnicos

## Arquiterura
Este projeto utiliza a arquitetura MVC (Model-View-Controller) para organizar e estruturar o código-fonte da aplicação Windows Form .NET. A escolha dessa arquitetura se baseia na simplicidade e direcionamento claro das responsabilidades, adequando-se às necessidades do projeto sem necessidades de arquiteturas mais robustas como a Clean Architecture.

### Sobre a Arquitetura MVC
O padrão MVC é amplamente utilizado no desenvolvimento de software e oferece uma divisão clara das responsabilidades em três componentes principais: Model, Views e Controllers. O vídeo [Entenda AGORA o PADRÃO Arquitetural MVC](https://www.youtube.com/watch?v=9Ieh0yoiiqI&pp=ygUSYXJxdWl0ZXR1cmEgbXZjIGMj) fornece mais detalhes sobre essa arquitetura.
### Vantagens da Arquitetura MVC para o Projeto
A escolha da arquitetura MVC para este projeto tem como objetivo aproveitar as seguintes vantagens:

- Separação de Responsabilidades:
A arquitetura MVC permite uma clara separação de responsabilidades entre as camadas do projeto. O Model se concentra na lógica de negócios e nos dados, a View na interface do usuário e a interação com o usuário, e o Controller na coordenação das ações entre o Model e a View. Isso torna o código mais organizado e facilita a manutenção e evolução do projeto.

- Facilidade de Testes:
A separação das responsabilidades na arquitetura MVC facilita a realização de testes unitários e automatizados. O Model, por exemplo, pode ser testado independentemente da View e do Controller, permitindo uma validação mais precisa da lógica de negócios.

- Reutilização de Componentes:
A arquitetura MVC incentiva a reutilização de componentes em diferentes partes do projeto. Por exemplo, a mesma View pode ser usada com diferentes Controllers para atender a diferentes requisitos ou fluxos de trabalho, sem a necessidade de reescrever o código.

Alguns exemplos da implementação deste modelo podem ser encontrados no vídeo [Projeto .NET: Aprenda as melhores práticas de arquitetura em 2023](https://youtu.be/jkPqczgDIZU).
### Conclusão

A arquitetura MVC oferece uma abordagem clara e estruturada para o desenvolvimento do projeto Windows Form .NET. Com a separação de responsabilidades e a facilidade de manutenção e teste, é possível desenvolver uma aplicação bem estruturada, escalável e de fácil evolução.

Este projeto busca tirar proveito dessas vantagens e oferecer uma experiência de desenvolvimento mais organizada e eficiente. Para mais informações sobre a arquitetura MVC, consulte a documentação fornecida e aproveite os recursos e exemplos disponíveis para ajudá-lo a criar uma aplicação de qualidade.

## Controle de Versões
Para transparência em nossos ciclos de lançamento e para manter a compatibilidade com versões anteriores, a aplicação será mantida sob [as diretrizes de Controle de Versão Semântico](https://semver.org/) armazenados e disponíveis no arquivo de [Releases](https://github.com/denissonjs/Rotina9817_AnaliseDeCredito/blob/main/changelog.md) deste repositório. 

# Instruções de instalação
A rotina estará disponível em arquivo executável (.exe) e gerenciada através do ERP da empresa, ou seja, em ambiente winthor. Sendo assim, a instalação partirá da equipe de análise de sistemas do ERP, não sendo necessárias nessa documentação, instruções sobre instalação do software.

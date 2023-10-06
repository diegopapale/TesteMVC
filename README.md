# TesteMVC
# Script para criação das tabelas no banco de dados SQL Server

CREATE TABLE Categoria
(
    Id INT PRIMARY KEY IDENTITY(1,1), 
    Descricao NVARCHAR(255) NOT NULL
);

CREATE TABLE Produto
(
    Id INT PRIMARY KEY IDENTITY(1,1),
    Descricao NVARCHAR(255),
    Quantidade INT CHECK (Quantidade BETWEEN 1 AND 10),
    CategoriaId INT FOREIGN KEY REFERENCES Categoria(Id),
    -- Outros campos podem ser adicionados aqui, conforme necessário
);

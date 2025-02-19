CREATE TABLE hotel.quarto_hospede (
    cpf_pk VARCHAR(11) PRIMARY KEY, 
    nome VARCHAR(40) NOT NULL,
    nascimento DATE NOT NULL,
    email VARCHAR(50),
    telefone VARCHAR(12) NOT NULL,
    cidade VARCHAR(20) NOT NULL,
    bairro VARCHAR(20) NOT NULL,
    rua VARCHAR(20),
    n_residencia INTEGER NOT NULL,
    n_quarto INTEGER,
    bloco VARCHAR(2) 
);


CREATE TABLE hotel.servico (
    id_servico_pk INTEGER PRIMARY KEY,
    horario_servico TIME,
    nomer_servico VARCHAR (25)
);

CREATE TABLE hotel.pagamento(
    id_pagamento_pk INTEGER PRIMARY KEY,
    h_baixa TIME,
    valor NUMERIC
);

CREATE TABLE hotel.funcionario (
    id_funcionario_pk INTEGER PRIMARY KEY,
    f_nome VARCHAR(40),
	id_servico_fk INTEGER NOT NULL,
	id_pagamento_fk INTEGER NOT NULL,

    FOREIGN KEY (id_servico_fk) REFERENCES hotel.servico (id_servico_pk),
    FOREIGN KEY (id_pagamento_fk) REFERENCES hotel.pagamento (id_pagamento_pk)
);

CREATE TABLE hotel.qh_servico(
    cpf_fk VARCHAR(11) NOT NULL,
    id_servico_fk INTEGER NOT NULL,

    FOREIGN KEY (cpf_fk) REFERENCES hotel.quarto_hospede (cpf_pk),
    FOREIGN KEY (id_servico_fk) REFERENCES hotel.servico (id_servico_pk)
);

CREATE TABLE hotel.qh_pagamento(
    cpf_fk VARCHAR(11) NOT NULL,
    id_pagamento_fk INTEGER NOT NULL,

    FOREIGN KEY (cpf_fk) REFERENCES hotel.quarto_hospede (cpf_pk),
    FOREIGN KEY (id_pagamento_fk) REFERENCES hotel.pagamento (id_pagamento_pk)
);
--DROP TABLE hotel; 
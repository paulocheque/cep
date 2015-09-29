=================================
 CEP
=================================

Esta biblioteca acessa o site dos Correios para fazer pesquisa por CEP.

INSTALAÇÃO
==========

::

    pip install cep

USO
===

::

    >>> from cep import Correios
    >>> c = Correios()
    >>> resultados = c.consulta('Juarez')
    >>> len(resultados)
    100
    >>> resultados[64]
    {'Localidade': u'Jo\xe3o Pessoa', 'Bairro': u'Torre', 'UF': u'PB', 'Logradouro': u'Avenida Juarez T\xe1vora - de 1147/1148 a 1911/', 'CEP': u'58040-021'}
    >>> c.detalhe(64)
    {'Localidade': u'Jo\xe3o Pessoa', 'Bairro': u'Torre', 'UF': u'PB', 'Logradouro': u'Avenida Juarez T\xe1vora - de 1147/1148 a 1911/1912', 'CEP': u'58040-021'}
    >>> c.consulta('91370000', primeiro=True)
    {'Localidade': u'Porto Alegre', 'Bairro': u'Vila Ipiranga', 'UF': u'RS', 'Logradouro': u'Rua Alberto Silva - at\xe9 965/966', 'CEP': u'91370-000'}


REQUIREMENTS
============

* BeautifulSoup4

LICENSE
=======

* MIT License

TODO
====

* Documentação
* Hospedar API pública (json/xml)

# CBL-Challenger
Aplicativo de Canais de comunicação e acesso de contato imediato


# Projeto "Alô Direto" 
Nosso projeto é uma plataforma que permite o acesso rápido e fácil a contatos essenciais de serviços públicos e autoridades locais, como SAMU, hospitais e assistência social, organizados por cidade e tipo de serviço. Com uma interface intuitiva, a aplicação visa minimizar o tempo de busca em situações de urgência, proporcionando apoio imediato e eficiente em momentos críticos.

# Links:
https://docs.google.com/document/d/1-JVgYfth44af2qD2Wx6k09hJmct85BFfhvEIwsobdEU/edit?usp=sharing
https://www.figma.com/board/zGIbD8Wx9ypxagr0OVDG5u/CBL?node-id=0-1&t=1AZe73he3b5HMfLq-1
https://docs.google.com/document/d/1V9F_EfP2oG39dEJFlG3xkp7q3pqYW5jw_bESO3U-0NU/edit?usp=sharing

# Código:
#!/bin/bash

echo "CBL Challenger - Sistema de Contatos de Emergência"

#Simula o aplicativo abrindo rapidamente
echo "Carregando aplicativo..."

#Manter localização ligada
echo "Deseja manter a localização ligada? (Sim/Não)"
read location

if [ "$location" == "Sim" ]; then
    echo "Localização ativada. Obtendo contatos de emergência baseados na sua localização..."
else
    echo "Insira o CEP da sua cidade/distrito:"
    read cep
    echo "Obtendo contatos de emergência para o CEP $cep..."
fi

#Mostrar opções de busca ou contatos automáticos
echo "Contatos de emergência obtidos:"
echo "1. Polícia"
echo "2. SAMU"
echo "3. Bombeiros"
echo "4. Assistência Social"
echo "Ou insira o nome do serviço desejado:"
read service

if [ -n "$service" ]; then
    echo "Procurando pelo serviço \"$service\"..."
    # Simula resultado da busca
    echo "Encontrado: $service"
else
    echo "Selecione o contato de emergência desejado (Digite o número correspondente):"
    read choice
    case $choice in
        1) service="Polícia";;
        2) service="SAMU";;
        3) service="Bombeiros";;
        4) service="Assistência Social";;
        *) echo "Opção inválida"; exit;;
    esac
fi

#Visualizar ou ligar
echo "Você selecionou: $service"
echo "Deseja visualizar o número ou ligar diretamente? (Visualizar/Ligar)"
read action

if [ "$action" == "Visualizar" ]; then
    echo "Número do $service: (xx) xxxxx-xxxx"
else
    echo "Ligando para $service diretamente do app..."
    # Simula uma chamada
    echo "Chamada em andamento..."
fi

Funcionalidades de Gestão de Contatos:
Armazenamento de Contatos:
Salvar uma lista de contatos de emergência, organizados por categoria (polícia, bombeiros, SAMU, etc.).
Pesquisa de Contatos:
Permitir pesquisa por nome ou serviço.
Visualização e Ligações:
Exibir informações do contato e oferecer a opção de ligar diretamente (simulado no CLI).


echo "Fim."


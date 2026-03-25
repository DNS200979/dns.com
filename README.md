<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ACS Platforms Strategic Analysis</title>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'IBM Plex Sans', sans-serif;
            background-color: #f4f7f6;
            color: #333;
            line-height: 1.6;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Language Toggle Styles */
        .lang-switch-container {
            text-align: right;
            margin-bottom: 10px;
        }
        .lang-switch-container button {
            background-color: #fff;
            border: 1px solid #ccc;
            padding: 5px 15px;
            cursor: pointer;
            border-radius: 4px;
            font-weight: 600;
            color: #333;
            transition: 0.3s;
            margin-left: 5px;
        }
        .lang-switch-container button.active-lang {
            background-color: #003366;
            color: white;
            border-color: #003366;
        }

        /* Language Display Logic - BULLETPROOF */
        .lang-pt { display: none !important; }
        body.pt-active .lang-en { display: none !important; }
        body.pt-active .lang-pt { display: inline !important; }

        /* Header Styles */
        .header {
            background-color: #003366;
            color: white;
            padding: 15px 20px;
            border-radius: 8px 8px 0 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .header-left {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .header-left img {
            max-height: 45px;
            background: white;
            padding: 5px;
            border-radius: 4px;
        }
        .header-left h1 {
            font-size: 1.5rem;
            margin: 0;
            color: white;
        }
        .header-left p {
            margin: 0;
            font-size: 0.9em;
            opacity: 0.8;
        }
        .header-right {
            text-align: right;
        }

        /* Tabs Styles */
        .tab-container {
            background: #ffffff;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            overflow: hidden;
        }
        .tab-buttons {
            display: flex;
            background-color: #e9ecef;
            border-bottom: 1px solid #dee2e6;
            flex-wrap: wrap;
        }
        .tab-buttons button {
            background-color: inherit;
            border: none;
            outline: none;
            cursor: pointer;
            padding: 15px 20px;
            transition: 0.3s;
            font-size: 1rem;
            font-weight: 600;
            color: #495057;
            flex-grow: 1;
            text-align: center;
        }
        .tab-buttons button:hover {
            background-color: #dee2e6;
        }
        .tab-buttons button.active {
            background-color: #ffffff;
            color: #003366;
            border-bottom: 3px solid #e74c3c;
        }

        /* Tab Content Styles */
        .tab-content {
            display: none;
            padding: 30px;
            animation: fadeIn 0.4s;
        }
        .tab-content.active {
            display: block;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .platform-header {
            margin-bottom: 20px;
            border-bottom: 1px solid #eee;
            padding-bottom: 15px;
        }
        .platform-header h2 {
            color: #003366;
            font-size: 1.6em;
            margin-bottom: 10px;
        }
        
        .market-info {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 20px;
            background-color: #f8f9fa;
            padding: 20px;
            border-radius: 6px;
            margin-bottom: 25px;
            border-left: 4px solid #003366;
        }
        .market-info div strong {
            display: block;
            color: #003366;
            margin-bottom: 5px;
            font-size: 1.1em;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        .tech-section h3 {
            font-size: 1.2em;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
            padding-bottom: 5px;
            border-bottom: 2px solid #eee;
        }
        .pros h3 { color: #27ae60; border-color: #27ae60; }
        .cons h3 { color: #e74c3c; border-color: #e74c3c; }
        
        .tech-list {
            list-style: none;
        }
        .tech-list li {
            margin-bottom: 15px;
            font-size: 0.95em;
            background: #fff;
            padding: 12px 15px;
            border-radius: 6px;
            border: 1px solid #eaeaea;
        }
        .tech-list li strong {
            display: block;
            color: #333;
            margin-bottom: 4px;
        }

        /* Table Styles */
        .hw-table-container {
            overflow-x: auto;
            margin-top: 20px;
        }
        .hw-table {
            width: 100%;
            border-collapse: collapse;
            background: #fff;
        }
        .hw-table th, .hw-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #eaeaea;
            font-size: 0.95em;
        }
        .hw-table th {
            background-color: #003366;
            color: white;
            font-weight: 600;
        }
        .hw-table tr:hover {
            background-color: #f8f9fa;
        }
        .hw-table td:first-child {
            font-weight: 600;
            color: #003366;
        }
        .badge {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.85em;
            font-weight: bold;
            color: white;
        }
        .badge.ont { background-color: #2980b9; }
        .badge.olt { background-color: #e67e22; }
        .badge.router { background-color: #27ae60; }

        @media (max-width: 768px) {
            .market-info, .tech-grid {
                grid-template-columns: 1fr;
            }
            .header {
                flex-direction: column;
                text-align: center;
                gap: 15px;
            }
            .header-right {
                text-align: center;
            }
            .tab-buttons button {
                padding: 12px 10px;
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>

<div class="container">
    
    <div class="lang-switch-container">
        <button id="btn-en" class="active-lang" onclick="switchLanguage('en')">English</button>
        <button id="btn-pt" onclick="switchLanguage('pt')">Português</button>
    </div>

    <div class="header">
        <div class="header-left">
            
            <div>
                <h1>
                    <span class="lang-en">Strategic ACS Platforms Analysis</span>
                    <span class="lang-pt">Análise Estratégica de Plataformas ACS</span>
                </h1>
                <p>
                    <span class="lang-en">Market Share & Technical Overview - Brazilian ISPs</span>
                    <span class="lang-pt">Market Share e Visão Geral Técnica - ISPs Brasileiros</span>
               </p>
           </div>
        </div>
        <div class="header-right">
            <strong style="font-size: 1.1em;">Denis Fernandes</strong><br>
            <span style="font-size: 0.85em; background:#f39c12; color:white; padding:2px 8px; border-radius:4px; font-weight:bold;">Technical Manager at Aprecomm</span>
        </div>
    </div>

    <div class="tab-container">
        
        <div class="tab-buttons">
            <button class="tab-link active" onclick="openTab(event, 'Anlix')">Anlix</button>
            <button class="tab-link" onclick="openTab(event, 'IXC')">IXC ACS</button>
            <button class="tab-link" onclick="openTab(event, 'RemoteISP')">RemoteISP</button>
            <button class="tab-link" onclick="openTab(event, 'Made4Graph')">Made4Graph</button>
            <button class="tab-link" onclick="openTab(event, 'Aprecomm')">Aprecomm</button>
            <button class="tab-link" onclick="openTab(event, 'Hardware')" style="color: #e74c3c;">
                <span class="lang-en">Hardware Integration</span>
                <span class="lang-pt">Homologação de Hardware</span>
            </button>
        </div>

        <div id="Anlix" class="tab-content active">
            <div class="platform-header">
                <h2>Anlix (Flashman / Flashboard)</h2>
                <p>
                    <span class="lang-en">The main Brazilian reference in telemetry focused on Wi-Fi Quality of Experience (QoE) and root cause analysis.</span>
                    <span class="lang-pt">A principal referência brasileira em telemetria focada na Qualidade de Experiência (QoE) do Wi-Fi e análise de causa raiz.</span>
                </p>
            </div>
            <div class="market-info">
                <div>
                    <strong>
                        <span class="lang-en">Size in Brazil</span>
                        <span class="lang-pt">Tamanho no Brasil</span>
                    </strong>
                    <p>
                        <span class="lang-en">Dominant. Over 10 million connected devices.</span>
                        <span class="lang-pt">Dominante. Mais de 10 milhões de dispositivos conectados.</span>
                    </p>
                </div>
                <div>
                    <strong>
                        <span class="lang-en">Market Profile</span>
                        <span class="lang-pt">Perfil de Mercado</span>
                    </strong>
                    <p>
                        <span class="lang-en">The "gold standard" tool for Super ISPs and large regional operations (such as Vero, Ligga, and Alloha). Anlix captures the largest share of the market focused on Wi-Fi Quality of Experience (QoE) and predictive analytics. Providers with massive direct purchasing power use this platform to unify device fleets acquired through mergers and acquisitions.</span>
                        <span class="lang-pt">A ferramenta "padrão-ouro" para Super ISPs e grandes operações regionais (como Vero, Ligga e Alloha). A Anlix captura a maior fatia do mercado focado em QoE de Wi-Fi e análises preditivas. Provedores com forte poder de compra direto usam esta plataforma para unificar parques adquiridos via fusões e aquisições.</span>
                    </p>
                </div>
            </div>
            <div class="tech-grid">
                <div class="tech-section pros">
                    <h3>
                        <span class="lang-en">Technical Advantages</span>
                        <span class="lang-pt">Vantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">End-to-End QoE Mapping:</span>
                                <span class="lang-pt">Mapeamento QoE Fim-a-Fim:</span>
                            </strong>
                            <span class="lang-en">Unlike a standard ACS, Flashboard reads parameters from every connected device in the customer's home (TV, smartphone, notebook), identifying specific Wi-Fi bottlenecks.</span>
                            <span class="lang-pt">Diferente de um ACS comum, o Flashboard lê parâmetros de cada dispositivo conectado na casa do cliente (TV, celular, notebook), identificando gargalos específicos do Wi-Fi.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Agile Certification:</span>
                                <span class="lang-pt">Homologação Ágil:</span>
                            </strong>
                            <span class="lang-en">As Broadband Forum members, they have a very fast process for integrating new brands and extracting proprietary parameters from complex ONTs (like Mesh networks).</span>
                            <span class="lang-pt">Como membros do Broadband Forum, possuem um processo ágil para homologar novas marcas e extrair parâmetros proprietários de ONTs complexas (como redes Mesh).</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">ERP Agnostic:</span>
                                <span class="lang-pt">Agnóstico a ERP:</span>
                            </strong>
                            <span class="lang-en">Features a robust open API, integrating easily with various billing and management systems.</span>
                            <span class="lang-pt">Possui API aberta e robusta, integrando-se facilmente com diversos sistemas de faturamento e gestão.</span>
                        </li>
                    </ul>
                </div>
                <div class="tech-section cons">
                    <h3>
                        <span class="lang-en">Technical Disadvantages</span>
                        <span class="lang-pt">Desvantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Cost Model:</span>
                                <span class="lang-pt">Modelo de Custos:</span>
                            </strong>
                            <span class="lang-en">Being a premium platform charged separately (usually per device license), it can be cost-prohibitive for very small ISPs with low Average Revenue Per User (ARPU).</span>
                            <span class="lang-pt">Por ser uma plataforma premium cobrada à parte (geralmente por licença/dispositivo), pode ser proibitiva para pequenos ISPs com baixo Ticket Médio (ARPU).</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Restricted Focus ("Last Mile"):</span>
                                <span class="lang-pt">Foco Restrito ("Última Milha"):</span>
                            </strong>
                            <span class="lang-en">The tool is brilliant inside the customer's home, but the provider will still need other platforms to manage the network core (concentrators and switches).</span>
                            <span class="lang-pt">A ferramenta é excelente dentro da casa do cliente, mas o provedor ainda precisará de outras plataformas para gerenciar o "core" da rede (concentradores e switches).</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div id="IXC" class="tab-content">
            <div class="platform-header">
                <h2>IXC ACS (IXC Soft)</h2>
                <p>
                    <span class="lang-en">The platform with the highest market penetration among small and medium regional ISPs, driven by the strength of its native ERP.</span>
                    <span class="lang-pt">A plataforma com maior capilaridade no mercado de provedores regionais de pequeno e médio porte, impulsionada pela força do seu ERP nativo.</span>
                </p>
            </div>
            <div class="market-info">
                <div>
                    <strong>
                        <span class="lang-en">Size in Brazil</span>
                        <span class="lang-pt">Tamanho no Brasil</span>
                    </strong>
                    <p>
                        <span class="lang-en">Over 1.6 million managed devices distributed across more than 550 client providers.</span>
                        <span class="lang-pt">Mais de 1,6 milhão de dispositivos gerenciados, distribuídos em mais de 550 provedores clientes.</span>
                    </p>
                </div>
                <div>
                    <strong>
                        <span class="lang-en">Market Profile</span>
                        <span class="lang-pt">Perfil de Mercado</span>
                    </strong>
                    <p>
                        <span class="lang-en">The great strength of IXC ACS is not the massive volume of ONTs, but its extreme fragmentation. It "piggybacks" on the IXC ERP, which is the absolute leading software among thousands of small and medium ISPs in Brazil. For the large mass of regional providers looking to handle billing, inventory, and basic Wi-Fi management on a single screen, IXC ACS is almost always the primary choice.</span>
                        <span class="lang-pt">A grande força do IXC ACS não é o volume massivo, mas a sua extrema pulverização. Ele pega "carona" no IXC Provedor, o ERP líder absoluto entre pequenos e médios ISPs no Brasil. Para a grande massa de regionais que buscam resolver faturamento, estoque e gerência básica de Wi-Fi em uma única tela, o IXC ACS é quase sempre a escolha principal.</span>
                    </p>
                </div>
            </div>
            <div class="tech-grid">
                <div class="tech-section pros">
                    <h3>
                        <span class="lang-en">Technical Advantages</span>
                        <span class="lang-pt">Vantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Native Transparent Integration:</span>
                                <span class="lang-pt">Integração Nativa e Transparente:</span>
                            </strong>
                            <span class="lang-en">Being from the same ecosystem as the leading ERP in Brazil, the provisioning flow is practically immediate without requiring third-party API integrations.</span>
                            <span class="lang-pt">Sendo do mesmo ecossistema do ERP líder no Brasil, o fluxo de provisionamento é quase imediato, sem necessitar de integrações de API de terceiros.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Minimal Learning Curve (N1):</span>
                                <span class="lang-pt">Curva de Aprendizado Mínima (N1):</span>
                            </strong>
                            <span class="lang-en">The interface is designed for support agents with low networking knowledge. Features like "Anti-reset" work very fluidly.</span>
                            <span class="lang-pt">A interface é desenhada para atendentes com baixo conhecimento técnico de redes. Recursos como "Anti-reset" funcionam de forma muito fluida.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Cost-Benefit:</span>
                                <span class="lang-pt">Custo-Benefício:</span>
                            </strong>
                            <span class="lang-en">Usually embedded or negotiated in bundles along with the ERP, lowering the barrier to entry for smaller ISPs.</span>
                            <span class="lang-pt">Geralmente embutido ou negociado em pacotes junto com o ERP, reduzindo a barreira de entrada para ISPs menores.</span>
                        </li>
                    </ul>
                </div>
                <div class="tech-section cons">
                    <h3>
                        <span class="lang-en">Technical Disadvantages</span>
                        <span class="lang-pt">Desvantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Vendor Lock-in:</span>
                                <span class="lang-pt">Fidelização Forçada (Lock-in):</span>
                            </strong>
                            <span class="lang-en">If the provider decides to switch ERPs in the future, they lose the ACS and all the automation built around it.</span>
                            <span class="lang-pt">Se o provedor decidir trocar de ERP no futuro, ele perde o ACS e toda a automação construída em torno dele.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Limited to Basics:</span>
                                <span class="lang-pt">Limitado ao Básico:</span>
                            </strong>
                            <span class="lang-en">The platform is excellent for standard operations (traditional TR-069, PPPoE, Wi-Fi password changes), but lacks deep telemetry (TR-369) and predictive analytical intelligence compared to dedicated platforms.</span>
                            <span class="lang-pt">Excelente para operações padrão (TR-069, PPPoE, troca de senha), mas carece de telemetria profunda (TR-369) e inteligência analítica preditiva comparado a plataformas dedicadas.</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div id="RemoteISP" class="tab-content">
            <div class="platform-header">
                <h2>RemoteISP (Int6 Tech)</h2>
                <p>
                    <span class="lang-en">The major multivendor bet for providers seeking operational standardization.</span>
                    <span class="lang-pt">A grande aposta multivendor para provedores que buscam padronização operacional.</span>
                </p>
            </div>
            <div class="market-info">
                <div>
                    <strong>
                        <span class="lang-en">Size in Brazil</span>
                        <span class="lang-pt">Tamanho no Brasil</span>
                    </strong>
                    <p>
                        <span class="lang-en">High penetration, with over 2 million monitored subscribers and around 60,000 new monthly activations.</span>
                        <span class="lang-pt">Alta penetração, com mais de 2 milhões de assinantes monitorados e cerca de 60.000 novas ativações mensais.</span>
                    </p>
                </div>
                <div>
                    <strong>
                        <span class="lang-en">Market Profile</span>
                        <span class="lang-pt">Perfil de Mercado</span>
                    </strong>
                    <p>
                        <span class="lang-en">Holds a very strong share among medium and large providers operating with highly heterogeneous networks (a mix of several ONT and router brands). Because it is agnostic and heavily focused on standardizing the support view, it is the top choice for those wanting to escape dependency on a specific ERP.</span>
                        <span class="lang-pt">Possui forte atuação entre provedores médios e grandes com redes altamente heterogêneas (mistura de várias marcas de ONTs e roteadores). Por ser agnóstico e focado em padronizar a visão de suporte, é a principal escolha de quem quer fugir da dependência de um ERP específico.</span>
                    </p>
                </div>
            </div>
            <div class="tech-grid">
                <div class="tech-section pros">
                    <h3>
                        <span class="lang-en">Technical Advantages</span>
                        <span class="lang-pt">Vantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Truly Multivendor:</span>
                                <span class="lang-pt">Verdadeiramente Multivendor:</span>
                            </strong>
                            <span class="lang-en">The platform's engine translates complex data trees from different manufacturers and displays everything on a standardized screen. The agent doesn't need to know the equipment brand to operate it.</span>
                            <span class="lang-pt">O motor "traduz" árvores de dados complexas de diferentes fabricantes e exibe tudo em uma tela padronizada. O atendente não precisa saber a marca do equipamento para operá-lo.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Technological Evolution:</span>
                                <span class="lang-pt">Evolução Tecnológica:</span>
                            </strong>
                            <span class="lang-en">Already supports TR-369 (USP), which is essential for managing Wi-Fi 6 routers and modern Mesh networks more securely (TLS) and with lower management bandwidth.</span>
                            <span class="lang-pt">Já suporta TR-369 (USP), essencial para gerenciar roteadores Wi-Fi 6 e redes Mesh modernas de forma mais segura (TLS) e com menor uso de banda de gerência.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Agent Architecture (CGNAT):</span>
                                <span class="lang-pt">Arquitetura de Agentes (CGNAT):</span>
                            </strong>
                            <span class="lang-en">Developed with distributed agents that seamlessly bypass communication issues caused by reverse NAT or CGNAT.</span>
                            <span class="lang-pt">Desenvolvida com agentes distribuídos que contornam perfeitamente problemas de comunicação causados por NAT reverso ou CGNAT.</span>
                        </li>
                    </ul>
                </div>
                <div class="tech-section cons">
                    <h3>
                        <span class="lang-en">Technical Disadvantages</span>
                        <span class="lang-pt">Desvantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">External Integration Dependency:</span>
                                <span class="lang-pt">Dependência de Integração Externa:</span>
                            </strong>
                            <span class="lang-en">Being a stand-alone system, the provider will have to invest time (or money) to integrate their ERP activations with RemoteISP via API.</span>
                            <span class="lang-pt">Sendo um sistema independente (stand-alone), o provedor terá que investir tempo ou dinheiro para integrar as ativações do ERP via API.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Fierce Mass Market Competition:</span>
                                <span class="lang-pt">Forte Concorrência no Mercado de Massa:</span>
                            </strong>
                            <span class="lang-en">Faces the challenge of convincing medium-sized ISPs to pay for a separate ACS when their current ERP already offers a "free" built-in module.</span>
                            <span class="lang-pt">Enfrenta o desafio de convencer ISPs médios a pagar por um ACS separado quando o seu ERP atual já oferece um módulo "gratuito" embutido.</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div id="Made4Graph" class="tab-content">
            <div class="platform-header">
                <h2>Made4Graph (Made4it)</h2>
                <p>
                    <span class="lang-en">A platform born focused on the network "Core" (PPPoE concentrators) that expanded into customer home management (TR-069).</span>
                    <span class="lang-pt">Uma plataforma que nasceu focada no "Core" da rede (concentradores PPPoE) e se expandiu para a gerência da casa do cliente (TR-069).</span>
                </p>
            </div>
            <div class="market-info">
                <div>
                    <strong>
                        <span class="lang-en">Size in Brazil</span>
                        <span class="lang-pt">Tamanho no Brasil</span>
                    </strong>
                    <p>
                        <span class="lang-en">Used by over 200 companies and strategic providers.</span>
                        <span class="lang-pt">Utilizada por mais de 200 empresas e provedores estratégicos.</span>
                    </p>
                </div>
                <div>
                    <strong>
                        <span class="lang-en">Market Profile</span>
                        <span class="lang-pt">Perfil de Mercado</span>
                    </strong>
                    <p>
                        <span class="lang-en">The share focused solely on CPEs is smaller, but the platform dominates a critical niche: heavy traffic management, CGNAT, and BRAS/BNG. It is the tool of choice for ISPs with advanced network engineering teams needing deep logs for legal compliance and internal network diagnostics.</span>
                        <span class="lang-pt">A fatia focada apenas em CPEs é menor, mas a plataforma domina um nicho crítico: gestão pesada de tráfego, CGNAT e BRAS/BNG. É a ferramenta escolhida por ISPs com equipes de engenharia avançadas que precisam de logs profundos para compliance legal e diagnósticos de rede interna.</span>
                    </p>
                </div>
            </div>
            <div class="tech-grid">
                <div class="tech-section pros">
                    <h3>
                        <span class="lang-en">Technical Advantages</span>
                        <span class="lang-pt">Vantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Direct BRAS/BNG Integration:</span>
                                <span class="lang-pt">Integração Direta BRAS/BNG:</span>
                            </strong>
                            <span class="lang-en">The strongest tool for analyzing traffic directly at the source (Cisco, Huawei, Juniper, Mikrotik), crossing concentrator information with the customer's ONU.</span>
                            <span class="lang-pt">A ferramenta mais forte para analisar o tráfego direto na fonte (Cisco, Huawei, Juniper, Mikrotik), cruzando informações do concentrador com a ONU do cliente.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Long Historical Retention (Compliance):</span>
                                <span class="lang-pt">Retenção Histórica (Compliance):</span>
                            </strong>
                            <span class="lang-en">Stores bandwidth and IP usage graphs for up to 5 years, acting as a critical tool for legal compliance.</span>
                            <span class="lang-pt">Armazena gráficos de uso de banda e IP por até 5 anos, atuando como ferramenta crítica para conformidade legal (Marco Civil da Internet).</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Deep IP Management:</span>
                                <span class="lang-pt">Gestão Profunda de IP:</span>
                            </strong>
                            <span class="lang-en">Excellent for network engineering to control IPv4 exhaustion and IPv6 delegation.</span>
                            <span class="lang-pt">Excelente para a engenharia de rede controlar o esgotamento do IPv4 e a delegação do IPv6.</span>
                        </li>
                    </ul>
                </div>
                <div class="tech-section cons">
                    <h3>
                        <span class="lang-en">Technical Disadvantages</span>
                        <span class="lang-pt">Desvantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Technical Interface:</span>
                                <span class="lang-pt">Interface Técnica:</span>
                            </strong>
                            <span class="lang-en">Because it handles edge router and concentrator data, the interface is denser, requiring slightly more training for basic N1 attendants.</span>
                            <span class="lang-pt">Como lida com dados de roteadores de borda e concentradores, a interface é mais densa, exigindo um pouco mais de treinamento para atendentes N1.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Secondary TR-069 Module:</span>
                                <span class="lang-pt">Módulo TR-069 Secundário:</span>
                            </strong>
                            <span class="lang-en">While their TR-069 module is good, it is an add-on to a network monitoring tool, lacking the same depth of User Experience (UX) for in-home diagnostics as dedicated platforms.</span>
                            <span class="lang-pt">Embora o módulo TR-069 seja bom, ele é um complemento a uma ferramenta de monitoramento de rede, não tendo a mesma profundidade de UX para diagnósticos residenciais que as plataformas dedicadas.</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div id="Aprecomm" class="tab-content">
            <div class="platform-header">
                <h2>Aprecomm</h2>
                <p>
                    <span class="lang-en">The "High-End" global player, intensely focused on Artificial Intelligence and Self-Healing networks.</span>
                    <span class="lang-pt">O player global "High-End", focado intensamente em Inteligência Artificial e redes Self-Healing.</span>
                </p>
            </div>
            <div class="market-info">
                <div>
                    <strong>
                        <span class="lang-en">Size in Brazil</span>
                        <span class="lang-pt">Tamanho no Brasil</span>
                    </strong>
                    <p>
                        <span class="lang-en">Globally exceeds 7 million devices, but operates in a highly segmented top-tier layer in the Brazilian market.</span>
                        <span class="lang-pt">Globalmente ultrapassa os 7 milhões de dispositivos, mas opera em uma camada de topo altamente segmentada no mercado brasileiro.</span>
                    </p>
                </div>
                <div>
                    <strong>
                        <span class="lang-en">Market Profile</span>
                        <span class="lang-pt">Perfil de Mercado</span>
                    </strong>
                    <p>
                        <span class="lang-en">Entering the Brazilian market, they have a solution capable of competing head-to-head with any of the aforementioned platforms. However, as they still lack major clients in Brazil, pricing will be a key differentiator to accelerate market penetration. Even with their AI solution, they still have few supported products, making an active product integration effort essential.</span>
                        <span class="lang-pt">Entrando no Brasil, tem solução para competir de igual para igual com qualquer outra citada. Mas, ainda sem grandes clientes no Brasil, preço será o diferencial para entrar mais rápido. Mesmo com a solução de AI, ainda possuem poucos produtos homologados, sendo importante ter uma frente ativa de homologação de produtos.</span>
                    </p>
                </div>
            </div>
            <div class="tech-grid">
                <div class="tech-section pros">
                    <h3>
                        <span class="lang-en">Technical Advantages</span>
                        <span class="lang-pt">Vantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Self-Healing Automation:</span>
                                <span class="lang-pt">Automação Self-Healing:</span>
                            </strong>
                            <span class="lang-en">The tool doesn't just point out the problem; the AI automatically adjusts Wi-Fi channels, frequencies, and power in the customer's home without human intervention.</span>
                            <span class="lang-pt">A ferramenta não apenas aponta o problema; a IA ajusta automaticamente canais, frequências e potência do Wi-Fi na casa do cliente sem intervenção humana.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Chipset Pre-integration:</span>
                                <span class="lang-pt">Pré-integração de Chipset:</span>
                            </strong>
                            <span class="lang-en">Operates at the hardware level. Their software (VCS) comes pre-integrated into major Asian manufacturers' chipsets, ensuring extremely deep and native data collection.</span>
                            <span class="lang-pt">Opera a nível de hardware. O software deles (VCS) já vem pré-integrado nos chipsets dos maiores fabricantes asiáticos, garantindo coleta de dados extremamente profunda e nativa.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Upsell Intelligence:</span>
                                <span class="lang-pt">Inteligência de Upsell:</span>
                            </strong>
                            <span class="lang-en">The AI analyzes household traffic and alerts the sales team: "This customer is heavily streaming in 4K and bottlenecking the Wi-Fi; offer a 1 Gig upgrade or an extra Mesh node."</span>
                            <span class="lang-pt">A IA analisa o tráfego doméstico e alerta a equipe de vendas: "Este cliente consome muito streaming em 4K e gargala o Wi-Fi; ofereça um upgrade para 1 Giga ou um ponto Mesh extra."</span>
                        </li>
                    </ul>
                </div>
                <div class="tech-section cons">
                    <h3>
                        <span class="lang-en">Technical Disadvantages</span>
                        <span class="lang-pt">Desvantagens Técnicas</span>
                    </h3>
                    <ul class="tech-list">
                        <li>
                            <strong>
                                <span class="lang-en">Overkill for Basic ISPs:</span>
                                <span class="lang-pt">Overkill (Exagero) para ISPs Básicos:</span>
                            </strong>
                            <span class="lang-en">The features are incredible but excessive for regional providers who simply want a tool to change router passwords remotely.</span>
                            <span class="lang-pt">As funcionalidades são incríveis, mas excessivas para provedores regionais que buscam apenas uma ferramenta para trocar senhas de roteador remotamente.</span>
                        </li>
                        <li>
                            <strong>
                                <span class="lang-en">Exchange Rate Cost Model:</span>
                                <span class="lang-pt">Modelo de Custo Cambial:</span>
                            </strong>
                            <span class="lang-en">As a global solution with high cloud AI processing loads, pricing is often tied to the dollar or premium licenses, making it a niche product for Tier 3 Super ISPs.</span>
                            <span class="lang-pt">Sendo uma solução global com altas cargas de processamento de IA em nuvem, a precificação frequentemente atrelada ao dólar a torna um produto de nicho para Super ISPs (Tier 3).</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div id="Hardware" class="tab-content">
            <div class="platform-header">
                <h2>
                    <span class="lang-en">Hardware Integration Overview</span>
                    <span class="lang-pt">Visão Geral de Homologação de Hardware</span>
                </h2>
                <p>
                    <span class="lang-en">Status of key equipment integration across major ACS and telemetry platforms in the Brazilian market.</span>
                    <span class="lang-pt">Status de integração dos principais equipamentos nas maiores plataformas de ACS e telemetria do mercado brasileiro.</span>
                </p>
            </div>
            
            <div class="hw-table-container">
                <table class="hw-table">
                    <thead>
                        <tr>
                            <th>
                                <span class="lang-en">Manufacturer</span>
                                <span class="lang-pt">Fabricante</span>
                            </th>
                            <th>
                                <span class="lang-en">Product</span>
                                <span class="lang-pt">Produto</span>
                            </th>
                            <th>
                                <span class="lang-en">Model</span>
                                <span class="lang-pt">Modelo</span>
                            </th>
                            <th>
                                <span class="lang-en">ACS Integration Status</span>
                                <span class="lang-pt">Status de Homologação ACS</span>
                            </th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Fiberhome</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>HG6154F3</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>
                        <tr>
                            <td>Fiberhome</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>HG6145F</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>
                        <tr>
                            <td>Fiberhome</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>HG6245D</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>
                        <tr>
                            <td>Fiberhome</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>SR1041Y (Wi-Fi 6)</td>
                            <td>
                                <span class="lang-en">Advanced Integration (TR-369 Ready / Anlix)</span>
                                <span class="lang-pt">Avançado (Pronto para TR-369 / Anlix)</span>
                            </td>
                        </tr>

                        <tr>
                            <td>Huawei</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>EG8145V5</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>
                        <tr>
                            <td>Huawei</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>OptiXstar K562 (Wi-Fi 6)</td>
                            <td>
                                <span class="lang-en">Partially Supported (TR-369 / Anlix, IXC, RemoteISP)</span>
                                <span class="lang-pt">Parcialmente Homologado (TR-369 / Anlix, IXC, RemoteISP)</span>
                            </td>
                        </tr>

                        <tr>
                            <td>ZTE</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>F670L</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>
                        <tr>
                            <td>ZTE</td>
                            <td><span class="badge ont">ONT</span></td>
                            <td>F6600 (Wi-Fi 6)</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>

                        <tr>
                            <td>TP-Link</td>
                            <td><span class="badge router">Router</span></td>
                            <td>EC220-G5</td>
                            <td>
                                <span class="lang-en">Partially Supported (Agile Config / Anlix, IXC)</span>
                                <span class="lang-pt">Parcialmente Homologado (Agile Config / Anlix, IXC)</span>
                            </td>
                        </tr>
                        <tr>
                            <td>TP-Link</td>
                            <td><span class="badge router">Router</span></td>
                            <td>EX220 (Wi-Fi 6)</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>

                        <tr>
                            <td>Intelbras</td>
                            <td><span class="badge router">Router</span></td>
                            <td>Wi-Force GF 1200</td>
                            <td>
                                <span class="lang-en">Fully Supported</span>
                                <span class="lang-pt">Totalmente Homologado</span>
                            </td>
                        </tr>
                        <tr>
                            <td>Intelbras</td>
                            <td><span class="badge router">Router</span></td>
                            <td>RX 1500 (Wi-Fi 6)</td>
                            <td>
                                <span class="lang-en">Fully Supported (InMesh Supported)</span>
                                <span class="lang-pt">Totalmente Homologado (Suporte InMesh)</span>
                            </td>
                        </tr>

                        <tr>
                            <td>Fiberhome</td>
                            <td><span class="badge olt">OLT</span></td>
                            <td>AN6000-15</td>
                            <td>
                                <span class="lang-en">Partially Supported <em>(RemoteISP and Made4it)</em></span>
                                <span class="lang-pt">Parcialmente Homologado <em>(RemoteISP e Made4it)</em></span>
                            </td>
                        </tr>
                        <tr>
                            <td>Fiberhome</td>
                            <td><span class="badge olt">OLT</span></td>
                            <td>AN6000-17</td>
                            <td>
                                <span class="lang-en">Partially Supported <em>(RemoteISP and Made4it)</em></span>
                                <span class="lang-pt">Parcialmente Homologado <em>(RemoteISP e Made4it)</em></span>
                            </td>
                        </tr>
                        <tr>
                            <td>Huawei</td>
                            <td><span class="badge olt">OLT</span></td>
                            <td>MA5800-X15</td>
                            <td>
                                <span class="lang-en">Partially Supported <em>(RemoteISP and Made4it)</em></span>
                                <span class="lang-pt">Parcialmente Homologado <em>(RemoteISP e Made4it)</em></span>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>

    </div>
</div>

<script>
    function openTab(evt, platformName) {
        var i, tabcontent, tablinks;
        tabcontent = document.getElementsByClassName("tab-content");
        for (i = 0; i < tabcontent.length; i++) {
            tabcontent[i].style.display = "none";
            tabcontent[i].classList.remove("active");
        }

        tablinks = document.getElementsByClassName("tab-link");
        for (i = 0; i < tablinks.length; i++) {
            tablinks[i].classList.remove("active");
        }

        document.getElementById(platformName).style.display = "block";
        document.getElementById(platformName).classList.add("active");
        evt.currentTarget.classList.add("active");
    }

    function switchLanguage(lang) {
        if(lang === 'pt') {
            document.body.classList.add('pt-active');
            document.getElementById('btn-pt').classList.add('active-lang');
            document.getElementById('btn-en').classList.remove('active-lang');
        } else {
            document.body.classList.remove('pt-active');
            document.getElementById('btn-en').classList.add('active-lang');
            document.getElementById('btn-pt').classList.remove('active-lang');
        }
    }
</script>

</body>
</html>

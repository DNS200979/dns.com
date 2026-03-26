<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Strategic Summary - Fiberhome</title>
    <style>
        /* Paleta de Cores Fiberhome */
        :root {
            --fiber-blue: #004B87;
            --fiber-orange: #FF6A13;
            --bg-dark: #002D52;
            --text-dark: #333;
            --text-light: #fff;
        }

        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: linear-gradient(135deg, var(--fiber-blue) 0%, var(--bg-dark) 100%);
            color: var(--text-dark);
            line-height: 1.6;
            margin: 0;
            padding: 60px 20px 40px 20px; /* Top padding adjusted for lang toggle */
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            padding: 40px;
            border-top: 8px solid var(--fiber-orange);
            position: relative;
        }

        /* Language Toggle Styles */
        .lang-switch-container {
            position: absolute;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }
        .lang-switch-container button {
            background-color: #f8f9fa;
            border: 1px solid #ccc;
            padding: 6px 14px;
            cursor: pointer;
            border-radius: 4px;
            font-weight: bold;
            color: var(--fiber-blue);
            transition: 0.3s;
            margin-left: 5px;
        }
        .lang-switch-container button.active-lang {
            background-color: var(--fiber-orange);
            color: white;
            border-color: var(--fiber-orange);
        }

        /* Language Display Logic */
        .lang-pt { display: none !important; }
        body.pt-active .lang-en { display: none !important; }
        body.pt-active .lang-pt { display: inline !important; }

        /* Typography & Layout */
        h1 {
            color: var(--fiber-blue);
            font-size: 2.2em;
            margin-top: 0;
            border-bottom: 2px solid #eee;
            padding-bottom: 15px;
            padding-right: 100px; /* Space for language buttons */
        }

        h2 {
            color: var(--fiber-orange);
            font-size: 1.5em;
            margin-top: 30px;
            margin-bottom: 15px;
        }

        p {
            font-size: 1.1em;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        ul li {
            background-color: #f8f9fa;
            margin-bottom: 15px;
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid var(--fiber-blue);
        }

        /* Destaque para os links do Edital */
        .edital-link {
            display: inline-block;
            color: var(--fiber-blue);
            font-weight: bold;
            text-decoration: none;
            background-color: #e6f0fa;
            padding: 4px 8px;
            border-radius: 4px;
            border-bottom: 2px solid var(--fiber-blue);
            transition: all 0.3s ease;
            margin: 5px 0;
        }

        .edital-link:hover {
            background-color: var(--fiber-blue);
            color: var(--text-light);
        }

        .edital-link::before {
            content: '📄 ';
        }

        /* Destaque para Perguntas Estratégicas */
        .question-highlight {
            background-color: var(--fiber-orange);
            color: var(--text-light);
            padding: 15px 20px;
            border-radius: 6px;
            font-weight: bold;
            font-size: 1.1em;
            margin-top: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 10px rgba(255, 106, 19, 0.3);
        }

        .question-highlight::before {
            content: '❓';
            font-size: 1.5em;
        }

        .solution {
            color: #27ae60;
            font-weight: 600;
        }

        .combo-box {
            background-color: #e6f0fa;
            padding: 20px;
            border-radius: 8px;
            border: 2px dashed var(--fiber-blue);
            margin-top: 20px;
        }

        .combo-box ul li {
            background-color: transparent;
            border: none;
            padding: 5px 0;
            margin: 0;
            font-size: 1.1em;
            font-weight: bold;
            color: var(--fiber-blue);
        }
        
        .combo-box ul li::before {
            content: '✓ ';
            color: var(--fiber-orange);
        }
    </style>
</head>
<body>
    <div class="container">
        
        <div class="lang-switch-container">
            <button id="btn-en" class="active-lang" onclick="switchLanguage('en')">EN</button>
            <button id="btn-pt" onclick="switchLanguage('pt')">PT</button>
        </div>

        <h1>
            <span class="lang-en">Strategic Summary - Compliance with Bid 021/2025</span>
            <span class="lang-pt">Resumo Estratégico - Adesão ao Edital 021/2025</span>
        </h1>
        
        <p>
            <span class="lang-en">Based on the analysis of Public Tender No. 021/2025 from the Municipality of Pindamonhangaba (Smart City as a Service - SCaaS) and the Fiberhome product portfolio.</span>
            <span class="lang-pt">Baseado na análise do Edital de Concorrência Pública nº 021/2025 da Prefeitura de Pindamonhangaba (Smart City as a Service - SCaaS) e no portfólio de produtos Fiberhome.</span>
        </p>

        <h2>
            <span class="lang-en">1. What Fiberhome perfectly fulfills</span>
            <span class="lang-pt">1. O que a Fiberhome atende perfeitamente</span>
        </h2>
        <ul>
            <li>
                <strong>
                    <span class="lang-en">Metro Ethernet Network and Concentrators (Core/Edge):</span>
                    <span class="lang-pt">Rede Metro Ethernet e Concentradores (Core/Edge):</span>
                </strong><br>
                <a href="#link-edital-olt" class="edital-link" title="See item in bid">
                    <span class="lang-en">Bid Requirement: The project requires concentration points with "Hybrid XGS-PON/GPON OLT"</span>
                    <span class="lang-pt">Requisito do Edital: O projeto exige pontos de concentração com "Hybrid XGS-PON/GPON OLT"</span>
                </a><br>
                <span class="solution">
                    <span class="lang-en">Fiberhome Solution:</span>
                    <span class="lang-pt">Solução Fiberhome:</span>
                </span> 
                <span class="lang-en">AN6000 Series (AN6000-15 and AN6000-17), hybrid GPON/XGS-PON platforms (and up to 50G PON).</span>
                <span class="lang-pt">Série AN6000 (AN6000-15 e AN6000-17), plataformas híbridas GPON/XGS-PON (e até 50G PON).</span>
            </li>
            <li>
                <strong>
                    <span class="lang-en">Edge Equipment and Wi-Fi 6 (CPEs):</span>
                    <span class="lang-pt">Equipamentos de Borda e Wi-Fi 6 (CPEs):</span>
                </strong><br>
                <a href="#link-edital-wifi" class="edital-link" title="See item in bid">
                    <span class="lang-en">Bid Requirement: Wi-Fi 6 connectivity in public buildings and streets</span>
                    <span class="lang-pt">Requisito do Edital: Conectividade Wi-Fi 6 em prédios públicos e ruas</span>
                </a><br>
                <span class="solution">
                    <span class="lang-en">Fiberhome Solution:</span>
                    <span class="lang-pt">Solução Fiberhome:</span>
                </span> 
                <span class="lang-en">SR1041Y (Wi-Fi 6), with TR-369 support for advanced telemetry.</span>
                <span class="lang-pt">SR1041Y (Wi-Fi 6), com suporte a TR-369 para telemetria avançada.</span>
            </li>
            <li>
                <strong>
                    <span class="lang-en">Standard Optical ONTs:</span>
                    <span class="lang-pt">ONTs Ópticas Padrão:</span>
                </strong><br>
                <a href="#link-edital-pontos" class="edital-link" title="See item in bid">
                    <span class="lang-en">Bid Requirement: Monitoring points and buildings needing only an optical link</span>
                    <span class="lang-pt">Requisito do Edital: Pontos de monitoramento e prédios com necessidade apenas de link óptico</span>
                </a><br>
                <span class="solution">
                    <span class="lang-en">Fiberhome Solution:</span>
                    <span class="lang-pt">Solução Fiberhome:</span>
                </span> 
                <span class="lang-en">Models HG6154F3, HG6145F, and HG6245D.</span>
                <span class="lang-pt">Modelos HG6154F3, HG6145F e HG6245D.</span>
            </li>
        </ul>

        <h2>
            <span class="lang-en">2. Where it will be necessary to partner or validate the roadmap</span>
            <span class="lang-pt">2. Onde será necessário compor com parceiros ou validar roadmap</span>
        </h2>
        <ul>
            <li>
                <strong>
                    <span class="lang-en">Wi-Fi 7 Indoor/Outdoor:</span>
                    <span class="lang-pt">Wi-Fi 7 Indoor/Outdoor:</span>
                </strong> 
                <span class="lang-en">Need to validate availability and lead times for certified equipment in Brazil.</span>
                <span class="lang-pt">Necessário validar disponibilidade e prazos de equipamentos certificados no Brasil.</span>
            </li>
            <li>
                <strong>
                    <span class="lang-en">Next Generation Firewall (NGFW) and SD-WAN:</span>
                    <span class="lang-pt">Next Generation Firewall (NGFW) e SD-WAN:</span>
                </strong> 
                <span class="lang-en">Requirement met by specialized brands (Fortinet, Palo Alto, Cisco).</span>
                <span class="lang-pt">Requisito atendido por marcas especializadas (Fortinet, Palo Alto, Cisco).</span>
                <div class="question-highlight">
                    <span>
                        <span class="lang-en">Strategic Question: Should Fiberhome focus strictly on transport and access, or seek official partnerships to compose the NGFW security layer?</span>
                        <span class="lang-pt">Pergunta Estratégica: A Fiberhome deve focar estritamente em transporte e acesso ou buscar parcerias oficiais para compor a camada de segurança NGFW?</span>
                    </span>
                </div>
            </li>
            <li>
                <strong>
                    <span class="lang-en">5G/LTE and Satellite Connectivity:</span>
                    <span class="lang-pt">Conectividade 5G/LTE e Satélite:</span>
                </strong> 
                <span class="lang-en">Prexx can validate availability to compose the project with modems/SIM cards from mobile operators.</span>
                <span class="lang-pt">Prexx pode validar a disponibilidade para compor o projeto com modems/SIM cards de operadoras móveis.</span>
            </li>
        </ul>

        <h2>
            <span class="lang-en">Suggested Commercial Strategy Summary</span>
            <span class="lang-pt">Resumo da Estratégia Comercial Sugerida</span>
        </h2>
        <p>
            <span class="lang-en">Fiberhome provides the "heart" of the optical network required by the municipality. The approach to ISPs and integrators should highlight the combo:</span>
            <span class="lang-pt">A Fiberhome fornece o "coração" da rede óptica exigida pelo município. A abordagem junto aos ISPs e integradores deve destacar o combo:</span>
        </p>
        
        <div class="combo-box">
            <ul>
                <li>Hybrid OLTs (AN6000)</li>
                <li>Wi-Fi 6 ONTs (HG6145F1 <span class="lang-en">and</span><span class="lang-pt">e</span> HG6145F3)</li>
            </ul>
        </div>

        <p style="margin-top: 20px;">
            <span class="lang-en">The main selling point is the robustness of the OLTs to withstand heavy traffic from cameras and sensors, coupled with the advanced management capabilities (TR-369) of the Wi-Fi 6 routers, drastically reducing OPEX for the winning provider through remote monitoring.</span>
            <span class="lang-pt">O argumento principal de venda é a robustez dos OLTs para suportar tráfego intenso de câmeras e sensores, aliado às capacidades de gestão avançada (TR-369) dos roteadores Wi-Fi 6, reduzindo drasticamente o OPEX para o provedor vencedor através do monitoramento remoto.</span>
        </p>
    </div>

    <script>
        // Lógica de Alternância de Idioma
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

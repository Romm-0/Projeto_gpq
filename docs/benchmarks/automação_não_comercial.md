# Automação de baixo custo, sem controladores comerciais, mas de alto desempenho

Com base nos benchmarks dos produtos os valores registrados podem desencorajar os pequenos produtores ou até médio produtores que nunca testaram automações antes por acharem que os valores são muito altos e o ROI é baixo. 

Com base nisso e em alguns artigos científicos nos iremos propor uma forma de automatizar usando single board computers (SBCs) ou relacionados e censores de baixo custo para lidar com o controle. A parte de ventilação, alimentação e silagem não tem uma economia considerável caso use produtos não industriais com base nas faixas de orçamento definidas no escopo do projeto.

---

## Controladores

O controlador deve ser uma sbc com poder computacional e opções de conectividade para conseguir suprir a demanda computacional de controlar um sistema autônomo. Com base nos artigos lidos um raspberry pi 4 ou superior se mostra capaz de servir como um controlador, a partir disso daremos opções semelhantes a ele em performance e superior a ele.

### Centrais

- [raspberry pi 4 - 8gb ram](https://pt.aliexpress.com/item/4000054878108.html?spm=a2g0o.productlist.main.1.3d2634b4Nxh0mT&algo_pvid=51ba6ea0-b8ce-4277-8079-bf2d61bd21ac&algo_exp_id=51ba6ea0-b8ce-4277-8079-bf2d61bd21ac-0&pdp_ext_f=%7B%22order%22%3A%22214%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%211014.13%21437.20%21%21%21175.44%2175.63%21%402101d49617635044796785606ea2f3%2112000028935457395%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756988&curPageLogUid=OyzMFdAh8TTd&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A4000054878108%7C_p_origin_prod%3A), valor aproximado na última checagem: R$ 900

	- Oferece menos poder computacional do que as suas concorrentes, mas uma comunidade mais ampla e bem desenvolvida tornando o desenvolvimento mais fácil

	- Em geral tem a maior gama de conectividade com sensores sem precisar de muitas configurações

	- Consegue ser um controlador central com conectividade wifi e ethernet

	- Valor na última checagem muito próximo ao de sua concorrente de marca (raspberry pi 5)

- [raspberry pi 5 - 8gb ram](https://pt.aliexpress.com/item/1005008041405153.html?spm=a2g0o.productlist.main.4.4c3f4d89MVfFwd&aem_p4p_detail=202511181423235614109670476680000211405&algo_pvid=257dbd26-5c88-406b-ae0d-4c2ebe969aee&algo_exp_id=257dbd26-5c88-406b-ae0d-4c2ebe969aee-3&pdp_ext_f=%7B%22order%22%3A%22396%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21580.03%21569.03%21%21%21713.36%21699.83%21%402101e83017635046033658036ea28e%2112000045465340993%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756890&curPageLogUid=IPSQCHQS0leD&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008041405153%7C_p_origin_prod%3A&search_p4p_id=202511181423235614109670476680000211405_1), valor aproximado na última checagem: R$ 1000

	- Oferece menos poder computacional do que as suas concorrentes, mas uma comunidade mais ampla e bem desenvolvida tornando o desenvolvimento mais fácil

	- Em geral tem a maior gama de conectividade com sensores sem precisar de muitas configurações

	- Consegue ser um controlador central com conectividade wifi e ethernet

	- Valor pouco maior que a sua antecessora, mas maior poder computacional

- [orange pi 4 pro - 8gb ram](https://pt.aliexpress.com/item/1005010218258516.html?spm=a2g0o.productlist.main.4.25c01644WS7v3F&algo_pvid=5f05955b-de2a-4f47-9c81-ed74c09d7fc1&algo_exp_id=5f05955b-de2a-4f47-9c81-ed74c09d7fc1-3&pdp_ext_f=%7B%22order%22%3A%2220%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21436.95%21401.99%21%21%21537.39%21494.39%21%402101c59117635048674224957e5842%2112000051563135855%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895&curPageLogUid=ZLnTpQTnMmfO&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005010218258516%7C_p_origin_prod%3A), valor aproximado na última checagem: R$650

	- Consegue ser um controlador central com conectividade wifi e ethernet

	- Poder computacional maior do que a raspberry pi 5

	- Comunidade menor e as vezes com problemas de conectividade com sensores out of the box

- [orange pi 5 pro - 16gb ram](https://pt.aliexpress.com/item/1005006800863351.html?spm=a2g0o.productlist.main.2.34eb7c1djaqQTA&algo_pvid=779a1d98-8a1c-4677-89ee-d1fdfdbae17e&algo_exp_id=779a1d98-8a1c-4677-89ee-d1fdfdbae17e-1&pdp_ext_f=%7B%22order%22%3A%2254%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%211138.64%21790.07%21%21%21196.98%21136.68%21%402101e83017635047089253325ea2cb%2112000038350469212%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756976&curPageLogUid=8IdK1GtyZHQr&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005006800863351%7C_p_origin_prod%3A), valor aproximado na última checagem: R$1500

	- Consegue ser um controlador central com conectividade wifi e ethernet

	- Mais poder computacional do que a sua antecessora, melhorando a estabilidade e dando uma margem para sistemas mais complexos

	- Capacidade de hospedar um site para controle do galpão

	- Comunidade menor e as vezes com problemas de conectividade com sensores out of the box

- [radxa x4 - 8gb ram](https://pt.aliexpress.com/item/1005008424476103.html?spm=a2g0o.productlist.main.7.6c05JuwpJuwpAM&algo_pvid=0ca73e00-b62b-43f6-8b3c-b0801ed97e67&algo_exp_id=0ca73e00-b62b-43f6-8b3c-b0801ed97e67-6&pdp_ext_f=%7B%22order%22%3A%2225%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21141.27%21133.27%21%21%21173.74%21163.90%21%402101c44f17635050331723225ef64b%2112000045014108886%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756981&curPageLogUid=8uR6Te9WVZwE&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008424476103%7C_p_origin_prod%3A), valor aproximado na última checagem: R$1500

	- Alto poder computacional e processador x86, pode ter programas que lidem melhor com essa arquitetura do que a ARM (todas as outras SBCs dessa lista)

	- Capacidade de hospedar um site para controle do galpão

	- Consegue ser um controlador central com conectividade wifi e ethernet

	- Comunidade menor e as vezes com problemas de conectividade com sensores out of the box

	- Maior consumo energético do que as outras, mesmo que a média seja de 5w a 10w em baixas cargas de trabalho

- [radxa rock 5 itx - 8gb ram](https://pt.aliexpress.com/item/1005008131571862.html?spm=a2g0o.productlist.main.5.6c05JuwpJuwpAM&algo_pvid=0ca73e00-b62b-43f6-8b3c-b0801ed97e67&algo_exp_id=0ca73e00-b62b-43f6-8b3c-b0801ed97e67-4&pdp_ext_f=%7B%22order%22%3A%2297%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21705.62%21697.62%21%21%21867.82%21857.98%21%402101c44f17635050331723225ef64b%2112000043914068206%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756981&curPageLogUid=xwmCs0wA2gBD&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008131571862%7C_p_origin_prod%3A), valor aproximado na última checagem: R$1300

	- A com maior poder computacional da lista, abre portas para aguentar todo o sistema e conectividade via web com site rodando localmente (talvez a versão de 16gb lide melhor com o site)

	- Comunidade menor e as vezes com problemas de conectividade com sensores out of the box

- [radxa zero 3w - 2gb](https://pt.aliexpress.com/item/1005007614734251.html?spm=a2g0o.productlist.main.1.6c05JuwpJuwpAM&algo_pvid=0ca73e00-b62b-43f6-8b3c-b0801ed97e67&algo_exp_id=0ca73e00-b62b-43f6-8b3c-b0801ed97e67-0&pdp_ext_f=%7B%22order%22%3A%22558%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%2195.56%2192.56%21%21%21117.53%21113.84%21%402101c44f17635050331723225ef64b%2112000041507910625%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756938&curPageLogUid=3umEurVj5Jxr&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007614734251%7C_p_origin_prod%3A), valor aproximado na última checagem: R$250

	- Baixo custo e poder computacional reduzido em comparação as outras, mas pode ser usada para automatizar pequenos sistemas como só ventilação ou só alimentação

### Periféricos

- [ESP32](https://www.aliexpress.com/item/1005006456519790.html), valor aproximado na última checagem: R$15

	- Valor mínimo, possibilita automações pontuais com conexão a um controlador central ou até mesmo sem, um exemplo seria automação de um sensor de temperatura, um alimentador

	- Possibilita a criação de um sistema wireless, um controlador central e diversos desses diretamente ligados as coisas a serem automatizadas

- [raspberry pi pico w](https://pt.aliexpress.com/item/1005008714908011.html?spm=a2g0o.productlist.main.1.6b0786c0roIxCn&algo_pvid=cc00e317-f6ca-4c08-ab25-2b15fba9113f&algo_exp_id=cc00e317-f6ca-4c08-ab25-2b15fba9113f-0&pdp_ext_f=%7B%22order%22%3A%221207%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%2135.91%216.99%21%21%2144.17%218.60%21%402101e81117635088937958623e854a%2112000046359830440%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756908&curPageLogUid=cQB4nn5IeFf4&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008714908011%7C_p_origin_prod%3A), valor aproximado na última checagem: R$10

	- Mesma utilidade do ESP32, menos recursos, mas na plataforma raspberry

---

## Conexão wifi

Seguindo a lógica de fazer todo o sistema, iremos sugerir algumas SBCs capazes de fazer o controle da rede local, mas isso facilmente pode ser substituído por um roteador ou ethernet cabeada.

- [orange pi rv2 - 2gb ram](https://pt.aliexpress.com/item/1005008678300684.html?spm=a2g0o.productlist.main.1.57395169PdLT82&algo_pvid=b23dcdd3-cab0-4ff7-a481-1e6729071fd7&algo_exp_id=b23dcdd3-cab0-4ff7-a481-1e6729071fd7-0&pdp_ext_f=%7B%22order%22%3A%2298%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21552.62%21266.31%21%21%2195.60%2146.07%21%402101eee917635065605752559e893a%2112000046206301977%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756878&curPageLogUid=KFXpsDQCaPIC&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008678300684%7C_p_origin_prod%3A), valor aproximado na última checagem: R$450

	- Placa voltada para redes, mas com capacidade de uso geral

	- Boa capacidade para fazer o controle de uma rede local e proteção para host do sistema para a web (controle a longa distância)

	- Versões com maior ram podem fazer o host do site

- [orange pi r2s - 1gb](https://pt.aliexpress.com/item/1005008678300684.html?spm=a2g0o.productlist.main.2.233178bfhjahm6&algo_pvid=158f91ea-ffb5-4857-915d-3fa3ad54b98e&algo_exp_id=158f91ea-ffb5-4857-915d-3fa3ad54b98e-1&pdp_ext_f=%7B%22order%22%3A%2298%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21552.62%21266.31%21%21%2195.60%2146.07%21%402103128917635068297756236e1a57%2112000046206301977%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756878&curPageLogUid=WaBDpRZGRTni&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005008678300684%7C_p_origin_prod%3A), valor aproximado na última checagem: R$380

	- Placa voltada totalmente para redes, múltiplas portas capazes de conectar todo o sistema de um galpão

	- Uso muito limitado a redes

---

## Sensores

Além dos citados no benchmark que ainda podem ser usados, existe a opção de usar outros controladores voltados a SBCs ou projetos de eletrônica, mesmo que sejam menos precisos em média, possuem um custo menor do que os sensores comerciais e são muito úteis para automações que buscam o menor gasto possível, mas ainda com qualidade.

 - [MQ-135 - CO2](https://pt.aliexpress.com/item/1005007138549841.html?spm=a2g0o.productlist.main.1.28efMqgjMqgjuO&algo_pvid=ff78af8a-8369-428a-85fe-0f81e52b0cbd&algo_exp_id=ff78af8a-8369-428a-85fe-0f81e52b0cbd-0&pdp_ext_f=%7B%22order%22%3A%22672%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%2110.93%216.99%21%21%2113.44%218.59%21%402103126e17635074913213825e41c1%2112000039541362028%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756908&curPageLogUid=YKAfy3CpHjXh&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007138549841%7C_p_origin_prod%3A), valor aproximado na última checagem: R$10

	- Valor muito mais baixo do que sensores comerciais com boa precisão, mas baixa área de detecção

	- Saída analógica

- [MH-Z19B - CO2](https://pt.aliexpress.com/item/1005007500137591.html?spm=a2g0o.productlist.main.1.6d1fVtdiVtdidQ&algo_pvid=4fd6427a-2b31-4844-9a45-dd244b5df24c&algo_exp_id=4fd6427a-2b31-4844-9a45-dd244b5df24c-0&pdp_ext_f=%7B%22order%22%3A%2243%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21112.87%21105.87%21%21%21138.82%21130.21%21%402103128817635082683961714ee009%2112000041037871679%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895%3BpisId%3A5000000187756976&curPageLogUid=qZylE2faA6PF&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007500137591%7C_p_origin_prod%3A), valor aproximado na última checagem: R$130

	- Maior precisão e maior área de atuação, para orçamentos maiores ele substitui o sensor acima

	- Saída analógica

 - [MQ-137 - NH3](https://pt.aliexpress.com/item/1005009441093029.html?spm=a2g0o.productlist.main.1.5d576d1ajBSBQ6&algo_pvid=7b3d20f1-dfcf-4d99-9150-60de31f2b2da&algo_exp_id=7b3d20f1-dfcf-4d99-9150-60de31f2b2da-0&pdp_ext_f=%7B%22order%22%3A%225%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%21201.32%2190.60%21%21%21247.59%21111.42%21%402103129f17635075352606306e9e00%2112000049107873761%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895&curPageLogUid=zhw5fCS163Lj&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009441093029%7C_p_origin_prod%3A), valor aproximado na última checagem: R$130

	- Baixa área de detecção, mas boa precisão

	- Saída analógica

- [DS18B20 - temperatura](https://pt.aliexpress.com/item/1005007908839006.html?spm=a2g0o.productlist.main.4.517e5763QmOecB&aem_p4p_detail=20251118151849156218735850820000243119&algo_pvid=5efeb455-22db-46b7-bdf6-d930960c10b1&algo_exp_id=5efeb455-22db-46b7-bdf6-d930960c10b1-3&pdp_ext_f=%7B%22order%22%3A%22149%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21BRL%215.82%214.95%21%21%217.16%216.09%21%402103129017635079294925908e1a50%2112000042797436754%21sea%21BR%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aab591c7b%3Bm03_new_user%3A-29895&curPageLogUid=pawPhetKRmtX&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007908839006%7C_p_origin_prod%3A&search_p4p_id=20251118151849156218735850820000243119_1), valor aproximado na última checagem: R$7

	- Precisa de múltiplos desse espalhados pelo galpão para uma medição mais precisa, área de atuação baixa

	- Considerar valor adicional para fiação

	- Saída analógica

---

## Conclusão

Com isso, por meio de um projeto de integração de software e a instalação do hardware é possível automatizar um galpão com um valor muito abaixo do que comprando controladores e sensores de mercado e com um gasto energético mínimo e rede local, conseguindo evitar a falta de conexão e de energia, já que uma bateria industrial pequena será capaz de manter o sistema por alguns dias, tornando mais acessível para o pequeno produtor a automatização da sua produção avícola.

## Fontes

Todas são pesquisas recentes dos últimos três anos para não correr risco de usar hardware muito desatualizado.

- A. Vijay, T. Garg, V. Goyal, Rashmi, A. Yadav and R. Mukherjee, "A Low-Cost Edge-IoT Based Smart Poultry Farm," 2023 15th International Conference on COMmunication Systems & NETworkS (COMSNETS), Bangalore, India, 2023, pp. 397-399, doi: 10.1109/COMSNETS56262.2023.10041317.

- M. G. M. Johar, A. I. Hajamydeen, L. Raya and K. C. Fui, "Automated Poultry Nutrition and Hydration Utilizing Raspberry Pi," 2024 IEEE International Conference on Agrosystem Engineering, Technology & Applications (AGRETA), Kuala Lumpur, Malaysia, 2024, pp. 204-208, doi: 10.1109/AGRETA61912.2024.10949016.

- M. G. M. Johar, A. I. Hajamydeen, L. Raya and K. C. Fui, "IoT-Powered Poultry Care: Optimizing Feeding and Watering with Raspberry Pi and ESP-8266," 2025 IEEE International Conference on Automatic Control and Intelligent Systems (I2CACIS), Kuala Lumpur, Malaysia, 2025, pp. 43-48, doi: 10.1109/I2CACIS65476.2025.11100815.

- K. K. V, M. C, P. P, S. T. B. V, J. M and R. P, "Raspberry PI-Based Real-Time Poultry Farm Feeder Tracking and Energy Management System," 2024 4th International Conference on Ubiquitous Computing and Intelligent Information Systems (ICUIS), Gobichettipalayam, India, 2024, pp. 1706-1711, doi: 10.1109/ICUIS64676.2024.10866577.

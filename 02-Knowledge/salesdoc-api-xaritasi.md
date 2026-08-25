---
type: knowledge
title: salesdoc-api-xaritasi
date: 2026-08-10
status: draft
verified: false
---

# SalesDoc — to'liq navbar/API xaritasi

2026-08-10: Ruslan qo'lda login qilgan Playwright brauzer sessiyasi orqali butun sidebar/navbar bitta JS so'rov bilan skanerlandi (barcha `<a href>` elementlari, DOM'da oldindan render qilingan — submenyularni ochish shart emas ekan). 130+ real yo'l topildi. To'liq ro'yxat quyida, bo'limlarga ajratilgan (rus tilidagi nomlar — SalesDoc interfeysi rus tilida).

## Hal qilingan ochiq muammolar

- **Agentlar ro'yxati** (`05-Errors/2026-08-07-salesdoc-agent-tuman-royxati-notoliq.md`): to'g'ri JSON manba — **`POST /staff/list/agent-paket`** (`GET /staff/list/agent` EMAS — u 404 beradi). Sahifa: `/staff/view/agent` ("Агенты Новый").
- **Planning/kunlik reja natijasi** (`05-Errors/2026-08-07-salesdoc-planning-daily-sub-endpoint-topilmadi.md`): `/planning/daily` degan sahifa yo'q ekan — to'g'ri sahifa **`/planning/monthly2`** ("Результаты выполнения плана"). Asosiy ma'lumot: `GET /planning/monthly2/data?year=YYYY&month=M&date_type=date_load&supervayzer=&category=&useReturns=n`. Qo'shimcha sub-endpointlar (bir xil query bilan): `/planning/monthly2/workingDays`, `/planning/monthly2/pulse`, `/planning/monthly2/diagram`, `/planning/monthly2/supervayzer`, `/planning/monthly2/productCategory`.

## Дашборд (top nav)
/dashboard/supervayzer, /dashboard/sales, /dashboard/finans, /dashboard/billing, /dashboard/kassaIncome, /dashboard/dolg, /dashboard/kpi, /dashboard/kpi?superviser=y, /dashboard/kpiExpeditor, /dashboard/kpiExpeditor/results, /dashboard/notification/list

## Планы
/planning/monthly2 (Результаты), /planning/outlet (Outlet targeting), /planning (Установка планов), /stock/planProduct/create, /stock/planProduct

## Заявки
/orders/list (Новый), /orders/orders (версия 1), /orders/view/createOrder, /orders/createOrder, /orders/recoveryOrder/create, /orders/rejects, /orders/recoveryOrder/createReplace, /onlineOrder/order, /orders/view/onMap, /orders/orders/editStatus, /vs/order (Van Selling), /orders/importOrder, /vs/view/return, /orders/importOrder/returns

## Склад
/warehouse/list, /stock/stock/detail, /warehouse/view/listPurchase, /stock/report, /stock/excretion, /stock/stockReport/pivotDetail, /warehouse/view/listAdjustment, /stock/purchaseReport/dailyRemainder, /warehouse/view/exchangeList, /stock/purchaseReport, /stock/purchase/refund, /stock/purchaseReportPivot, /stock/storeCorrector/fileImport, /stock/purchaseReport/profit, /store/materialReport, /stock/financialReport, /stock/lotReport, /warehouse/view/purchaseDraft, /orders/supplier/receipt, /stock/purchase/refund?movement=1, /warehouse/view/filialMovement

## Маркировка
/markirovka/view/incomingInvoices, /markirovka/view/outgoingInvoices

## Клиенты
/clients/client, /gps2 (Клиенты на карте), /clients/agentRoute, /clients/view/clientMap, /inventory/list (Оборудования), /clients/stock, /clients/client/duplicate, /onlineOrder/contact, /clients/taradoc, /integration/view/idokon, /sms/view/list

## Команда
/staff/view/agent, /staff/view/supervisor, /staff/view/expeditor, /team/auditor, /dashboard/kpi, /agents/kpiNew, /dashboard/kpi?superviser=y, /agents/kpiNew/superviser, /dashboard/kpiExpeditor/results, /dashboard/kpiExpeditor, /agents/limit, /agents/taskNew

## Аудит
/audit/dashboard/daily, /audit/audits, /audit/facing, /audit/sku, /audit/price, /audit/pollResult (Мерчандайзинг/Опрос), /audit/storecheck, /audit/settings, /audit/photoReport

## Отчеты (30+)
/report/agent, /report/customer, /report/customer/minimum, /report/customer/clientList, /report/volumeReport, /report/report/type, /report/volumeReport/version2, /report/expeditor, /report/defect, /report/expeditorReport, /report/export, /clients/Inventorization, /report/photoReport, /report/tasksReport, /report/feedbackReport, /report/RlpReport, /report/bonusReport, /report/bonusAccumulation, /report/agent/visit, /report/report, /report/reportVisit, /report/workingTime, /report/price, /clients/taradoc, /report/reportBuilder, /report/client/classification, /report/planExpeditor/index, /report/expeditorDefect, /report/bonus, /report/visit, /report/saleDetail?type=discount, /report/saleDetail, /report/discountDetail, /report/rfm, /report/vanselDailyReport, /report/expeditorDebt, /report/analyze

## Финансы
/clients/finans, /clients/finans/revise2, /clients/finans/clientPayment, /clients/finans/report, /dashboard/dolg, /clients/finans/initialBalans, /dashboard/kassaIncome, /clients/transactions, /clients/computation, /clients/transactionPivot, /clients/view/clientDebtByShipment, /clients/shipper, /clients/shipperFinans, /clients/shipperFinans/report, /clients/shipperFinans/revise, /clients/shipperFinans/initialBalans, /finans/consumption, /clients/finans/cashboxBalans, /finans/consumption/report, /clients/finans/cashbox, /finans/consumption/category, /finans/consumption/credit, /payment/approval, /clients/finans/deliver, /clients/finans/deliver?type=agent, /finans/pnl, /finans/paymentTransfer

## GPS
/gps/monitoring, /gps2/monitoring

## Настройки
/settings/diler, /access/frontend/permissionUsers (Контроль доступа), /api/apiLog/index (Журнал интеграции)

## Eslatma
Bu — sahifalarning HTML/frontend yo'llari (navbar link'lari), API sub-endpoint emas. Quyida har bir bo'lim tasdiqlangandan keyin haqiqiy JSON sub-endpointlar shu yerga qo'shib boriladi (progress: Отчеты — 36/36, Склад — 17/20, Клиенты — 9/11, Команда — 7/12, Аудит — 6/9, GPS — 2/2, Настройки — 3/3, Маркировка — 2/2, Финансы — 9/27, Заявки — 1/14 (qisman), Дашборд/Планы — tekshirilmagan qoldi).

## Tasdiqlangan sub-endpointlar — GPS (2026-08-10, 2/2 sahifa tekshirildi)

- /gps/monitoring → GET /gps/backend/last?c_datetime=YYYY-MM-DD HH:MM:SS (real vaqtda GPS pozitsiyalari), GET /gps/get/getSuperviser
- /gps2/monitoring → GET /gps2/monitoring/fetchData?date=YYYY-MM-DD HH:MM:SS, GET /gps2/monitoring/fetchSupervayzers

## Tasdiqlangan sub-endpointlar — Настройки (2026-08-10, 3/3 sahifa tekshirildi)

- /access/frontend/permissionUsers → GET /access/backend/users (diqqat: /js/translations/ru/access.json 404 beradi, lekin ma'lumot baribir ishlaydi)
- /api/apiLog/index → GET /api/apiLog/getFolders
- /settings/diler → klassik HTML, JSON topilmadi

## Tasdiqlangan sub-endpointlar — Маркировка (2026-08-10, 2/2 sahifa tekshirildi)

- /markirovka/view/incomingInvoices → GET /markirovka/api/incoming-invoices?from=&to= (ISO datetime)
- /markirovka/view/outgoingInvoices → GET /markirovka/api/outgoing-invoices?from=&to=&by=date_load

## Tasdiqlangan sub-endpointlar — Финансы (2026-08-10, 9/27 sahifa tekshirildi, QISMAN — vaqt tugadi)

- /finans/paymentTransfer → GET /finans/paymentTransfer/getData?from=&to=, GET getCashbox, GET getCashbox?balance=true
- /payment/approval → GET /payment/approval/getData?from=&to=, GET getAccesses
- /clients/finans → GET /clients/finans/AjaxIndex?summa_from=&summa_to=&payment_type=&datestart=&endstart=&by_date=DATE&... (DataTables); shu sahifada yana /orders/invoice/nds, /orders/invoice/diler ham chaqiriladi
- /clients/transactions → GET /clients/transactions/JsonData?active=Y&access=Y
- /clients/view/clientDebtByShipment → GET /clients/computation/debtApi?page=&limit=&sort=&order=&date_from=&date_to=

Klassik/JSON topilmagan (bu safar): /finans/pnl, /finans/consumption, /clients/finans/cashbox, /dashboard/dolg, /clients/shipper.

**Sinalmagan qoldi (18 ta, keyingi bosqichda davom ettirish kerak):** /clients/finans/revise2, /clients/finans/clientPayment, /clients/finans/report, /clients/finans/initialBalans, /dashboard/kassaIncome, /clients/computation, /clients/transactionPivot, /clients/shipperFinans, /clients/shipperFinans/report, /clients/shipperFinans/revise, /clients/shipperFinans/initialBalans, /clients/finans/cashboxBalans, /finans/consumption/report, /finans/consumption/category, /finans/consumption/credit, /clients/finans/deliver, /clients/finans/deliver?type=agent, /finans/pnl (qayta, filtr bilan).

## Tasdiqlangan sub-endpointlar — Заявки (2026-08-10, 1/14 sahifa tekshirildi, QISMAN — vaqt tugadi)

- /orders/list → asosiy ma'lumot avvaldan ma'lum /orders/list/orders orqali (bu safar buyurtmalar ro'yxati bo'sh bo'lgani uchun chaqiruv ushlanmadi); shu sahifada /orders/list/getAccesses, /invoiceTemplate/list?group=orders.list, /invoiceTemplate/repository ham topildi.

**Sinalmagan qoldi (13 ta):** /orders/orders, /orders/view/createOrder, /orders/createOrder, /orders/recoveryOrder/create, /orders/rejects, /orders/recoveryOrder/createReplace, /onlineOrder/order, /orders/view/onMap, /orders/orders/editStatus, /vs/order, /orders/importOrder, /vs/view/return, /orders/importOrder/returns.

**Butunlay sinalmagan bo'limlar:** Дашборд (top nav, 11 ta yo'l — bulardan /dashboard/supervayzer, /dashboard/sales, /dashboard/finans allaqachon avvalgi sessiyalarda ma'lum edi, lekin bu safar network orqali qayta tasdiqlanmadi), Планы (5 ta yo'ldan faqat /planning/monthly2 tasdiqlangan, qolgan 4 tasi — /planning/outlet, /planning, /stock/planProduct/create, /stock/planProduct — sinalmagan).

## Tasdiqlangan sub-endpointlar — Команда (2026-08-10, 7/12 sahifa tekshirildi)

- /staff/view/expeditor → POST /staff/list/expeditor-paket (agent-paket bilan bir xil pattern: /staff/list/{role}-paket)
- /dashboard/kpiExpeditor → GET /dashboard/kpiExpeditor/getInstalled
- /agents/taskNew → GET /agents/taskNew/getData?date_from=&date_to=&date_type=DATE_CREATE

**MUAMMO topildi:** /staff/view/supervisor sahifasida JS xatosi — `vue-demi.min.js` **404** qaytaradi, shu sabab Vue ilova ishga tushmayapti, ma'lumot yuklanmaydi (buzilgan sahifa, IT'ga xabar berish kerak bo'lishi mumkin). Pattern bo'yicha to'g'ri endpoint `/staff/list/supervisor-paket` bo'lishi kerak edi (agent/expeditor pattern asosida), lekin frontend xatosi tufayli chaqirilmayapti.
**MUAMMO topildi:** /team/auditor sahifasida `/js/translations/ru/team.json` **404** qaytaradi, JSON ma'lumot endpointi umuman chaqirilmadi.

Klassik/hali JSON topilmagan: /dashboard/kpi, /dashboard/kpi?superviser=y, /agents/kpiNew, /agents/kpiNew/superviser, /dashboard/kpiExpeditor/results, /agents/limit (barchasi filtr/interaktsiya kerak bo'lishi mumkin).

## Tasdiqlangan sub-endpointlar — Аудит (2026-08-10, 6/9 sahifa tekshirildi)

Sinalgan sahifalar (dashboard/daily, audits, facing, sku, price, storecheck) — hech biri sahifa yuklanganda avtomatik JSON/XHR chaqirmadi, hammasi klassik ko'rinishda, lekin filtr/sana tanlab "Показать" bosilganda ma'lumot yuklanishi mumkin (bu safar tugmalar bosilmadi — vaqt tanqisligi). Sinalmagan qoldi: /audit/pollResult, /audit/settings, /audit/photoReport.

## Tasdiqlangan sub-endpointlar — Клиенты (2026-08-10, 9/11 sahifa tekshirildi)

- /clients/client → POST /clients/client/JasonData2/?pageUrl=/clients/client/&active=Y
- /clients/agentRoute → POST /clients/agentRoute/getClients
- /clients/view/clientMap → GET /clients/api/getAgentVisitsOnMap?ids=
- /inventory/list → GET /inventory/list/data
- /clients/stock → GET /clients/stock/AjaxIndex2?type=product|category&... (DataTables format)
- /onlineOrder/contact → POST /onlineOrder/contact/filter
- /integration/view/idokon → GET /integration/list/idokon-incoming-requests
- /sms/view/list → GET /sms/message/list?from_date=&to_date=, /sms/message/balance, /sms/message/checking/

Sinalgan, JSON topilmadi: /clients/client/duplicate (forma sahifasi, ehtimol qidiruv kiritilgach so'rov yuboradi). Sinalmagan qoldi: /gps2 (Клиенты на карте — /gps2/monitoring bilan bir xil bo'lishi mumkin, GPS bo'limida tekshiriladi).

## Tasdiqlangan sub-endpointlar — Склад (2026-08-10, 17/20 sahifa tekshirildi)

- /warehouse/list → GET /warehouse/list/data (avvaldan ma'lum, qayta tasdiqlandi)
- /warehouse/view/listPurchase → GET /warehouse/list/purchase?from=&to=&by=date
- /stock/stockReport/pivotDetail → GET /stock/stockReport/pivotData, GET /stock/stockReport/reportTemplates
- /warehouse/view/listAdjustment → GET /warehouse/api/list-adjustments?by=create_date&from=&to=
- /warehouse/view/exchangeList → GET /warehouse/exchange/list?from_date=&to_date= (detail: /warehouse/exchange/view?id=)
- /stock/purchaseReportPivot → GET reports?type=false, POST pivotData?date=
- /store/materialReport → GET /store/materialReport/data?start_date=&end_date=&warehouses=
- /stock/financialReport → GET /stock/financialReport/getJson?id=total
- /stock/lotReport → GET /stock/lotReport/data
- /warehouse/view/purchaseDraft → GET /warehouse/api/list-purchase-draft?dateFilterType=create_at&startDate=&endDate=
- /orders/supplier/receipt → POST /orders/orderState/orders, GET /orders/orderState/getMainFilials, /orders/orderState/movementFilials
- /warehouse/view/filialMovement → GET /warehouse/filialMovement/list-requests?direction=incoming&type=primary

Klassik HTML (JSON kerak emas): /stock/stock/detail, /stock/report, /stock/excretion, /stock/purchaseReport.

Sinalgan, JSON topilmadi (interaktsiya kerak bo'lishi mumkin): /stock/purchaseReport/dailyRemainder, /stock/purchase/refund, /stock/purchaseReport/profit. Sinalmagan qoldi: /stock/storeCorrector/fileImport (fayl import, ehtimol data-so'rov emas), /stock/purchase/refund?movement=1 (bazaviy /stock/purchase/refund bilan bir xil sahifa).

## Tasdiqlangan sub-endpointlar — Отчеты (2026-08-10, network orqali, 36/36 sahifa tekshirildi)

JSON/XHR endpoint topilganlar:
- /report/customer/minimum → POST /report/customer/getAkb, POST /report/customer/getOkb, POST /report/customer/getAgent
- /report/customer/clientList → GET /report/customer/clientListAjax?status[]=2&status[]=3&inventory=&active_client=&bydate=DATE_LOAD&datestart=&endstart=&last_days=15
- /report/report/type → GET /report/report/AjaxType
- /report/defect → GET /report/defect/getJson?id=total (WebDataRocks pivot)
- /report/expeditorReport → GET /report/expeditorReport/ajax?type=1&bydate=DATE
- /report/tasksReport → GET /report/tasksReport/pivotData?dateFrom=YYYY-MM-DD&dateTo=YYYY-MM-DD
- /report/feedbackReport → GET /report/feedbackReport/pivotData?dateFrom=&dateTo=, POST checkFeedbacks, GET getUsers
- /report/report → GET /report/report/AjaxReport
- /report/price → POST /report/price/getData
- /clients/taradoc → POST /clients/taradoc/getReport
- /report/planExpeditor/index → POST /report/planExpeditor/getData
- /report/expeditorDefect → GET reports, POST pivotData?date_load=YYYY-MM-DD,YYYY-MM-DD
- /report/bonus → GET /report/bonus/data?DATE_LOAD=YYYY-MM-DD,YYYY-MM-DD
- /report/visit → GET /report/visit/getjson
- /report/saleDetail (va ?type=discount) → GET reports?type=false, POST pivotData?date_load=
- /report/discountDetail → GET reports, GET pivotData?date=&status[]=1..5
- /report/rfm → POST /report/rfm/getData
- /report/vanselDailyReport → POST getDataVan
- /report/expeditorDebt → GET /report/expeditorDebt/list?from=&to=&bydate=date

Klassik server-rendered HTML (JSON kerak emas, get_dashboard_page HTML'ni to'g'ridan-to'g'ri parse qiladi): /report/agent, /report/customer, /report/volumeReport, /report/expeditor, /report/photoReport, /report/agent/visit, /report/workingTime, /report/client/classification.

Sinab ko'rilgan, lekin sahifa yuklanganda JSON chaqirmagan (ehtimol filtr/"Показать" tugmasini bosish yoki qo'shimcha interaktsiya kerak — hali aniqlanmagan): /report/volumeReport/version2, /report/export, /clients/Inventorization, /report/RlpReport, /report/bonusReport, /report/bonusAccumulation, /report/reportVisit, /report/reportBuilder, /report/analyze (40 ta console warning bilan — buzilgan/eski bo'lishi ham mumkin).

*<- [[hub|Xarita]]* · bog'liq: [[salesdoc-malumot-sxemasi]], [[salesdoc-agent-tuman-royxati-notoliq]], [[salesdoc-planning-daily-sub-endpoint-topilmadi]]

## 2026-08-25 - qo'shimcha
2026-08-25 QOSHIMCHA - agent_id -> ISM xaritasi qayerdan olinadi. Muammo: /payment/approval/getData faqat agent_id (d0_9x) beradi, ism yoq; POST /staff/list/agent-paket 11 ta agent qaytaradi lekin javobda FAQAT id bor (config_agents/limit_agents kalitlari), ISM MAYDONI YOQ. YECHIM: GET /gps2/monitoring/fetchData?date=YYYY-MM-DD HH:MM:SS javobida har yozuvda AGENT_ID va FIO birga keladi - shu bilan xarita tuziladi. 2026-08-25 holatiga: d0_4 Offis, d0_91 Angren & Oqqorgon, d0_92 Abdullaxojaev Boxodirxoja, d0_94 Athamov Faxriddin, d0_95 Sobirov Botirjon, d0_96 Murodullayev Shoxrux, d0_98 Muhammad Ali, d0_99 Djorayev Shuxratbek, d0_100 Yashnobod & Sergeli, d0_101 Muhammadjonov Muhtorjon, d0_103 Sobitov Abdurahmon. Osha javobda BATTERY, DATE (signal yoshi), GPS_STATUS, MODE ham bor - ertalabki holat uchun bitta chaqiruv yetadi. DIQQAT: /gps2/monitoring/fetchData ni PARAMETRSIZ chaqirish 500 xato beradi (CDbException) - date majburiy.

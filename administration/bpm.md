# Business Process Management
# Pagdumala sa Proseso sa Negosyo

Business Process Management (BPM) tool provides the ability to model and automate business processes in EspoCRM. It's an engine executing business processes described in BPMN 2.0 standard. BPM tool is available in [Advanced Pack](https://www.espocrm.com/extensions/advanced-pack/) extension.
Ang galamiton nga Pagdumala sa Proseso sa Negosyo (BPM) naghatag ug abilidad sa pagmodel ug awtimeyt sa mga proseso sa negosyo sa EspoCRM. Usa kini ka makina sa pagpatuman sa mga proseso sa negosyo nga gideskribir sa sukdanan sa BPMN 2.0. Ang galamiton nga BPM kay naa sa ekstensyon sa [Advanced Pack](https://www.espocrm.com/extensions/advanced-pack/).

![BPM example](../_static/images/administration/bpm/bpm-1.png)

### Difference from Workflows tool
### Kala-inan gikan sa galamitang mga Workflow

Workflows tool is intended for automation of simple business rules, w/o sequential flow items, when there is no need to display the flow graphically.
Ang galamitang mga workflow kay gilayon para sa pagpaawtomaik sa mga simple nga mga lagda sa pagnegosyo, wala'y mga aytem nga sunod sa agay-ay, kung wala kini nagkinahanglan ug pagdispley sa grapikal nga agay-ay.

BPM tool is intended for more complex business flows, where there can be diverging and converging flows, execution delays, user interactions. A flowchart view makes the business process more comprehensible for a human, a log allows to see how the process was held.
Ang galamitang BPM kay gilayon para sa mas komplikado nga agay-ay sa pagnegosyo, kung diin aduna'y mahimong mga agay-ay na managlain ug mga pareho, mga pagkadugay sa pagpatuman, ug mga interaksyon sa mga manggamitay. Ang pagpakita sa flowchart ang nagpahimo sa mga preseso sa pagnegosyo nga masabtan sa tawo, ang pagkalagda ang nagatugot sa pagkakita kung gi-unsa pagbuhat ang proseso.

## Process Flowcharts
## Ang mga Flowchart sa Proseso

The link to process flowcharts is available from administration panel. It also can be added as a tab on the navigation panel.
Ang link sa mga flowchart sa proseso kay makita gikan sa panel sa administrasyon. Pwede pud kini madugang isip usa ka tab sa panel sa nabigasyon.

Flowcharts are intended for business processes modeling. Administrator can create and edit flowcharts. Regular users can only view flowcharts.
Ang mga flowchart kay gilayon para sa pagmodelo sa mga proseso sa pagnegosyo. Ang tig-dumala kay pwedeng magbuhat ug mag-edit sa mga flowchart. Ang mga regular na manggamitay kay pwede lang makakita sa mga flowcharts.

Every flowchart has its specific entity type (Target Type field). The flowchart determines execution of future process instances. It comprises flowchart elements and connections between elements.
Kada flowchart kay adunay spesipik nga klase sa entity (Target Type field). Ang flowchart naghukom sa pagpatuman sa mga umaabot nga mga proseso nga mahitabo. 

If process flowchart has the unchecked 'Is Active' field then it won't initiate process instances.
Kung ang flowchart sa mga proseso kay naay unchecked nga field nga 'Is Active' mao nga dili siya makapasugod sa mahitabong proseso.

To show details and parameters of a certain flowchart element you need to click on it. In edit mode you will be able to edit parameters.
Para mapakita ang mga detalye ug parametro  sa usa ka maong elemento sa flowchart kinahanglan nimo ning i-klik. Sa moda nga edit ikaw kay mamahimong mo-edit sa mga parametro.

## Processes
## Mga Proseso

Processes are available from administration panel. The link also can be added as a tab on the navigation panel.
Ang mga proseso kay makita gikan sa panel sa administrasyon. Pwede pud kini madugang isip usa ka tab sa panel sa nabigasyon.

Process represents business process instance. When it's initiated it gets the status 'Started'. When process is finished it gets the status 'Ended'. The process can also be stopped manually by a user who has an access to edit the process. If it's stopped manually it gets status the 'Stopped'.
Ang proseso nagrepresentar sa mga preseso nga mahitabo sa negosyo. Kung kini kay nasugdan na naa kini'y status nga 'Started'. Kung ang proseso kay nahuman na naa kini'y status nga 'Ended'. Ang proseso kay mamahimo pud ihunong ug manu-mano sa user nga naay akses sa pag-edit sa proseso. Kung kini kay nahunong sa pama-aging manu-mano naa kini'y status nga 'Stopped'.

The process is executed according the flowchart. Flowchart of process can't be changed after process is started.
Ang proseso kay mapatuman matud sa flowchart. Ang flowchart sa proseso kay dili mamahimong usbon mahuman kini sugdan.

The process obligatorily is related to single target record.
Ang proseso kay obligadong naay relasyon sa usa ka target nga rekord.

Processes can be started automatically (upon specific conditions or by scheduling) or manually (where there is at least one Start Event in the flowchart). To start process manually the user needs to click 'Start Process' button on the list view of processes.
Ang mga proseso kay mamahimong sugdan sa pamaaging awtomatik (sa mga spesipik nga mga kondisyon o sa pagskedyul) o manu-mano (kung diin adunay usa ka Start Event sa flowchart). Para masugdan ang proseso sa pama-aging manu-mano ang manggamitay kay dapat nga i-klik ang 'Start Process' nga buton nga naa sa makitang listahan sa mga proseso.

## Flowchart Elements
## Mga Elemento sa Flowchart

### Events
### Mga Event

Events are displayed on a flowchart as circles.
Ang mga event kay nakadispley sa flowchart isip mga lingin.

#### Start Event
#### Start Event

Doesn't have parameters. It's a starting point of the process. Start Event can be initiated manually by a user who has an access to create processes. The user needs to click  'Start Process' button on the list view of processes.
Wala'y mga parametro. Kini ang punto sa pagsugod sa proseso. Ang Start Event kay mamahimong sugdan sa pamaaging manu-mano sa manggamitay nga adunay akses sa pagbuhat ug mga proseso. Ang manggamitay kay knahanglang i-klik ang 'Start Process' nga buton nga naa sa makitang listahan sa mga proseso.

#### Conditional Start Event
#### Conditional Start Event

A starting point of the process. It's supposed to be triggered automatically when specified conditions are met. There are two types of trigger: 'After record created', 'After record saved'.
Ang punto sa pagsugod sa proseso. Kini kay gituohang matrigger sa pamaaging awtomatik kung ang gibungat nga mga kondisyon kay makab-ot. Aduna'y duha ka klase ang trigger: 'After record created', 'After record saved'.

#### Timer Start Event
#### Timer Start Event

A starting point of the process. It initiates processes by scheduling. You need to specify the list report that returns records for initiating processes and scheduling in crontab notation.
Ang punto sa pagsugod sa proseso. Mamahimo niining sugdan ang mga proseso sa pag-iskedyul niini. kinahanglan nimo nga ibungat ang report sa listahan nga mag-uli ug mga rekord para sa pagsugod sa mga proseso ug pag-iskedyul sa notasyon sa crontab.

#### Conditional Intermediate Event
#### Conditional Intermediate Event

This event stops the flow until specified criteria is met.
Kini nga event ang magpahunong sa agay-ay hangtod ang gibungat nga kriterya kay makab-ot.

#### Timer Intermediate Event
#### Timer Intermediate Event

This event stops the flow and waits as long as is specified by event's parameters.
Kini nga event ang magpahunong sa agay-ay ug maghuwat hangtod kung mao kini ang gibungat sa mga parametro sa event.

For more complex timer settings you can utilize [formula](formula.md). Formula scripts should return Date-Time value (in UTC timezone). Once this time comes the flow will be proceeded to the next element.
Para sa mas komplikado nga mga gitakda sa orasan mamahimo nimong gamiton ang [formula](formula.md). Ang mga skrip sa mga pormula kay dapat nga magbalik ug Date-Time value (naka-UTC timezone). Sa oras nga maabot na kini nga oras ang agay-ay kay ipalahos sa sunod nga elemento.

By utilizing datetime\closest formula function it's possible to set the timer to a specific time in the future, e.g. the beginning of the next working day.  
Sa paggmit sa datetime\closest nga panksyon sa pormula posible kini nga magtakda sa orasan sa gibungat nga oras nga umaabot, e.g. ang sinugdanan sa sunod nga adlaw sa pagtrabaho.

#### End Event
#### End Event

Ends the current flow. It doesn't end flows running in parallel. When the flow reaches the end event and there is no anything running in parallel then process ends.
Magtapos sa agay-ay sa pagkakaron. Dili kini magtapos sa mga nagdagan nga agay-ay sa pareho. Kung ang agay-ay kay maka-abot sa end event ug wala na'y bisan unsang nagdagan sa pareho unya ra mahunong ang proseso.

#### Terminate End Event
#### Terminate End Event

Ends all flows. Process is subsequently ended.
Magtapos sa tanang agay-ay. Ang proseso kay sunod-sunod nga matapos.

### Gateways
### Mga Gateway

Gateways are displayed as diamonds.
Ang mga gateway kay gidisplay isip mga diyamante. 

#### Exclusive Gateway
#### Eksklusibong Gateway

Can diverge or converge flows.
Mamahimong magkapananglahi o magkadungan sa mga agay-ay.

In case of diverging it defines a single flow (path) that will be chosen according specified criteria. The first met condition determines the flow, next conditions are omitted. There is an ability to specify default flow. Default flow is chosen if there are no any met conditions. Default flow is marked with a slash sign.
Sa kaso sa pagpananglain kini kay giila isip usa ka agay-ay (subayanan) nga pilion matud sa mga gibungat nga kriterya. Ang una nga makab-ot nga kondisyon ang magdeterminar sa agay-ay, ang sunod nga mga kondisyon kay ilaktaw. Aduna'y abilidad sa pagbungat sa default nga agay-ay. Ang default nga agay-ay kay pilion kung wala'y nakab-ot nga mga kondisyon. Ang default nga agay-ay kay aduna'y tima-ilhan nga slash sign.

In case of converging it just directs the flow to the outgoing element. It doesn't get blocked after the flow come though, so parallel flows won't be merged into the single flow.
Sa kaso sa panagdungan gidirekta niini ang agay-ay sa mga elemento nga paggawas. Dili na kini mamahimong babagan human niini makasulod, mao nga ang pareho nga mga agay-ay kay gitipon nga mamahimong usa ka agay-ay.

![exclusive gateway divergent](../_static/images/administration/bpm/gateway-exclusive-divergent.png)

![exclusive gateway convergent](../_static/images/administration/bpm/gateway-exclusive-convergent.png)

#### Inclusive Gateway
#### Inklusibong Gateway

Can diverge or converge flows.
Mamahimong magpalahi o magpadungan sa mga agay-ay.

In case of diverging, it can direct to one or multiple parallel flows (paths), depending on accomplishment of criteria of each flow. Default flow is chosen if there are no any met conditions. Default flow is marked with a slash sign.
Sa kaso sa pagpananglahi, mamahimo niining idorekta sa usa o daghang pareho nga mga agay-ay (subayanan), nagdepende sa nakab-ot sa kriterya sa kada agay-ay. Ang default nga agay-ay kay pilion kung wala'y mga kondisyon nga nakab-ot. Ang default nga agay-ay kay aduna'y tima-ilhan nga slash sign. 

If there is a necessity to merge parallel flows produced by a diverging inclusive gateway you need to use a converging inclusive gateway. It will wait for all incoming flows and then continue to the outgoing element.
Kung aduna'y panginahanglan sa panaghiusa sa mga pareho nga mga agay-ay nga nabuhat sa pagpananglahi sa inklusibo nga gateway kinahanglan nimo mugamit ug pagpadungan nga inklusibong gateway. Maghuwat kini sa tanan nga umaabot nga mga agay-ay ug magpadayon sa elemento nga paggawas.

![inclusive gateway](../_static/images/administration/bpm/gateway-inclusive.png)

Note: Diverging and converging gateways must be balanced.
Pahibalo: Ang pagpananglahi ug pagpanagdungan nga mga gateway kay gikinahanglang balanse.

Note: If one of parallel flows has been ended for some reason then diverging gateway will never be processed. The process will be blocked. Avoid a flowchart design that can bring about such a situation.
Pahibalo: Kung ang usa sa mga pareho nga mga agay-ay kay natapos tungod sa mga pipila ka mga rason mao nga ang pagpananglahi nga gateway kay dili maproseso. Ang proseso kay mababagan. Likayan ang desinyo sa flowchart nga magresulta sa mao nga sitwasyon.

#### Parallel Gateway
#### Parallel Gateway

Can diverge or converge flows.
Mamahimong magpalahi o magpadungan sa mga agay-ay.

In case of diverging it splits flow into multiple parallel flows. There are no parameters for this gateway type.
Sa kaso sa pagpananglahi bungkagon niini ang agay-ay sa daghang pareho nga mga agay-ay. Walay mga parametro sa ing-ani nga klase sa gateway.

In case of converging it waits until all incoming flows come and then continues to the next outgoing element.
Sa kaso sa pagpanagdungan huwaton niini hangtod nga maabot ang tanan nga padulong nga mga agay-ay ug magpadayon sa sunod nga elemento nga paggawas.

![parallel gateway](../_static/images/administration/bpm/gateway-parallel.png)

Note: Diverging and converging gateways must be balanced.
Pahibalo: Ang pagpananglahi ug pagpanagdungan nga mga gateway kay gikinahanglang balanse.

Note: If one of parallel flows has been ended for some reason then diverging gateway will never be processed. The process will be blocked. Avoid a flowchart design that can bring about such a situation.
Pahibalo: Kung ang usa sa mga pareho nga mga agay-ay kay natapos tungod sa mga pipila ka mga rason mao nga ang pagpananglahi nga gateway kay dili maproseso. Ang proseso kay mababagan. Likayan ang desinyo sa flowchart nga magresulta sa mao nga sitwasyon.

#### Event Based Gateway
#### Event nga naga-Base sa Gateway

Can only diverge flows.
Mamahimong magpalahi sa mga agay-ay.

It stops the flow until any of outgoing events gets triggered. Triggered event determines the single flow. Other outgoing events get rejected.
Magpahunong sa agay-ay hangtod nga aduna'y usa sa mga umaabot nga mga event ang matrigger. Ang natrigger nga event ang magterminar sa usa ka agay-ay. Ang ubang paggawas nga mga event kay isalikway.

Only intermediate events can be on the other end of outgoing sequence flows.
Ang intermediate nga mga event lamang ang mamahimong naa sa pikas tumoy sa paggawas nga sunod nga agay-ay.

![event based gateway](../_static/images/administration/bpm/gateway-event-based.png)

### Activities
### Aktibidades

Activities are displayed as rounded rectangles.
Ang mga aktibidades kay gidispley isip mga gilingin nga rektanggulo.

#### Task
#### Tahas

Task can execute following the actions:
Ang tahas kay mamahimong magpatuman sa sunod nga mga aksyon:

* Create Record - creates new record of any entity type;
* Create Related Record - creates new record related to the target record;
* Update Target Record;
* Update Related Record - updates the record or records related to the target record;
* Update Created Record - updates specific field of any record created in the current process;
* Update Process Record - can be used to assign the process to specific user or team;
* Link to Another Record - links the target record with a specified record;
* Unlink from Another Record - unlinks the target record from the specified record;
* Apply Assignment Rule - assigns the target record, the process record or any record created by the process according to the specific rule;
* Create Notification - creates in-app notification for specific users;
* Make Followed - makes specific users follow the target record, the process record or any record created by the process;
* Run Service Action - runs custom service actions implemented by developers.

* Create Record - magbuhat ug mga bag-ong rekord sa bisan-unsa'ng klase sa entity;
* Create Related Record - magbuhat ug mga bag-ong rekord nga iglabot sa target nga rekord;
* Update Target Record;
* Update Related Record - mag-apdeyt sa rekord o magrekord sa mga iglabot sa target nga rekord;
* Update Created Record - mag-apdeyt sa ispesipik nga field sa bisan-unsa'ng rekord nga nabuhat sa pagkakaron nga proseso;
* Update Process Record - mamahimong gamiton sa pagtakda sa proseso sa spesipik nga mugamit o bahan;
* Link to Another Record - maglink sa target rekord sa gibungat nga rekord;
* Unlink from Another Record - mag-unlink sa target rekord gikan sa gibungat nga rekord;
* Apply Assignment Rule - nagtakda sa target rekord, ang rekord sa proseso o bisan unsa nga rekord nga nabuhat sa proseso matud sa ispesipik nga lagda;
* Create Notification - magmugna ug notipikasyon nga in-app para sa mga ispesipik nga mga manggamitay;
* Make Followed - magpasunod sa mga ispesipik nga manggamitay sa target rekord, ang rekord sa proseso o bisan unsa nga rekord nga nabuhat sa proseso ;
* Run Service Action - magpadagan mga aksyon sa kustom nga serbisyo nga giimplementar sa mga nagpalambo niini.

Actions available for task are almost the same as in Workflow feature. See more details about [workflow's actions](workflows.md#actions).
Mga aksyon nga aduna para sa tahas kay halos pareha ra sa kagawian sa Workflow. Para sa mga dugang nga detalye mahitungod sa [workflow's actions](workflows.md#actions).

#### Send Message Task
#### Tahas sa Pagpadala ug Mensahe

Sends email message to specific recipient.
Magpadala ug mensahe nga email sa ispesipik nga magdadawat.

#### User Task
#### Tahas sa Mugamit

Provides a flexible ability of user interaction. It stops execution until the user (specified explicitly or by assignment rule) resolves the task. Process User Task record will be created in the system. By default there are three action types: Approve, Review, Accomplish.
Maghatag ug mausab-usab nga abilidad sa interaksyon sa mugamit. Magtapos sa pagsugod hangtod ang mugamit (gibungat nga tino o gitakda sa lagda) makaresolba sa tahas. Ang Process User Task rekord kay mabuhat sa sistema. Sa default aduna'y tulo ka klase nga aksyon: Approve, Review, Accomplish.

* Approve type requires the user to chose between 'Approved' and 'Declined'.
* Review type gives only one option: 'Reviewed'.
* Accomplish type has two options: 'Completed' and 'Failed'.
* Approve type nanginahanglan sa mugamit sa pagpili tali sa 'Approved' ug 'Declined'.
* Review type magahatag lamang ug usa ka opsyon: 'Reviewed'.
* Accomplish type kay aduna'y duha ka opsyon: 'Completed' ug 'Failed'.

The user assigned to the created Process User Task record will receive in-app notification. Administrator can also enable email notifications.
Ang mugamit nga natakda sa nabuhat sa rekord sa Process User Task kay makadawat ug in-app nga notipikasyon. Ang admintrador kay mamahimong magpagana sa mga notipikasyon sa email.

Users can also add Process User Tasks dashlet on their dashboard to see their actual process user tasks.
Ang mga mugamit kay mamahimo pud mudugang ug Process User Tasks nga dashlet sa ilahang dashboard paara makita ang ilang aktwal na proseso sa tahas sa naggamit.

It's possible to read the resolution of the passed user task within diverging gateways or conditional events, making ramification in the process flow.
Posible nga mabasa ang resolusyon sa napasa nga tahas sa mugamit gamit ang pagpananglahi nga mga gatewat o mga kondisyonal nga mga panghitabo, pagbuhat sa ramipikasyon sa sulod sa agay-ay sa proseso.

#### Script Task
#### Skrip sa Tahas

Executes the script in [espo-formula](formula.md) language. All set variables (`$variableName`) will be stored and available within the process.
Magpasugod sa skript sa [espo-formula](formula.md) nga lenggwahe. Ang tanan nga natakda nga mga baryabol (`$variableName`) kay matipigan ug pwedeng gamiton sa sulod sa proseso.

### Flows
### Mga Agay-ay

#### Sequence Flow
#### Sunod-sunod nga Agay-ay

Represented as a solid arrow. Indicates the order in which process elements will be executed.
Girepresentar isip usa ka solid nga pana. Nag-indikar sa kahan-ayan sa kung unsa nga mga elemento sa proseso ang sugdan.

## Conditions
## Mga kondisyon

Conditional events, exclusive and inclusive diverging gateways have conditions that determine the flow of the process.
Ang mga kondisyonal na panghitabo, ekslusibo ug inklusibo sa pagpananglahing mga gateway kay aduna'y mga kondisyon sa pagdeterminer sa agay-ay sa proseso.

Through UI there is an ability to check conditions for the following records:
Gamit ang UI aduna'y abilidad sa pagtsek sa mga kondisyon sa mga musunod nga mga rekord:

* Target record;
* Records related to the target through many-to-one and children-to-parent relationships;
* Records created by the process via tasks;
* User task records, which allows checking the resolution.
* Target rekord;
* Nagrekord sa mga iglabot target gamit ang daghan-sa-usa ug mga anak-to-ginikanan nga mga relasyon;
* Mga rekord nga nabuhat sa proseso gamit ang mga tahas;
* Mga rekord sa mga tahas sa mugamit, nagatugot sa pagtsek sa resolusyon.


It's also possible to define conditions in [Espo-formula](formula.md) language.
Posible usab ang pag-ila sa mga kondisyon sa [Espo-formula](formula.md) nga lengguwahe.

Conditions in BPM tool are the same as in Workflow feature. See more details about [workflow's conditions](workflows.md#conditions).
Mga kondisyon sa galamitan sa BPM kay pareha sa sama sa kagawian sa Workflow. Para sa mga dugang nga detalye mahitungod sa [workflow's conditions](workflows.md#conditions).

## Examples
## Mga Sampol

### Sampol 1

![Example 1](../_static/images/administration/bpm/example-1.png)

### Sampol 2

![Example 2](../_static/images/administration/bpm/example-2.png)

### Sampol 3

![Example 3](../_static/images/administration/bpm/example-3.png)

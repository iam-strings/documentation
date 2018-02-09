# Emails
# Mga Email

> Important. [Cron](https://github.com/espocrm/documentation/blob/master/administration/server-configuration.md#setup-a-crontab) should be configured in your system to make email fetching work. You can find the information in your EspoCRM at Administration > Scheduled Jobs.
>Importante. Ang [Cron](https://github.com/espocrm/documentation/blob/master/administration/server-configuration.md#setup-a-crontab) kay kinahanglang nakakonpigyur na sa imong sistema para mapagana ang paghatod-kuha sa email. Mahimong makit-an ang impormasyon sa imong EspoCRM sa Administration > Scheduled Jobs.

## Overview
## Katingbanan

Ang EspoCRM kay aduna'y abilidad sa pagbantay sa mga IMAP mailbox. Ang email kay mamahimong i-archive sa duha ka pamaagi: Grupo nga mga Email Account ug Personal nga mga Email Account. Ang Grupo nga mga Inbound Account kay gitagana para sa mga group mailbox: ang pinakakomon nga kaso kay ang support box. Ang Personal nga mga Email Account kay gitagana para sa personal nga mailbox sa manggamit niini.

As an email is coming the system tries to link it with the appropriate record (Accounts, Lead, Opportunity, Case). Users who follow that record will receive notification about a new email in the system, even if they are not in To or CC.

Sa pagpadulong sa email suwayan sa sistema ang paglink niini sa tukmang rekord (mga Account, Lead, Oppurtunidad, Kaso). Ang mga manggamitay nga nisunod sa marong rekord kay makadawat ug notisya mahitungod sa bag-ong email sa sistema, bisan ug wala sila sa To o CC.

## Group Email Accounts
## Mga Grupo nga mga Email Account

Only administrator can setup Group Email Accounts. Group Email Accounts can be used for both receiving and sending emails. Sending emails from group accounts has been available since 4.9.0 version.

Ang administrador lang ang makatakda sa Grupo nga mga Email Account. Ang Grupo nga mga Email Account kay mamahimong gamiton sa pagpadala ug pagkuha sa mga email. Ang pagpadala sa mga email gikan sa grupo nga mga account kay mamahimong gamiton gikan pa sa 4.9.0 nga bersyon.

Teams field determines which teams incoming emails will be assigned to. 
Ang mga bahan nga field ang maghukom kung kang asa maasayin ang mga umaabot nga mga email sa bahan.

If the group email account has SMTP and it's checked as shared then an access will be controlled by Roles through Group Email Account permission. Teams field will be used if permission level is set to 'team'.
Kung ang grupo nga mga email account kay adunay SMTP ug natsek kini isip usa ka pamahin unya ang akses kay makontrol sa mga Papel pinaagi sa katugotan sa Grupo nga Email Account. Ang mga bahan nga field kay magamit kung ang lebel sa pagtugot kay nakatakda sa "bahan".

There is an ability to make the system send an auto-reply for incoming emails.
Adunay abilidad sa pagbuhat sa sistema sa pagpadala ug awtomatik nga tubag para sa mga umaabot na mga email.

## Email-to-Case
## Ang Email-padulong sa-Kaso

There is an option to make the system create cases from incoming group emails. 
This feature is intended for support teams. 
Cases can be distributed to users from a specified team according to these ways: 
`direct assignment`, `round-robin` and `less-busy`. 
Only the first email in the thread creates a new case. 
Every subsequent one will be linked to the existing case record and displayed in its Stream panel.
Aduna'y opsyon para mamahimo sa sistema ang paggama ug mga kaso gikan sa mga padulong nga grupo nga mga email.
Ang kini nga kagawian kay gitagana para sa suporta sa mga bahan.
Ang mga kaso kay mamahimong maapod-apod sa mga manggamitay gikan sa gibungat nga bahan nga matud niini nga mga pamaagi:
ang `direct assignment`, `round-robin` ug ang `less-busy`.
Ang una nga email lang sa listahan ang makagama ug bag-ong kaso.
Kada sunod na usa kay malink sa mga anaa na nga rekord sa kaso ug makita sa Stream panel niini.

When users want to send a reply to the customer they need to make sure that the case is selected as a parent of the email that is being sent. It will make the customer reply to the group email address rather than to the user’s own.
Kung ang manggamitay kay gustong magpadala ug usa ka tubag sa kustomer nga kinahanglan nila para masiguro nga ang kaso kay napili isip usa ka ginikanan sa email nga gipadala. Mamahimo niini ang pagtubag sa kustomer adto sa grupo nga email adres imbis na sa iyang kaugalingon.

## Personal Email Accounts
## Ang Personal na mga Email Account

Users can setup their own email accounts that need to be monitored. Emails > Top Right Dropdown Menu > Personal Email Accounts. Administrator also can manage users' email accounts.
Ang mga manggamitay kay mamahimong magtakda sa ilahang kaugalingong mga account na kinahanglang bantayan. Emails > Top Right Dropdown Menu > Personal Email Accounts. Ang adminitrador kay mamahimong magdumala usab sa mga email account sa mga manggamitay.

## Email Filters
## Mga Pilter sa Email

These allow the filtering of incoming emails according to specified criteria. E.g. if you don't want notification messages sent by some application to be imported to EspoCRM you can create filter to make EspoCRM skip them.
Nagatugot sa pagpilter sa mga umaabot nga mga email matud sa mga gibuangat nga kriterya. E.g. kung dili ka ganahan ug mga mensahe nga notisya nga gipadala sa usa ka aplikasyon na i-import sa EspoCRM mamahimo kang magbuhat ug pilter para malibkas kini sa EspoCRM.

Admin can create global filters, applied to all email accounts. Users can create filters for their own personal email account and for entire inbox.
Ang admin kay mamahimong magbuhat sa mga kinatibuk-ang pilter, nga gipangdapat sa tanang email account. Ang mga manggamitay kay mamahimong magbuhat ug ilang kaugalingong pilter para sa ilang personal na email account ug para sa tibuok nga inbox.

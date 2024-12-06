Reading Book Club


DataIntensive Application (créer un GitHub avec Markdown ) 


Chap-1 => Thématique abordée

=> Stratégie de Gestion de cache : 
      * https://aws.amazon.com/fr/builders-library/caching-challenges-and-strategies/?did=ba_card&trk=ba_card
      * https://docs.aws.amazon.com/whitepapers/latest/database-caching-strategies-using-redis/caching-patterns.html
      * https://newsletter.systemdesign.one/p/caching-patterns

=> Chaos engineering 
       * https://www.oreilly.com/library/view/chaos-engineering/9781617297755/
       * https://chaostoolkit.org/reference/usage/cli/

==> Redis as message queue
       * https://github.com/sonus21/rqueue

==> Protocol Database
      * https://github.com/jeroenrinzema/psql-wire
      * https://www.mongodb.com/docs/manual/reference/mongodb-wire-protocol/#:~:text=a%2Dservice%20offering.-,Introduction,a%20regular%20TCP%2FIP%20socket.
     *  https://github.com/bwaldvogel/mongo-java-server

==> Change Data capture
* https://debezium.io/documentation/reference/2.7/tutorial.html

Demo API Cache Patterns : 
 *  https://docs.aws.amazon.com/whitepapers/latest/database-caching-strategies-using-redis/caching-patterns.html
 * https://newsletter.systemdesign.one/p/caching-patterns
Technologies : Debezium, mongodb, Postgresql, invalidation du cache java spring-boot


Prochaine : haute disponibilité (troisième séance)
* https://www.asprom.com/technologie/smile.pdf
  * https://aws.amazon.com/fr/builders-library/caching-challenges-and-strategies/?did=ba_card&trk=ba_card


ii Reliability

https://www.ionos.fr/digitalguide/serveur/know-how/serveurs-racks/
https://medium.com/@dbclin/aws-and-elasticity-keeping-ahead-of-user-demand-7ca618013a69
https://www.manning.com/books/learn-amazon-web-services-in-a-month-of-lunches

Faille linux : https://www.wired.com/2012/07/leap-second-glitch-explained/

Elasticité. : 
https://medium.com/@dbclin/aws-and-elasticity-keeping-ahead-of-user-demand-7ca618013a69



Human Errors: 

Erreurs humaines
Les humains conçoivent et construisent des systèmes logiciels, et les opérateurs qui assurent le fonctionnement des systèmes sont également humains. Même lorsqu'ils ont les meilleures intentions, les humains sont connus pour être peu fiables. Par exemple, une étude sur les grands services Internet a révélé que les erreurs de configuration des opérateurs étaient la principale cause des pannes, alors que les pannes matérielles (serveurs ou réseau) ne jouaient un rôle que dans 10 à 25 % des pannes [13].
Par exemple, une étude sur les grands services Internet a révélé que
les erreurs de configuration des opérateurs étaient la principale cause des pannes, alors que les pannes matérielles (serveurs ou réseau) ne jouaient un rôle que dans 10 à 25 % des pannes [13].

Concevez les systèmes de manière à minimiser les risques d'erreur. Par exemple, des abstractions, des API et des interfaces d'administration bien conçues permettent de faire facilement « la bonne chose » et de décourager « la mauvaise chose ». Cependant, si les interfaces sont trop restrictives, les utilisateurs les contourneront, ce qui annulera leur avantage. Il s’agit donc d’un équilibre délicat à trouver.

Différenciez les endroits où les utilisateurs font le plus d’erreurs de ceux où ils peuvent provoquer des échecs. En particulier, fournissez des environnements sandbox non productifs complets où les utilisateurs peuvent explorer et expérimenter en toute sécurité, en utilisant des données réelles, sans affecter les utilisateurs réels.

Effectuez des tests approfondis à tous les niveaux, des tests unitaires aux tests d’intégration de l’ensemble du système et aux tests manuels [3]. Les tests automatisés sont largement utilisés, bien compris et particulièrement utiles pour couvrir les cas particuliers qui surviennent rarement dans le cadre d’un fonctionnement normal.

Permettez une récupération rapide et facile des erreurs humaines, afin de minimiser l’impact en cas d’échec. Par exemple, faites en sorte qu’il soit rapide d’annuler les modifications de configuration, de déployer progressivement le nouveau code (de sorte que les bogues inattendus n’affectent qu’un petit sous-ensemble d’utilisateurs) et de fournir des outils pour recalculer les données (au cas où il s’avérerait que l’ancien calcul
était incorrect).

Divers les transactions : 
- https://www.postgresql.org/docs/current/transaction-iso.html
- https://medium.com/@darora8/transaction-isolation-in-postgres-ec4d34a65462
- https://www.amazon.fr/High-Performance-PostgreSQL-Rails-Maintainable/dp/B0CX876RLY/ref=asc_df_B0CX876RLY/?tag=googshopfr-21&linkCode=df0&hvadid=701510839370&hvpos=&hvnetw=g&hvrand=9391711952525364740&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9055729&hvtargid=pla-2293646746018&psc=1&mcid=876e00c7c6d034bea5573eda90bcc24d&gad_source=1
- https://www.postgresql.org/docs/current/rules-materializedviews.html
- https://medium.com/design-microservices-architecture-with-patterns/materialized-view-pattern-f29ea249f8f8
- https://www.metisdata.io/blog/transaction-isolation-levels-and-why-we-should-care
- https://www.iambobur.com/post/querying-microservices-in-real-time-with-materialized-views
Exemple : 
 - Les vues sql permettent de sécuriser la données : https://www.pairform.fr/les-vues-sql.html


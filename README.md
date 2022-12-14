# Travelnetic

Hem decidit crear aquest repositori per posar-hi fitxers d'interès del nostre cercador. Dins el repositori hi podem veure el programa amb el que hem creat el dataset que hem estat utilitzant durant tot el projecte i el codi dels recomanadors implementats en el cercador. També hem penjat l'Excel necessari per crear el dataset i un dels datasets obtinguts amb el nostre programa.

Per començar, el fitxer en el que creem el dataset és el fitxer de Jupyter "CreateFlightDataset.ipynb". Per tal que aquest fitxer funcioni es necessita l'Excel "world_capitals.xlsx", que també es troba en aquest repositori. Aquest Excel té 50 capitals de paísos d'arreu del món (i Barcelona) juntament amb les seves coordenades i altres camps que no son rellevants per nosaltres. Aquestes 50 ciutats son les que poden apareixer com a origen o destí en el nostre dataset. A partir de les coordenades calculem les distàncies entre origen i destí i a partir d'aquesta distància calculem el temps del vol.

Molts dels camps del nostre dataset com per exemple l'hora i el dia de sortida del vol o l'aerolínia són dades aleatòries, en aquest últim cas escollint aleatòriament entre una llista de 10 aerolínies. Hi ha altres camps com el nombre de parades o la classe que també son aleatòries però amb probabilitats. Afegim probabilitats al nombre de parades perquè no és molt comú veure vols de poca distància amb alguna parada, igual que tampoc son comuns els vols de llargues distàncies sense parades. Aleshores, segons si la distància del vol és major o menor li apliquem unes probabilitats o unes altres al nombre de parades. Seguint amb la classe del vol, aquest camp també té probabilitats per dues raons: primer perquè hi acostumen a haver menys vols de classe Business que de classe Economy, i segon perquè ens interessa tenir més vols econòmics perquè el que volem és trobar vols barats. Per aquesta raó hem decidit que la probabilitat que la classe del vol sigui Economy és superior, amb una probabilitat del 65%.

Per últim, comentar que el preu del vol es basa sobretot en la duració del vol però no li afecta l'hora del vol ni la data, ja que trobavem que era bastant complicat obtenir preus precisos afegint aquestes variables. Aleshores, el preu depèn principalment del temps del vol tot i que es multiplica per un valor que es troba en un rang per tal de obtenir preus diferents per un mateix vol i així poder buscar els vols amb millor preu en el nostre cercador. El preu es multiplica per un valor superior en els vols que són de classe Business que en els Economy.


En aquest repositori també hi hem posat un dels datasets que hem creat amb el codi comentat anteriorment, s'anomena "dataset_50k.xlsx". Com el seu nom indica, aquest dataset conté 50.000 vols i és el més petit que hem creat. Hem penjat aquest perquè pugueu veure un exemple de com és el dataset que utilitzem nosaltres pel projecte, ja que aquest conté els mateixos camps i està creat de la mateixa manera.
El dataset que utilitzem nosaltres és el més gran que hem creat fins ara, ja que el programa no és molt ràpid i tardariem bastant en obtenir datasets més grans. Tot i així, aquest dataset té 500.000 vols i és suficientment gran com perquè hi hagi més d'un vol per un mateix origen, destí i dia, pel que ens és molt útil per cercador.



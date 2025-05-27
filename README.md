# Hornet 3D Model – Blender Project

Questo progetto consiste nella modellazione 3D del personaggio **Hornet** dal videogioco *Hollow Knight*, realizzato in **Blender 4.4.0** come progetto per il corso Fondamenti di Computer Grafica. Come reference ho usato semplicemente immagini prese online.

![0010-0250](https://github.com/user-attachments/assets/ff42db18-413e-4b94-b77f-717338452e11)


Nota: prima di fare questo progetto, ho seguito il tutorial su Youtube di blenderGuru sulla creazione di modelli di ciambella, caricato anch'esso su github: [ciambellaBlender](https://github.com/FedericoCerra/ciambelleBlender)

Nella cartella **file blend** sono presenti tutti i salvataggi eseguiti passo passo, in seguito commenterò per ogni file cosa ho fatto.

1. Creato lo scheletro della testa, usando una **curva Bèzier** e specchiandola(modificatore mirror). Aggiunto spessore con l'impostazione Depth, fatto la punta con Alt + S (che riduce il raggio del cerchio attorno al punto).
    Convertito in mesh per applicare il modificatore mirror.

  ![image](https://github.com/user-attachments/assets/0467844b-d629-455d-bc00-9f0291c6d20c)


2. Migliorato un po la forma usando la sculpt mode

![image](https://github.com/user-attachments/assets/78c25958-3bad-462a-ade9-00b3c7b071a9)


3.  Creato il corpo. principalmente ho usato un cerchio con 10 lati, estrudendone i vertici per creare busto e gambe. Piccoli miglioramenti alla testa e fatto i buchi per gli occhi usando la sculpt mode (pennello blob inverso, tenendo premuto ctrl)

![image](https://github.com/user-attachments/assets/635dd84a-08e7-4fa3-bf21-105e71553780)


4.  Piccoli cambiamenti.

![image](https://github.com/user-attachments/assets/3c4f80bf-f782-48d4-a3bf-5044f68563e7)


5. Prime prove di mantello. anche qua un cerchio con estrusione di vertici. A questo punto stavo cercando di applicare la fisica al mantello per farlo "svolazzare". Ho fatto un pò di prove con un piano sopra ad un cubo per capire come funzionasse l'aggiunta di fisica agli oggetti. (Aggiungi collision all'oggetto che vuoi rendere rigito, cloth all'oggetto che vuoi sia il mantello)

![image](https://github.com/user-attachments/assets/2d9d563d-a476-4214-b8cd-20925437cc4d)


6. Sempre prove col vento, non funzionanti. Aggiunto il pin al mantello mettendo i vertici attorno al colletto in un vertex group e in seguito mettendo quel vertex group come pin in modo da far stare appeso il mantello. Il mantello qua rimaneva comunque troppo rigido.

![image](https://github.com/user-attachments/assets/f0bad255-0110-4f1a-bfab-d831aaa1812a)


7. Fine del mantello, aumentato le subdivision in modo che si pieghi di più. Qua ho avuto diversi problemi con il vento quindi l'ho momentaneamente rimosso.

![image](https://github.com/user-attachments/assets/aaca2b75-db9a-4522-89ab-ea103d822503)


8. Creata l'arma. Qua ho unito un torus ad un cilindro, ho poi aggiunto la lama fatta con un piano che è stato modificato.

![image](https://github.com/user-attachments/assets/ba683c1b-b703-4977-a158-6b6c2c99456e)


9. Lama finita, aggiustato di poco le dimensioni per farla proporzionata al modello di hornet. piccoli ritocchi alla sezione physics del mantello per renderlo più morbido.

![image](https://github.com/user-attachments/assets/e27eed60-9c4f-4bf8-ab07-324e2382e47b)


10. Piccole modifiche alla testa.

![image](https://github.com/user-attachments/assets/91077c00-e67a-4eac-8418-505b34d7c6ac)


11. Ho creato gli occhi, aggiungendoli al modello della testa. Creato materiali per mantello, arma, pelle e occhi. Piccola modifica al manico dell'arma, che non era propriamente simmetrico.

![image](https://github.com/user-attachments/assets/85aa2ff4-10bc-4e00-8d03-ac53ddf57b38)


12. Creato il filo attorno a hornet. ho usato una curva Bèzier a cui ho aggiunto sempre più punti(ctrl+click sulla curva). Piccole modifiche alla testa, resa più spessa.

![image](https://github.com/user-attachments/assets/63c2ae60-f311-4db2-92ea-35e3cd790638) ![image](https://github.com/user-attachments/assets/426f9b2b-eaba-42b2-95c7-e396f65bb729)


13. Reso il materiale del filo leggermente luminoso(surface: Emission), filo reso piu spesso.

![image](https://github.com/user-attachments/assets/b814ecfc-b7dc-4dc2-8347-4d322f407946)


14. Creato una scena. Qua ho usato un piano con bevel per lo sfondo, aggiunto luci ad area. Per la colorazione del piano, ho usato i Geometry Nodes per dare l effetto sfumato. (ho seguito un tutorial su youtube)

![image](https://github.com/user-attachments/assets/210289a1-0f5c-40e0-aa33-10f7e0376758)
![image](https://github.com/user-attachments/assets/d7a6a310-fa97-41a6-a734-05fdec0f5763)


15-16. Stavo provando diverse cose per il mantello, ho riscontrato diverse difficoltà qua. O non si muoveva col vento o si muoveva troppo, compenetrandosi con il modello del corpo. Ho provato diversi livelli di subdivision sia del modello che del mantello fino ad avere un mantello che non si compenetrasse.

![image](https://github.com/user-attachments/assets/b34da464-a407-4015-9c86-843dd05d6a4f)



17. Qua ho provato ad animare il filo che circonda hornet. All'inizio ho provato con un Taper. Non ha funzionato. Ho provato poi a selezionare alcuni punti e applicare il modificatore Wave. In seguito ho provato a mettere un oggetto ancora a alcuni punti ed applicare ad esso il modificatore Wave. Ho scoperto che i punti non seguono l oggetto ancora se lo spostamento avviene con un modificatore(Ho anche provato ad applicarlo, ma niente). Infine, ho risolto aggiungendo un empty, ancorare ad esso alcuni punti e muoverlo "a mano", mettendo keyframes.

https://github.com/user-attachments/assets/944737b5-7d31-4698-ac1f-5058fcd2d678


18. Fine. Ho modificato di poco la testa del modello (pennello smooth, scalato di poco verso l'alto e rimpicciolito).Ho inoltre tolto un lattice per la testa che avevo messo per piegare la testa all'indietro, ma alla fine ho optato per toglierlo e usare la sculpt mode. Ho eseguito il rendering di 240 frames, con cycles. Ho renderizzato la sequenza di immagini e poi unite nell'video editor fornito da blender(a quanto ho visto su internet, è meglio rispetto a renderizzare il video direttamente siccome è possibile recuperare da dove ci si è fermati in caso di interruzioni)

![image](https://github.com/user-attachments/assets/529b1a07-03fc-4d73-b72f-63810312e380)


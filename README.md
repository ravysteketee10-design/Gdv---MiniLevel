Mini-level — Inleveren
Naam: Ravy Steketee
Klas: Datum:
Les: GDV Les 6

Wat heb ik gemaakt?
Ik heb een platformer gemaakt waar je 4 coins moet pakken en het parcour goed moet doen.

Screenshot / GIF van je level
 ![status](img/test.png)

Bewegend object
void Update() 
{ 
Vector3 move = Vector3.right * speed * Input.GetAxis("Horizontal") * Time.deltaTime; 
 transform.position += move; 
 Vector3 moveforward = Vector3.forward * speed * Input.GetAxis("Vertical") * Time.deltaTime; 
 transform.position += moveforward; 
} 
Collider of trigger
private void OnCollisionEnter(Collider other) 
{ 
	if (other.gameObject.CompareTag("Stucture")){ 
    jumpingtest = true; 
} 
} 
Logica met if of switch
if (other.gameObject.CompareTag("Enemy")) 
 { 
     health -= 1; 
     Debug.Log($"you took damage, you now have {health} health left."); 
     Destroy(other.gameObject); 
 } 

Evaluatie 

Wat ging goed? en waarom? 

Het maken van het level en de platforms gingen goed aangezien ik dat meerdere keren heb gedaan.

Wat vond je lastig? en waarom? 

Zorgen dat mijn game geen flappy birds is, Ik had problemen met dat de speler zo vaak als je wou kon springen.

Wat zou je een volgende keer anders doen? 

Nu ik weet hoe ik ervoor zorg dat het geen flappy birds is hoef ik daar niet mee te kloten voor een uur.
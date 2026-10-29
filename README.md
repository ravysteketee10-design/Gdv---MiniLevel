Mini-level — Inleveren<br>
Naam: Ravy Steketee<br>
Klas: SD1C<br>
Datum:28-10-26<br>
Les: GDV Les 6<br>

Wat heb ik gemaakt?<br>
Ik heb een platformer gemaakt waar je 4 coins moet pakken en het parcour goed moet doen.<br>

Screenshot / GIF van je level<br>
 ![status](img/test.png)<br>

Bewegend object<br>
void Update() <br>
{ <br>
Vector3 move = Vector3.right * speed * Input.GetAxis("Horizontal") * Time.deltaTime; <br>
 transform.position += move; <br>
 Vector3 moveforward = Vector3.forward * speed * Input.GetAxis("Vertical") * Time.deltaTime; <br>
 transform.position += moveforward; <br>
} 
Collider of trigger<br>
private void OnCollisionEnter(Collider other) <br>
{ <br>
	if (other.gameObject.CompareTag("Stucture")){ <br>
    jumpingtest = true; <br>
} <br>
} <br>
Logica met if of switch<br>
if (other.gameObject.CompareTag("Enemy")) <br>
 { <br>
     health -= 1;<br>
     Debug.Log($"you took damage, you now have {health} health left."); <br>
     Destroy(other.gameObject); <br>
 } <br>

Evaluatie <br>
<br>
Wat ging goed? en waarom? <br>
<br>
Het maken van het level en de platforms gingen goed aangezien ik dat meerdere keren heb gedaan.<br>
<br>
Wat vond je lastig? en waarom? <br>
<br>
Zorgen dat mijn game geen flappy birds is, Ik had problemen met dat de speler zo vaak als je wou kon springen.<br>
<br>
Wat zou je een volgende keer anders doen? <br>
<br>
Nu ik weet hoe ik ervoor zorg dat het geen flappy birds is hoef ik daar niet mee te kloten voor een uur.<br>
# Ex4.2-Animal-Feeding-Phase-2
##AIM :

To develop a animal feeding game-Phase-2 using unity.

## ALGORITHM :
Step 1
In the Hierarchy, create an Empty object called “SpawnManager”
step 2
Create a new script called “SpawnManager”, drag the script and attach it to the Spawn Manager in the hierarchy , and open it
step 3
Declare new public GameObject[ ] animalPrefabs;
step 4
In the inspector assign the size as 3 , for each element drag the animals from prefabs folder into the array
step 5
Double-click on one of the animal prefabs, then Add Component > Box Collider
step 6
Check the “Is Trigger” checkbox
step 7
Add a RigidBody component to the (banana)projectile and uncheck “use gravity”.
step 8
Create a new DetectCollisions.cs script, then drag the scripts and add it to each animal prefab and banana, then open it and check it.
step 9
For all the animal prefabs and food in th inspector (below the layer ) drop down the override option and choose apply all.
##  PROGRAM :
### DEVELOPED BY : MOURYA .G
### REG NO : 212224230170
### SPAW MANAGER
~~~
 using UnityEngine;
using System.Collections;
using System.Collections.Generic;

public class SpawnManager : MonoBehaviour
{

    public GameObject[] animalPrefabs;
    private float spamRangeX=5;
    private float spamPosZ=2;
    private float startDelay=2;
    private float spamInterval=1.5f;
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    void Start()
    {
        InvokeRepeating("SpawnRandomAnimal",startDelay, spamInterval);
    }

    // Update is called once per frame
    void Update()
    {
        
    }
    void SpawnRandomAnimal()
    {
        int animalIndex = Random.Range(0, animalPrefabs.Length);
        Vector3 spamPos = new Vector3(Random.Range(-spamRangeX,spamRangeX),0 ,spamPosZ);
        Instantiate(animalPrefabs[animalIndex],spamPos, animalPrefabs[animalIndex].transform.rotation);
    }
}
~~~
### OUTPUT :
![image](https://github.com/user-attachments/assets/301d96a1-7798-4d8c-b26a-e354cbd23eca)
### RESUT:
Animal feeding game-Phase-2 using unity is developed successfully.


      

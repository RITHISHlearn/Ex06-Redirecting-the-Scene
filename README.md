# Ex06-Redirecting-the-Scene

## Aim:

To Redirecting the scene in the unity engine.

## Algorithm:

Step 1: To open the unity engine.


Step 2: Create a new 3D project.


Step 3: Create plane and name it as ground and create cube and name it as player.


Step 4: Add WinText in Hierarchy.


Step 5: Create a C# Script and name it as playercontroller and add the script to player.


Step 6: Use the R button to change the level2


Step 7 Print the Output and end the program.

## Program:

### DEVELOPED BY: RITHISH P

### REGISTER NUMBER : 212223230173

### CUBE PLAYER:


````
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Coding : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();

    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }

    }
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}

````

## Output:

![image](https://github.com/user-attachments/assets/abd595af-dcee-443f-ac7f-9cfd96be980a)

![image](https://github.com/user-attachments/assets/0d068981-164c-43da-a6ad-8f7a90ae30cb)

## Result:

Thus, the execution of above C# coding is successfully redirecting the scene in the unity engine.

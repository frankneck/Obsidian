1. Создание проекта
2. Установка нужных пакетов
	1. XR Interaction Toolkit
	2. New Input System
3. Создание движения перснонажа
4. Создание взаимодействия с миром
	1. Create script: abstract class Interactable
	2. Create folder: Interactable
	3. Create script for object: keypad. In this script we override Interact()
	4. Create script PlayerUI. 
	5. Create script PlayerInteract.
		1. A creation of fields:
			1. distance
			2. mask
			3. cam
			4. playerUI
			5. inputManager
		2. Awake()
			1. cam
			2. playerInput
			3. inputManager
		3. Update()
			1. string.Empty
			2. ray
			3. Debug.Dra...
			4. hitInfo
			5. code below
	6. A creation of  



```C#
if (Physics.Raycast(ray, out hitInfo, distance, mask))
    {
		if (hitInfo.collider.GetComponent<Interactable>() != null)
		{
			Interactable interactable = hitInfo.collider.GetComponent<Interactable>();
			playerUI.UpdateText(interactable.message);
                
			if (inputManager.onFoot.Interact.triggered)
            {
				interactable.BaseInteract();
            }
        }
    }
```
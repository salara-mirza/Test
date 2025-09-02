# ShopInventory_2

A robust shop and inventory system built in Unity. This project demonstrates a clean architecture using centralized dependency management, a modular UI, and event-driven logic to create an extensible and maintainable framework for in-game economies.

[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-in--progress-yellow.svg)]()
[![Made with Unity](https://img.shields.io/badge/engine-Unity-black.svg?logo=unity)]()

---

## Gameplay Demo

*To make this work, choose **one** of the options below and delete the other. Replace the placeholders with your file paths or YouTube video ID.*

[![Watch the Gameplay Video](https://img.youtube.com/vi/4PXhIu0BPcE&t=58s/0.jpg)](https://www.youtube.com/watch?v=4PXhIu0BPcE&t=58s)

---

## UML Architecture Diagram

*To make this work, place your UML diagram image inside the `AboutProject` folder and name it `UML_Diagram.png`, or update the path below.*

![UML Diagram](https://github.com/salara-mirza/Test/blob/main/Shop_InventoryUML.png)

---

### Project Features

*   **Centralized Dependency Management:** All major managers and controllers (GameContext, AudioManager, UIRootController, PlayerInventory, ShopInventory) are created and referenced from a single CentralRegistry, simplifying initialization and access.
*   **Modular UI System:** UIRootController manages all UI logic, including shop/inventory toggling, item lists, descriptions, buy/sell panels, and feedback popups.
*   **Inventory and Shop Logic:** PlayerInventory and ShopInventory handle item management, transactions, and validation, supporting stackable/non-stackable items, weight limits, and stock refresh.
*   **Audio Feedback:** AudioManager provides background music and SFX for UI interactions and transaction outcomes.
*   **Popup Feedback:** PopupPanel displays modal messages for user feedback and hints.
*   **Extensible Item System:** ItemData and related enums (ItemTypes, ItemRarity) support a variety of item types and rarities.
*   **Validation Layer:** TransactionValidator ensures all buy/sell actions are checked for rules and constraints.

### Design Patterns Used

*   **Singleton (CentralRegistry):** CentralRegistry uses a singleton pattern to ensure a single instance manages all dependencies.
*   **Dependency Injection:** Managers and controllers receive their dependencies via DI methods (e.g., `SetDependencies`), improving testability and decoupling.
*   **Service Locator:** CentralRegistry acts as a service locator, providing access to shared services and managers.
*   **Event-Driven Architecture:** Inventory and shop changes use C# events to notify UI and other systems of state changes.
*   **Prefab/Component-Based UI:** `ItemButtonBinder` is used as a prefab component for dynamic item lists in the UI.

### Principles Followed

*   **Single Responsibility Principle (SRP):** Each class has a clear, focused responsibility (UI, audio, inventory, shop, validation, etc.).
*   **Separation of Concerns:** UI logic, game logic, audio, and data management are separated into distinct classes.
*   **Encapsulation:** Internal state is protected; public methods are used for interaction.
*   **Loose Coupling:** Dependency injection and event-driven updates reduce direct dependencies between classes.
*   **Extensibility:** The system is designed to easily add new item types, UI features, or managers.

---

### Getting Started

1.  Clone the repository: `git clone <your-repo-url>`
2.  Open the project folder in Unity Hub.
3.  Launch the project in the Unity Editor.
4.  Open the main scene located in the `Assets/Scenes` folder and press Play.

### Repository Structure


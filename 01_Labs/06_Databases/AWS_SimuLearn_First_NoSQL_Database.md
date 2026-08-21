# ☁️ AWS SimuLearn: First NoSQL Database

## 🎯 Objective
Design and provision a fully managed Amazon DynamoDB NoSQL table, define primary keys (Partition and Sort keys), construct complex JSON-like schema attributes, and execute Query vs. Scan operations for efficient data retrieval.

---

## 🏗️ Architecture & Configuration
* **Database Service:** Amazon DynamoDB
* **Table Name:** `UserVideoHistory`
* **Primary Key Schema:**
  * **Partition Key (HASH):** `userId` (String)
  * **Sort Key (RANGE):** `lastDateWatched` (Number - UNIX Timestamp)
* **Custom Attributes:** `videoId` (String), `preferredLanguage` (String), `supportedDeviceTypes` (List), `lastStopTime` (Number), `rating` (Number)

---

## 🛠️ Key Implementation Steps
1. **Table Provisioning:** Provisioned the `UserVideoHistory` DynamoDB table using default capacity settings with a composite primary key structure.
2. **Item Creation & Attribute Definition:** Constructed initial viewer history records incorporating diverse data types including Strings, Numbers, and nested Lists (`supportedDeviceTypes`).
3. **Item Modification:** Updated item attributes dynamically to append `lastStopTime` for playback tracking functionality.
4. **Data Insertion (DIY Task):** Created a new unique record within `UserVideoHistory` and appended a custom `rating` attribute defined explicitly as a **Number** data type.
5. **Query vs. Scan Execution:** Ran targeted key-based **Query** operations using conditional operators (`Greater than` on timestamps) and evaluated the performance trade-offs against full-table **Scan** operations.

---

## 💡 Key Architectural Takeaway
DynamoDB provides single-digit millisecond latency at scale by enforcing schema flexibility on item attributes while keeping key indexing strict. Applications should rely on precise **Query** operations using Partition and Sort keys rather than costly **Scan** operations, which evaluate every item in the table and consume significantly more Read Capacity Units (RCUs).

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/First%20NoSQL%20Database.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/First%20NoSQL%20Database.png" alt="AWS SimuLearn - First NoSQL Database Badge" width="350" />
  </a>
</p>

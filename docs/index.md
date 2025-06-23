# IBM Application Development Demos

Welcome! Use the sidebar on the left to navigate through available demo environments and modernization workflows.

---

## 🚀 Demo Environments

- **[Liberty Environment Demo](liberty-demo/index.md)**  
  Step-by-step instructions for reserving and accessing the Liberty/OpenShift demo VM.

- **[Watsonx Code Assistant (WCA) Demo](wca4j-demo/index.md)**  
  Hands-on instructions for using watsonx Code Assistant for AI-driven Java development and modernization.

---

## 🏗️ WCA + TWAS to Liberty Modernization POC

This Proof of Concept demonstrates modernizing a **Traditional WebSphere (WAS)** app to **Liberty WebSphere**, integrating with IBM WCA and modernization tools.

### 🔄 Modernization Workflow Overview

1. **Convert build system from Ant to Maven**  
   - Compile & package `.war` and `.ear` artifacts.

2. **Maven Project Build**  
   - Inject environment-specific configurations.

3. **Run Static Analysis**  
   - Scan the WAR using **Application Modernization Accelerator** (AMA) / **Transformation Advisor** (TA).

4. **Upload Scan Artifacts**  
   - Push results to AMA UI and watsonx Code Assistant.

5. **Modernize WebSphere Runtime**  
   - Refactor the application from **Traditional WAS** to **Liberty**.

6. **Upgrade Java Version**  
   - Migrate to a modern, supported Java runtime.

7. **Containerize the Application**  
   - Package into OCI-compliant images using best practices.

8. **Deploy to OpenShift Container Platform (OCP)**  
   - Deploy the containerized app to a cloud-native platform.

---

!!! note "Proceed to Workstation Setup"
    Once you have completed the prerequisites, please continue to the [Workstation Setup](./workstation-setup.md) guide.

---

Click on one of the demo names in the sidebar to begin.

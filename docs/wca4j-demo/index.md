# App Development & Modernization with WCA

The main objective of this lab is to provide hands-on experience with some of the core features and capabilities available to developers in IBM watsonx Code Assistant (WCA). The lab content is loosely organized to align with the capabilities found in the two different plans (editions) available for WCA:

- **Essentials**: This accelerates software development, allowing developers to use WCA with integrated generative AI for coding tasks, including:
  - Generating code  
  - Explaining code  
  - Creating unit tests  
  - Documenting code  

- **Standard**: In addition to all the capabilities found in the Essentials plan, the Standard plan also includes these enterprise Java modernization capabilities:
  - Java upgrades, regardless of runtime  
  - WebSphere to Liberty transformation  
  - Enhanced test generation and code explanation  

After completing this lab, you will have a deeper understanding of what is possible with WCA and will have observed how it can be a powerful tool to help accelerate software development and application modernization.

---

## Prerequisite Installation Steps

As previously mentioned, there are two separate components that make up IBM watsonx Code Assistant (WCA):

1. **WCA service** – This is the back-end software, leveraging generative AI, that services requests from developers. It is available as software-as-a-service (SaaS) on IBM Cloud and as deployable software for on-premises and cloud deployments.  
2. **WCA extension (plug-in)** – Installed in an integrated development environment (IDE) on a developer’s own system, this is how the developer interacts with WCA. It includes a chat interface as well as in-source options for generating, explaining, and documenting code. It can also help drive Java upgrades and WebSphere to Liberty transformation, among other things. The IDEs currently supported by WCA are Visual Studio Code (VS Code) and Eclipse.

> **Tip**  
> To avoid the need for you to set up your own development environment (which would include installation of an IDE, the WCA extension, various other software, and sample source code), a pre-configured environment has been made available for you in IBM Technology Zone (TechZone). Likewise, a WCA service has been made available to you as well, also available through TechZone. However, this lab assists you in setting up your own system to perform the lab on your own system using the TechZone WCA Service as the back-end.

---

## Reserve the TechZone Environment

1. **Open the collection for WCA-related environments in TechZone.** Sign in with your IBMid if prompted.

2. **Locate the “Request watsonX Code Assistant – Standard (GA) [Approval Gated]” tile** and click the **IBM Cloud environment / Reserve it** button (A).  
   ![Click “Reserve it” on the WCA – Standard tile](images/request-watsonx.png)  
   *Figure 1 – Selecting the WCA – Standard (GA) tile and clicking “Reserve it” (A).*

3. **Accept the default for the reservation Name (A)** or provide a name of your choosing. For the Purpose of the reservation, select **Education** (B).  
   ![Provide a name and select Education](images/reservation-request-watsonx.png)  
   *Figure 2 – Providing a reservation name and selecting “Education.”*

4. **Fill in the Purpose description box** with the reason you are making the reservation. Then select your Preferred Geography based on your desired location.  
5. **Adjust the reservation’s Start date and time and End date and time** as needed (note that you can extend your reservation later if you need more time).  
6. **In the lower-right corner, follow the links to read TechZone’s terms, conditions, and security policies**, and then select the checkbox to agree to them.  
7. **Click Submit for approval.** A message in the upper-right corner will briefly appear stating that the reservation has been created.

> **Note**  
> You will receive an email from IBM Technology Zone with a subject of “Request is Pending Approval.” Once it has been approved you will receive another email with a subject of “Request Approved.”  
> When provisioning starts (based on the start time you provided) an email with a subject of “Reservation Provisioning on IBM Technology Zone” is sent. Finally, an email with a subject of “Reservation Ready on IBM Technology Zone” indicates that provisioning has completed.

---

### If You Want a Developer System from TechZone

If you chose not to use your local system as your development environment, follow these steps to provision the pre-configured demonstration environment from TechZone (includes RHEL 9, VS Code w/ WCA extension, Eclipse IDE, OpenJDK 11 & 21, and sample ModResorts application).

1. **Open the collection of WCA-related environments in TechZone.** Sign in with your IBMid if prompted.  
2. **Locate the “watsonx Code Assistant – Demonstration VM” tile** and click the **IBM Cloud environment / Reserve it** button.  
   > _Note: There are multiple tiles listed—ensure you select the correct one._  
3. **For the reservation type, select the “Reserve now” radio button.**  
   ![Select “Reserve now” for the WCA demonstration VM](images/wca-reserve.png)  
   *Figure 3 – Reserving the “watsonx Code Assistant – Demonstration VM” (Reserve now).*

4. **Accept the default for the reservation Name** or provide a custom name. For the Purpose, select **Education**.  
5. **Fill in the Purpose description box** and then select your Preferred Geography.  
6. **Adjust the reservation’s End date and time** as needed. Leave **VPN Access** set to **Disable**.  
7. **Follow the terms links**, check the agreement box, and click **Submit**.  
   ![Agree to terms and submit the WCA demo VM reservation](images/reservation-request-watsonx.png)  
   *Figure 4 – Agreeing to TechZone terms and submitting.*

8. **Watch for provisioning emails**: “Reservation Provisioning on IBM Technology Zone” and then “Reservation Ready on IBM Technology Zone.”

---

## Workstation Setup

### Java Installation

1. **Install Java 21** using the applicable download for your OS:  
   - **Mac (Arm64)**: Download Java for MacOS – Arm64  
   - **Mac (x86)**: Download Java for MacOS – x86  
   - **Windows**: Download Java for Windows  

   All of the above are compressed files; extract them to any folder on your local system.

2. **Check if Java is installed properly**:  
   ```bash
   java --version

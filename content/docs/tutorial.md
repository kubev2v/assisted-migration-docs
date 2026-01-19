---
title: "Tutorial"
linkTitle: "Tutorial"
weight: 2
---

# How to Use Migration Assessment

This tutorial covers two methods to assess your VMware environment for migration to OpenShift Virtualization.

**Choose your assessment method:**

- **[RVTools Flow](#rvtools-flow)** - Upload an existing RVTools Excel export for instant assessment
- **[Discovery Agent Flow](#discovery-agent-flow)** - Deploy an OVA to vCenter for live discovery

---

## RVTools Flow

Upload an existing RVTools export file for instant assessment. Watch the video tutorial below:

<iframe width="700px" height="400px" src="https://embed.app.guidde.com/playbooks/2o11fzpTRbEM2uDjauyBCi" title="Assisted Migration Using RVtools Flow" frameborder="0" referrerpolicy="unsafe-url" allowfullscreen="true" style="border-radius: 10px"></iframe>

### Prerequisites: RVTools File Requirements

Before uploading your RVTools export, ensure your Excel file meets the following requirements. The migration assessment tool validates your RVTools export and will report errors or warnings based on what's present.

#### Hard Requirements (Errors)

If these are missing, the upload will **fail**. All of these reside in the **vInfo** sheet:

| Requirement | Why? |
|-------------|------|
| **vInfo** sheet must have at least 1 row | No VMs means there is no inventory to plan |
| Column **VM ID** must not be null/empty | Used as the primary unique identifier for VMs |
| Column **VM** (Name) must not be null/empty | Used to identify and display the VM |

#### Soft Requirements (Warnings)

The following sheets are checked, but if they are empty or missing, the tool will only issue a **warning**. The inventory will still be built, but specific data points will be blank:

| Sheet | Impact if Missing |
|-------|-------------------|
| **vHost** | Host-related info will be unavailable |
| **vDatastore** | Storage/datastore info will be missing |
| **vNetwork** | Network configuration details will be missing |
| **vCPU** | Detailed CPU metrics (like core counts) will be missing |
| **vMemory** | RAM allocation details will be missing |
| **vDisk** | Disk size and provisioning data will be missing |
| **vNic** | Network interface details (IPs/MACs) will be missing |

Export your RVTools data with **all sheets enabled** to ensure the most comprehensive migration assessment. 

### Go to [console.redhat.com](https://console.redhat.com)

### 1\. Introduction

![Introduction](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FedE8CD8BE2bhNc9ovm6Lac_doc.png?alt=media&token=98b822c4-a9cf-4826-9237-8741e0770d05)

### 2\. Click Start Evaluation

![Click Start Evaluation](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FaynpBPyt5wh324VWxpnVoM_doc.png?alt=media&token=2c913f60-c768-4c79-b1d7-a92505797d3e)

### 3\. Introduction

![Introduction](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2Fn7FfByLQMii671hpFhPVRs_doc.png?alt=media&token=3612ff9b-8310-4933-a035-dc0a19d5b7a2)

### 4\. Click Create New Migration Assessment

![Click Create New Migration Assessment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FtUtFVs9Gdeyz6CoQ3XXVAf_doc.png?alt=media&token=df181c86-bbcd-4395-8f5b-a1a3a00b4e4e)

### 5\. Select RVTools File Option

![Select RVTools File Option](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2F4XLGQ97HixcgmMR7wwz9Vj_doc.png?alt=media&token=638026ea-e597-4db6-9dd3-519ccde6ae39)

### 6\. Access Assessment Name Field

![Access Assessment Name Field](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FdBGYtcae2tqQZrmDD7LMap_doc.png?alt=media&token=d6db4615-ec6b-4308-88d6-7743f3b5b0a1)

### 7\. Click Select Button

![Click Select Button](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FfPrEmmnF8Q43GnKEWiyEic_doc.png?alt=media&token=4ecae9b7-25c6-4d11-9eb2-d8ef10eb77cb)

### 8\. Create Migration Assessment

![Create Migration Assessment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2F2cp31QcofkpjHudvRfT893_doc.png?alt=media&token=06847d1b-9773-45ee-bf03-92a57cf672b5)

### 9\. Validate Virtual Machines

![Validate Virtual Machines](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2F19Yh38UG35ULYrpNp6s67K_doc.png?alt=media&token=72c059f2-6f59-4d77-8f8e-4e9816fe3384)

### 10\. Review Migration Data Chart

![Review Migration Data Chart](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FpJJtb8QrVXhBd6CsmZ3iw9_doc.png?alt=media&token=2d0bbd0d-e3ab-4217-b233-62eaaa759d47)

### 11\. Check Changed Block Tracking Status

![Check Changed Block Tracking Status](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2F2fKZ7yidCcNpsKqh87AhHk_doc.png?alt=media&token=15b3bf40-5f31-469e-9757-98219dc57f3e)

### 12\. Analyze Migratable VM Data

![Analyze Migratable VM Data](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2F2o11fzpTRbEM2uDjauyBCi%2FbQ1iWK2aPCzaaRCjzSF7Zi_doc.png?alt=media&token=a30e126b-8c15-4525-8800-af15ddb8a589)

---

## Discovery Agent Flow

Deploy a discovery agent to your vCenter for live environment analysis. Watch the video tutorial below:

<iframe width="700px" height="400px" src="https://embed.app.guidde.com/playbooks/cZNzDp6dWjJ5UKdwozk3gc?mode=videoOnly" title="Configure Assisted Migration Agent Flow in Red Hat" frameborder="0" referrerpolicy="unsafe-url" allowfullscreen="true" allow="clipboard-write" sandbox="allow-popups allow-popups-to-escape-sandbox allow-scripts allow-forms allow-same-origin allow-presentation" style="border-radius: 10px"></iframe>

### Go to [console.redhat.com](https://console.redhat.com)

### 1. Introduction

![Introduction](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F8GAaxrXmMpCxLperW8fcd7_doc.png?alt=media&token=eaada01f-437a-446d-b169-9040e05d5b79)

### 2. Click Start Evaluation

![Click Start Evaluation](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F8xEQeTrXvwnhQaDVnjsCbF_doc.png?alt=media&token=f832b6ef-0888-4efd-9d39-acfadf9359d6)

### 3. Navigate to Environments Tab

![Navigate to Environments Tab](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Fwn4S76gPVkwcCh6UNM91Qv_doc.png?alt=media&token=a8af4c46-20d7-467f-bb71-085c813bc555)

### 4. Add New Environment

![Add New Environment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FssX6VvE45qGWqJaV1rnj1n_doc.png?alt=media&token=1a088725-7de1-436e-99ec-90c6c5a1303a)

### 5. Select Name Field

![Select Name Field](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FeNgsRvzTsnV7zKqpg4sUKw_doc.png?alt=media&token=f6b693f3-b4f4-4ee8-a9c1-0e4e283a9adb)

### 6. Select SSH Key Option

![Select SSH Key Option](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FsRyeysPLdu9hQ3Vns4U6ey_doc.png?alt=media&token=94bfeec9-82b4-4504-86af-eb2d12a647db)

### 7. Confirm Proxy Enablement

![Confirm Proxy Enablement](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FgkzMA4utuz7DhXFb983D7M_doc.png?alt=media&token=ffb16eed-89ac-4296-8a0f-21e19300c83c)

### 8. Generate OVA Template

![Generate OVA Template](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F51nMDdSPf7Gzkp76sGVajW_doc.png?alt=media&token=e1dfde90-fc46-41c8-be2c-e4390c5695b9)

### 9. Access Deployment Link

![Access Deployment Link](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FuoiTuGJpcajNvN88Mc1UPp_doc.png?alt=media&token=97ab76f3-2756-4642-94a0-adcaebae6f86)

### 10. Switch to vCenter Server

![Switch to vCenter Server](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F131yDfKDueYUBXVxx8G7o4_doc.png?alt=media&token=755f3768-1cc9-47d2-9149-c3fc656f839a)

### 11. Select User Account

![Select User Account](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FxhBYCxwnKFHTyrno6Evetg_doc.png?alt=media&token=b9603219-33c5-4352-b05b-cb76cc0ea9fb)

### 12. Start OVF Template Deployment

![Start OVF Template Deployment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Fu7hJb5QdCaTesi8ExVhCPy_doc.png?alt=media&token=f621b690-6bd5-4670-a7b8-d01283800a58)

### 13. Enter OVF Template URL

![Enter OVF Template URL](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FwfNY3QQ2xYZ3oX1DU7FzvU_doc.png?alt=media&token=9d15f0f1-9c60-44b0-8e89-f0825aa66c62)

### 14. Proceed to Next Step

![Proceed to Next Step](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FmDNVUxGAzofmgSnKU3Gbe5_doc.png?alt=media&token=d19c443e-ac5d-4373-aeb0-99e6a9915697)

### 15. Complete Deployment

![Complete Deployment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FaWkaaybaf5ZMUkZXuqnGq9_doc.png?alt=media&token=8a262f6c-c150-4b9c-8849-bb2a9a8a621c)

### 16. Access Deployment Details

![Access Deployment Details](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F4MBmYX5FyL2oPkB1nK5DJn_doc.png?alt=media&token=a7b884b3-e87a-4ee6-9caa-72eb1570e6fa)

### 17. Open Additional Options

![Open Additional Options](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FpriYJae3n82Bb6zxv1WegZ_doc.png?alt=media&token=fea1e10d-50a6-480b-961f-ccd42cb365d4)

### 18. Switch to Migration VM Interface

![Switch to Migration VM Interface](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Ff8JzHUdJ9HwwgrFd16TBJU_doc.png?alt=media&token=808674cf-6310-4f63-a25c-8e03b45a5754)

### 19. Switch to VM Interface

![Switch to VM Interface](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Ffzvtp12nGDWmno8U5zDUk5_doc.png?alt=media&token=053dff42-eec9-42a6-a610-0621c6d57302)

### 20. Select Environment URL Field

![Select Environment URL Field](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FuP5Yi18XRuqtMuYrcRNYN8_doc.png?alt=media&token=19af07f4-0379-4a80-b169-407b633fb7d1)

### 21. Enter Environment URL

![Enter Environment URL](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FayV75ZmjtsmmB4xWsvRk2h_doc.png?alt=media&token=2fc400d9-f65e-4152-9240-31ae1422282c)

### 22. Apply Environment Filters

![Apply Environment Filters](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Fqk29oembuENJPZHVGbisL7_doc.png?alt=media&token=5e61a79c-7e5f-4c4d-b3bb-1454cb698cae)

### 23. Create New Migration Assessment

![Create New Migration Assessment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FaqdENsHLPHYznuAc1YZG7d_doc.png?alt=media&token=33b0d5bd-52fd-4f99-860f-034dedd291d7)

### 24. Choose Discovery OVA Option

![Choose Discovery OVA Option](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Frxx3FEfwAjVmuxoHqCezyA_doc.png?alt=media&token=704bf162-0d33-49f1-a9ce-df9d64c36fcb)

### 25. Select Assessment Name Field

![Select Assessment Name Field](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F8uueE8tBxaS9rpRTZe1Wdi_doc.png?alt=media&token=7f53df87-23a7-44ef-9909-21ba3fae2997)

### 26. Enter Assessment Name

![Enter Assessment Name](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F4d4YydcpMY5qe47zsYL18L_doc.png?alt=media&token=43d7d3c4-e521-4c05-9bab-538f0867bc5f)

### 27. Select Existing Environment

![Select Existing Environment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F9Ygmqo6YmSes3g5nriz3QA_doc.png?alt=media&token=c6b32934-a4d8-43c3-8106-86d8b8b3d8be)

### 28. Confirm Environment Selection

![Confirm Environment Selection](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2F1qG3AXj9AfEPBN6SaB3TC8_doc.png?alt=media&token=e3729d9d-ee4b-4ae5-a4e4-668ec0be25bf)

### 29. Choose Environment from List

![Choose Environment from List](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FsEzsVEjcnrRQ3QESM3NEq5_doc.png?alt=media&token=3f474b12-ad7f-48a1-9876-e52b19b803ae)

### 30. Create Assessment Report

![Create Assessment Report](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FhD3WdFZARiG4JLgx1dHYBX_doc.png?alt=media&token=202f5892-1e5a-4f47-8083-406c349cbaf5)

### 31. View Cluster Overview

![View Cluster Overview](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FjnQjz8tSxtXz61pSSSsWFB_doc.png?alt=media&token=4fe25ac2-27ce-45e2-b07e-d758a1c16917)

### 32. Access VM Distribution by Cluster

![Access VM Distribution by Cluster](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FcmHMzWVTf1NXYXggjUKe99_doc.png?alt=media&token=8a53cdf9-d602-4580-ac7f-a0e39806d700)

### 33. Review Cluster CPU Overcommitment

![Review Cluster CPU Overcommitment](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FbhKaHCrBiK5d2EwT9B4QwU_doc.png?alt=media&token=660f0efe-2dcd-46bb-9281-7db6d3e3f12a)

### 34. Revisit CPU Overcommitment Details

![Revisit CPU Overcommitment Details](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Fk8pmoG8f36b2Y5MQhELrVH_doc.png?alt=media&token=2d790af7-d5dd-4ccb-a3a8-1bded709525c)

### 35. Analyze Cluster Distribution

![Analyze Cluster Distribution](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FjT5XwNLnjGE7KKKwK32gae_doc.png?alt=media&token=159acf97-5c2e-4274-886e-7d9811e8704e)

### 36. Check VM Count by Disk Size

![Check VM Count by Disk Size](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2Fr7iZA1xAV56zfESo5RxqWp_doc.png?alt=media&token=7956c213-10f5-44b7-97c8-817ec072552b)

### 37. Review VM Count by Disk Type

![Review VM Count by Disk Type](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FhCr8WYngiCjfZU3N4koX8C_doc.png?alt=media&token=70034434-2dfd-485f-8472-22a12a2b797a)

### 38. Click "VM count by disk type"

![Click 'VM count by disk type'](https://static.guidde.com/v0/qg%2FQrdIipHdyefgdDSo6nWk2qLNf753%2FcZNzDp6dWjJ5UKdwozk3gc%2FuSi2MWx7QCxjPPk6nEzTsJ_doc.png?alt=media&token=f026e7ad-ab4d-4f84-9a3d-f70c3b310cee)


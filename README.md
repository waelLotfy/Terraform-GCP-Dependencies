# Terraform-GCP-Dependencies
Provisioning Google Cloud infrastructure with Terraform, demonstrating implicit and explicit resource dependencies and infrastructure lifecycle management.

# Terraform Resource Dependencies on Google Cloud

This project demonstrates how **Terraform manages infrastructure dependencies** on **Google Cloud Platform (GCP)** using **Infrastructure as Code (IaC)**.

The configuration provisions Compute Engine virtual machines, static IP
addresses, and Cloud Storage buckets while showcasing both **implicit** and
**explicit** dependency handling, as well as Terraform’s execution graph.

---

## 🛠 Technologies Used

- Terraform (Community Edition)
- Google Cloud Platform (GCP)
- Google Compute Engine
- Google Cloud Storage
- HashiCorp Configuration Language (HCL)
- Google Cloud Shell

---

## 📐 Key Capabilities Demonstrated

- Google Cloud provider configuration
- Infrastructure initialization using `terraform init`
- Parameterization using input variables
- Output values for exposing resource attributes
- Implicit resource dependency management
- Explicit dependency declaration using `depends_on`
- Infrastructure lifecycle management (create, update, destroy)
- Dependency graph visualization

---

## 📂 Project Structure

- `provider.tf` – Google Cloud provider configuration
- `instance.tf` – Compute Engine instance definition
- `variables.tf` – Input variable declarations
- `outputs.tf` – Output values for resource attributes
- `exp.tf` – Explicit dependency configuration
- `.terraform.lock.hcl` – Provider version locking

---

## 🚀 Infrastructure Workflow

### Initialization
- Configured Google Cloud as the Terraform provider
- Initialized the working directory and installed required provider plugins

### Implicit Dependencies
- Created a static external IP address
- Attached the IP to a Compute Engine instance
- Terraform automatically inferred the dependency and ensured correct creation order

### Explicit Dependencies
- Created a Cloud Storage bucket
- Declared an explicit dependency using `depends_on`
- Ensured the VM instance was created only after the bucket existed

### Outputs and Visibility
- Exposed instance identifiers and resource links using output values
- Verified resource creation through the Terraform CLI and Google Cloud Console

### Dependency Visualization
- Generated and inspected Terraform’s dependency graph to understand resource relationships

---

## 🧠 Key Learnings

- How Terraform automatically detects implicit dependencies
- When and why explicit dependencies are required
- How Terraform builds and executes a dependency graph
- How execution order is independent of file or resource declaration order
- Why dependency management is critical for reliable infrastructure automation

---

## 📎 Notes

This project was completed as part of the **Google Cloud Skills Boost**
learning path on Infrastructure as Code with Terraform.


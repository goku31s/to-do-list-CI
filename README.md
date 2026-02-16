# 3-Tier App: GitOps CI (Application Repo)

This is the **Application Repository** for a GitOps-based deployment. It focuses on the Continuous Integration (CI) side of the pipeline.



## 🔄 CI Workflow
1. **Code Push:** Developer pushes changes to this repo.
2. **Build:** GitHub Actions builds the Docker image.
3. **Registry:** Image is pushed to Docker Hub/Google Artifact Registry with a unique Git SHA tag.
4. **Manifest Update:** The pipeline automatically clones the **CD (Manifest) Repository** and updates the image tag in the YAML files.

## 📂 Tech Stack
- **Language:** Python 3.x (Flask)
- **CI Tool:** GitHub Actions
- **Container Registry:** Docker Hub / GCP Artifact Registry

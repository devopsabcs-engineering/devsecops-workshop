# 4 - Adding Additional DevSecOps Controls
In this lab you will reuse workflow templates.
> Duration: 10-15 minutes

References:
- [Gitleaks.io](https://gitleaks.io/)
- [OWASP Dependency-Review GitHub Action](https://github.com/actions/dependency-review-action)
- [CodeQL](https://codeql.github.com/)
- [Microsoft Security DevOps (MSDO)](https://github.com/microsoft/security-devops-action)
- [GitHub Trivy Action](https://github.com/aquasecurity/trivy-action)

## 4.1 Secret Scanning with Gitleaks

1. For Gitleaks Secret Scanning, uncomment this action:
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/0894fb96-77a9-4d16-96ac-b17a20d325f6)
1. Run the pipeline to see
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/db223fc0-ce46-422a-a564-04aa9573dc4a)

## 4.2 Software Composition Analysis with OWASP Dependency Review

1. prerequisite - to avoid error:
```
Do DevSecOps Tasks
Dependency review is not supported on this repository. Please ensure that Dependency graph is enabled along with GitHub Advanced Security on private repositories, see https://github.com/<your-github-repo>/devsecops-workshop/settings/security_analysis
```
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/6a37ed61-fb3e-4a64-adc6-1d9d64e1b51b)
1. Uncomment the actions ```actions/dependency-review-action```
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/8b01c834-a9a5-4316-b2f8-0575828b5dc4)
1. See the pipeline run
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/5a573256-dd04-4783-b91d-18e3016595da)

## 4.3 Static Application Security Test with CodeQL

1. Enable CodeQL in GitHub security settings
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/49a1f30a-7485-4454-bf38-385d19660d32)
3. Be sure to configure the tool
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/c2f5d15e-35dc-408c-9a34-bee0a70647e7)
4. Click Enable CodeQL
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/d21d21dd-a839-4665-8807-9836172fcc1c)
6. After a scan, you should see some security vulnerabilities
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/7bf6aeb6-5f64-4498-ab76-a166bb86c551)
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/d74ea483-e82e-4dcc-aae0-6bab275487d7)

## 4.4 Container Scanning with Microsoft Security DevOps (MSDO)

1. uncomment this trivy action:
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/0166f0c2-8219-4ad4-822e-ccd6bba6d235)
1. and these two actions
![image](https://github.com/devopsshield/devsecops-workshop/assets/112144174/f88b04ad-1408-4b19-8224-a1d5a39c25a4)

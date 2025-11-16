# Risk AI Kubernetes + SOAR Project

## Contenu du projet
- `playbooks/` : playbooks SOAR pour isolation et patching automatique
- `helm/risk-ai-api/` : Helm chart pour déployer l’API IA sur Kubernetes

## Utilisation

### Helm
```bash
helm install risk-ai-api ./helm/risk-ai-api
```

### Playbooks SOAR
- Configurer votre SOAR pour consommer les fichiers YAML dans `playbooks/`
- Le worker peut appeler les playbooks en fonction du score_risque retourné par l’API

## Architecture
- Worker → API IA → Score risque → Playbook SOAR
- API IA déployée via Helm chart sur Kubernetes

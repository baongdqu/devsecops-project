1. Chủ đề:
Thiết kế và triển khai hệ thống DevSecOps & Multi-Environment GitOps tích hợp Observability toàn diện cho ứng dụng Web 3-Tier trên nền tảng Kubernetes

2. Nội dung dự kiến:
- Container hóa và đóng gói ứng dụng Web 3-Tier (React Frontend, Node.js REST API, PostgreSQL, Redis) với Docker và Docker Compose.
- Xây dựng hạ tầng Cloud theo mô hình Infrastructure as Code (IaC) sử dụng Terraform trên nền tảng AWS (VPC, Subnet, Route Table, Security Group).
- Xây dựng quy trình CI/CD tích hợp DevSecOps qua GitHub Actions: chạy Unit Test, quét lỗ hổng bảo mật SAST (SonarQube), quét lỗ hổng image (Trivy), tự động build và push container image lên GitHub Container Registry (GHCR).
- Xây dựng luồng triển khai liên tục GitOps đa môi trường (Dev/Prod) sử dụng Kustomize và ArgoCD với cơ chế Auto-Sync và Self-Healing trên cụm Kubernetes.
- Cấu hình định tuyến lưu lượng Traffic Routing qua NGINX Ingress Controller và tự động cấp phát chứng chỉ SSL/TLS Let's Encrypt bằng Cert-Manager.
- Thiết lập hệ thống giám sát và cảnh báo toàn diện (Full Observability Stack): Prometheus thu thập Metrics, Grafana Loki và Promtail gom log tập trung, Grafana Dashboard trực quan hóa và Alertmanager phát cảnh báo sự cố thời gian thực qua Telegram / Discord.

3. Kết quả dự kiến:
- Source code và cấu hình hạ tầng được quản lý tách biệt qua 2 Git repository theo chuẩn Enterprise GitOps (app-repo và infra-repo).
- Pipeline CI/CD tự động hóa 100%: từ khi lập trình viên push code, hệ thống tự kiểm thử, quét bảo mật, đóng gói Docker và tự động đẩy cập nhật tag sang GitOps repository.
- Hệ thống GitOps (ArgoCD) tự động đồng bộ hóa và duy trì trạng thái mong muốn trên các môi trường Dev và Production độc lập.
- NGINX Ingress hỗ trợ định tuyến HTTP/HTTPS với chứng chỉ SSL được quản lý tự động bởi Cert-Manager.
- Dashboard Grafana giám sát trực quan tài nguyên (CPU, RAM, Latency, Throughput, Logs) và nhận được thông báo cảnh báo qua Telegram/Discord khi hệ thống gặp sự cố hoặc tải cao.

Thông tin nộp bài:
1. Link Google Drive chứa báo cáo, slides: [Điền link Drive của nhóm]
2. Link GitHub chứa mã nguồn:
   - App Repo: https://github.com/baongdqu/devops-webserver
   - GitOps Infra Repo: https://github.com/baongdqu/devops-gitops

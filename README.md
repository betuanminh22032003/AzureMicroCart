# AzureMicroCart

📂 **Week 1 - Tận dụng Azure Free Services**
├── **1.1 Cài đặt (0.5 ngày)**
│   ├─ Docker Desktop + VS Code
│   ├─ Azure CLI (`az login` với student account)
│   └─ Kiểm tra credit: https://www.microsoftazuresponsorships.com/
│       📌 Lưu ý: Tránh dùng Cosmos DB (tốn credit), thay bằng Azure SQL Database (free tier)
├── **1.2 Code 3 Microservices (3 ngày)**
│   ├─ Dùng .NET 8 Minimal API (nhẹ, ít code):
│   │   - UserService: `/users` (GET/POST)
│   │   - CartService: `/cart/{userId}` (GET/PUT)
│   │   - OrderService: `/orders` (POST)
│   ├─ Database: Azure SQL Free Tier (DTU S0)
│   └─ Test nhanh với Swagger UI
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/azure-sql/database/free-services
├── **1.3 Dockerize (1 ngày)**
│   ├─ Viết Dockerfile đơn giản (multi-stage build)
│   └─ Chạy local với `docker-compose.yml`
│       📌 Ví dụ: `docker build -t userservice .`
├── **1.4 Deploy thử (1.5 ngày)**
│   ├─ Tạo Azure Container Registry (ACR) - Free tier
│   ├─ Push 1 image lên ACR (vd: UserService)
│   └─ Deploy lên Azure Container Apps (Free tier)
│       📌 Dùng `az containerapp up` để deploy nhanh
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/container-apps/quickstart-code-to-cloud

📂 **Week 2 - Sử dụng dịch vụ Free**
├── **2.1 API Management (2 ngày)**
│   ├─ Dùng **Azure API Management Developer tier** (Free)
│   ├─ Import OpenAPI từ Swagger
│   └─ Thêm rate limiting (vd: 10 requests/phút)
│       📌 Lưu ý: Developer tier chỉ 1 đơn vị scale
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/api-management/developer-how-to-create-service
├── **2.2 Auth với Azure AD Free (2 ngày)**
│   ├─ Đăng ký App Registration (Free)
│   ├─ Cấu hình JWT Bearer trong .NET Core
│   └─ Test token với Postman
│       📌 Dùng MSAL.js cho frontend (nếu có)
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-v2-netcore-webapi
├── **2.3 Event-Driven đơn giản (1 ngày)**
│   ├─ Dùng **Azure Storage Queue** (Free thay Event Grid)
│   ├─ OrderService gửi message khi tạo đơn
│   └─ CartService lắng nghe và xử lý
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/storage/queues/storage-quickstart-queues-dotnet
└── **2.4 Frontend tối giản (1 ngày)**
    ├─ Dùng Static Web Apps (Free tier)
    └─ Call API qua APIM endpoint
        📚 Tutorial: https://learn.microsoft.com/en-us/azure/static-web-apps/get-started-portal

📂 **Week 3 - Tự động hóa Free Tier**
├── **3.1 GitHub Actions (Free) thay Azure DevOps (2 ngày)**
│   ├─ Build Docker image + Push lên ACR
│   ├─ Deploy lên Container Apps
│   └─ Dùng GitHub Secrets thay Key Vault
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/container-apps/github-actions
├── **3.2 IaC với Bicep (2 ngày)**
│   ├─ Viết template triển khai cả hệ thống
│   └─ Deploy qua `az deployment group create`
│       📌 Ưu tiên resources free tier trong template
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/deploy-cli
├── **3.3 Security cơ bản (2 ngày)**
│   ├─ SonarCloud Free (SAST)
│   ├─ Trivy scan Docker image (miễn phí)
│   └─ NSG block inbound không cần thiết
│       📚 Tutorial: https://aquasecurity.github.io/trivy/v0.18.3/
└── **3.4 Monitoring (1 ngày)**
    ├─ Dùng Application Insights Free tier
    └─ Log Analytics: 5GB data free/tháng
        📚 Tutorial: https://learn.microsoft.com/en-us/azure/azure-monitor/app/azure-web-apps-net-core

📂 **Week 4 - Tối ưu hóa**
├── **4.1 Zero Trust Free (2 ngày)**
│   ├─ Managed Identity cho Container Apps
│   ├─ RBAC phân quyền tối thiểu
│   └─ VNET isolation (nếu credit còn)
│       📚 Tutorial: https://learn.microsoft.com/en-us/azure/container-apps/managed-identity
├── **4.2 Load test miễn phí (1 ngày)**
│   ├─ Dùng k6.io (open-source)
│   └─ Test auto-scaling của Container Apps
│       📚 Tutorial: https://k6.io/docs/
├── **4.3 Chuẩn bị Demo (2 ngày)**
│   ├─ Viết README.md (kiến trúc + screenshot)
│   ├─ Quay video demo (3 phút)
│   └─ Slide tổng hợp (dùng Canva Free)
└── **4.4 Dự phòng (1 ngày)**
    └─ Fix lỗi phát sinh + Tối ưu cost

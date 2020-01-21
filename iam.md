[Home](./readme.md)

# IAM

- cho phép quản lý truy cập của users và resources
- tạo mới user => ko có quyền gì cả
- user mới dc gắn với access key với secret key khi tạo tài khoản với option programmatic access
- access key chỉ sử dụng với cli và sdk. chỉ hiển thị 1 lần khi tạo user. sẽ mất khi xóa và tạo lại
- polices lưu trữ quyền định nghĩa bởi json.
- managed policies tạo bởi aws, ko thể edit
- custom managed policies tạo bởi người dùng, có thể edit
- inline policies là quyền gắn trực tiếp vào user

# Cognito

- Quản lý đăng nhập từ nguồn ngoài aws.
- User pools - user directory, cho phép xác thực user sử dụng OAuth giống mhư fb,google ...
- Identity pools cung cấp truy cập tạm thời tới các service qua aws cli.
- Web identity federation - đảm nhận giao tiếp giữa identity provider (IdP) và ứng dụng
- Identity provider - cung cấp giải pháp xác thực
- SAML là kiểu xác thực của IdP - sử dụng SSO
- OIDC là kiểu xác thực của IdP - sử dụng OAuth

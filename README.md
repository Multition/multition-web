# Multition Web

Technical scaffold cho web Multition. Repo này chỉ thiết lập React, Vite,
TypeScript, lint, build và CI. Chưa có feature, dashboard hoặc design system;
nhóm sẽ triển khai UI riêng trên khung này.

## Chạy local

```bash
cp .env.example .env
npm install
npm run dev
```

## Kiểm tra

```bash
npm run typecheck
npm run lint
npm run build
```

Biến `VITE_API_URL` được chuẩn bị để kết nối với `multition-api` khi nhóm bắt đầu
triển khai API client.

OpenAPI types được sinh từ `multition-api/openapi/openapi.yaml` vào
`src/types/generated/core-api.d.ts`. Không sửa file generated bằng tay.
Sửa contract rồi chạy `npm run contracts:sync` tại API repo. Snapshot được
commit trong web repo để clone và chạy độc lập.

`src/App.tsx` chỉ là bootstrap screen và có thể được thay thế hoàn toàn khi nhóm
bắt đầu thiết kế UI.

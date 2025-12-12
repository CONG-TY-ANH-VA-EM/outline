# Outline – README (Tiếng Việt)

## Giới thiệu

Outline là một nền tảng kiến thức cộng tác nhanh, được xây dựng bằng **React** và **Node.js**. Bạn có thể dùng phiên bản **đám mây** tại https://www.getoutline.com hoặc tự triển khai bản sao của mình.

## Cài đặt

Vui lòng tham khảo tài liệu chi tiết tại [tài liệu hosting](https://docs.getoutline.com/s/hosting/) để triển khai Outline trong môi trường production.

Nếu có thắc mắc hoặc muốn cải thiện tài liệu, hãy tạo một **thread** trong [GitHub Discussions](https://github.com/outline/outline/discussions).

## Phát triển

Có một hướng dẫn ngắn gọn để [cài đặt môi trường phát triển](https://docs.getoutline.com/s/hosting/doc/local-development-5hEhFRXow7) nếu bạn muốn đóng góp, sửa lỗi hoặc thêm tính năng.

### Đóng góp

Outline được duy trì bởi một nhóm nhỏ – chúng tôi rất mong nhận được sự giúp đỡ của bạn!

- **Dịch thuật**: xem file `docs/TRANSLATION.md`.
- **Vấn đề đầu tiên**: các issue có nhãn `good first issue`.
- **Cải thiện hiệu năng** cho server và frontend.
- **Cải thiện tài liệu** và trải nghiệm nhà phát triển.
- **Sửa lỗi** được liệt kê trên GitHub.

Trước khi gửi Pull Request, **hãy thảo luận** với nhóm core bằng cách tạo hoặc bình luận trong một issue trên [GitHub Issues](https://github.com/outline/outline/issues) hoặc tham gia [discussions](https://github.com/outline/outline/discussions).

### Kiến trúc

Để hiểu cách thức hoạt động của dự án, hãy đọc tài liệu kiến trúc tại `docs/ARCHITECTURE.md`.

### Gỡ lỗi

- Trong môi trường phát triển, Outline ghi log đơn giản tới console, mỗi dòng có tiền tố danh mục.
- Trong production, log được xuất dưới dạng JSON.
- Để bật log HTTP, đặt biến môi trường `DEBUG=http`.
- Để bật log cho tất cả danh mục: `DEBUG=*` hoặc cho danh mục cụ thể như `DEBUG=database`.
- Đặt `LOG_LEVEL=debug` hoặc `LOG_LEVEL=silly` để có log chi tiết hơn.

### Kiểm thử

Chúng tôi hướng tới độ phủ kiểm thử đủ cho các phần quan trọng, không yêu cầu 100%.

- Viết test bằng **Jest** và đặt file `.test.ts` cạnh mã nguồn.
- Chạy toàn bộ test: `make test`.
- Chạy test backend trong chế độ watch: `make watch`.
- Chạy test backend: `yarn test:server`.
- Chạy test backend cụ thể trong watch mode: `yarn test path/to/file.test.ts --watch`.
- Chạy test frontend: `yarn test:app`.

### Migration

Outline sử dụng **Sequelize** để quản lý migration.

```bash
# Tạo migration mới
yarn db:create-migration --name my-migration
# Chạy migration
yarn db:migrate
# Hoàn tác migration
yarn db:rollback
```

Đối với database test:

```bash
yarn db:migrate --env test
```

## Hoạt động

![Hoạt động của dự án](https://repobeats.axiom.co/api/embed/ff2e4e6918afff1acf9deb72d1ba6b071d586178.svg "Repobeats analytics image")

## Giấy phép

Outline được cấp phép theo **BSL 1.1** – xem file `LICENSE` để biết chi tiết.

# Tái cấu trúc Landing Page CSS → SASS

Bài tập: Tái cấu trúc mã CSS của các phần Landing Page (Header/Nav, Sản phẩm nổi bật, Số liệu thống kê, Footer) sang SASS.

## Các phần đã hoàn thành

| Phần | File SASS | Mô tả |
|------|-----------|-------|
| 1. Navigation + Header | `layout/_header.scss` | Sticky header, nav, logo, CTA, Hero |
| 2. Sản phẩm nổi bật | `components/_products.scss` | Grid sản phẩm + card |
| 3. Số liệu thống kê | `components/_stats.scss` | 4 cột số liệu |
| 4. Footer | `layout/_footer.scss` | Brand + links + social |

## Cấu trúc thư mục

```
landing-page-sass/
├── scss/
│   ├── abstracts/
│   │   ├── _variables.scss   # Màu, font, spacing, breakpoint...
│   │   └── _mixins.scss      # flex, button, card, respond-to...
│   ├── base/
│   │   ├── _reset.scss
│   │   └── _typography.scss
│   ├── layout/
│   │   ├── _header.scss
│   │   └── _footer.scss
│   ├── components/
│   │   ├── _products.scss
│   │   └── _stats.scss
│   └── main.scss
├── css/styles.css
├── index.html
└── README.md
```

## Tính năng SASS đã áp dụng

- **Variables**: `$color-primary`, `$spacing-xl`, `$bp-md`...
- **Mixins**: `@include btn-primary`, `@include card`, `@include respond-to(md)`
- **Nesting**: `.header { &__nav { a { &:hover { ... } } } }`
- **Partials**: Tách theo chức năng (abstracts / base / layout / components)
- **BEM-like naming**: `.product-card__title`, `.stat-item__number`

## Biên dịch

```bash
npx sass scss/main.scss css/styles.css
npx sass scss/main.scss css/styles.css --watch
```

## Cách chạy

Mở `index.html` trong trình duyệt (hoặc dùng Live Server).

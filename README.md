# Pacifica Sentinel 🌊 `v1.0.0-beta`
> **The Active Liquidity Immune System for Perpetual DEXs**

**Pacifica Sentinel** là một đại lý AI tự trị (Autonomous AI Agent), được thiết kế như một "Hệ thống miễn dịch" cho hệ sinh thái Pacifica. Hệ thống thực hiện giám sát sức khỏe thị trường theo thời gian thực và can thiệp để giảm thiểu rủi ro hệ thống, đảm bảo ổn định giá và bảo vệ người dùng khỏi các điều kiện thị trường tiêu cực.

---

## 🚩 The Problem: Liquidity Fragility

Trong thế giới của các sàn giao dịch hợp đồng tương lai vĩnh cửu (**Perp DEXs**), sự biến động cực hạn thường dẫn đến lỗ hổng thanh khoản. Khi thanh khoản bị mỏng, các vấn đề sau nảy sinh:

* **Oracle Divergence:** Giá trên sàn (Mark Price) lệch đáng kể so với giá thực (Oracle Price), gây thanh lý nhầm.
* **Funding Rate Instability:** "Flash Crashes" làm biến dạng cơ chế Funding, gây chi phí phát sinh vô lý cho người dùng.
* **Systemic Erosion of Trust:** Các sai lệch giá lặp đi lặp lại làm nản lòng các nhà cung cấp thanh khoản (LP) và các quỹ lớn.



---

## 🛡️ Our Solution: The Sentinel Architecture

Sentinel vận hành như một lớp giám sát và thực thi không nghỉ. Nó không chỉ giao dịch vì lợi nhuận; nó giao dịch vì **Sự cân bằng (Equilibrium)**.

### 1. Autonomous Monitoring (The Pulse)
Sử dụng luồng dữ liệu **WebSocket** độ trễ thấp của Pacifica để theo dõi độ lệch giữa Mark Price và Oracle Price. Xác định chính xác các "Lỗi thanh khoản" (Liquidity Glitches) — những bất thường cho thấy sự thất bại của thị trường thay vì các chuyển động hữu cơ.

### 2. The Liquidity Shield (Active Hedging)
Khi phát hiện sai lệch nghiêm trọng (ví dụ: `>0.5%`), Sentinel tự động kích hoạt chiến lược **Delta-Neutral Hedging**:
* **Market Balancing:** Thực hiện lệnh đối ứng qua *Pacifica Python SDK* để hấp thụ biến động và đẩy giá Mark trở lại mốc Oracle.
* **Risk Mitigation:** Chủ động ngăn chặn công cụ thanh lý kích hoạt sai trên các "râu nến" (wicks) nhân tạo.

### 3. Funding Rate Stabilization
Giám sát `next_funding` và cung cấp thanh khoản đối lưu để bình ổn phí, đảm bảo cơ chế hội tụ giá luôn là động lực lành mạnh.

---

## 🗺️ Roadmap & Versioning

### **v1.0.0 (Hackathon Edition) - Current**
- [x] Initial Architecture & Core Logic.
- [x] REST/WebSocket API Integration for real-time price monitoring.
- [x] Price Deviation Analyzer (Mark vs. Oracle).
- [ ] Automated Order Execution via Pacifica SDK.
- [ ] Builder Program integration with `builder_code`.

### **v1.1.0 (Post-Hackathon)**
- [ ] **Multi-Pair Support:** Mở rộng hệ thống miễn dịch cho tất cả các cặp giao dịch.
- [ ] **Dynamic Thresholds:** AI tự điều chỉnh ngưỡng sai lệch dựa trên biến động lịch sử.

---

## 🛠️ Technical Integration

| Component | Technology |
| :--- | :--- |
| **SDK** | Pacifica Python SDK (Official) |
| **Data Source** | `GET /api/v1/info/prices` & WebSocket stream |
| **Infrastructure** | Python Cloud-native (24/7 Uptime) |

---

## 🤝 Connect with Small Piece Labs
*Small solutions, vital impact. 🏗️ Scaling Privacy.*

* **Email:** [smallpiecelabs@gmail.com](mailto:smallpiecelabs@gmail.com)
* **X (Twitter):** [@SmallPieceLabs](https://x.com/SmallPieceLabs)
* **Telegram:** [@platink](https://t.me/platink)
* **YouTube:** [@smallpiecelabs](https://youtube.com/@smallpiecelabs)

---
*Built exclusively for the **Pacifica 2026 Hackathon**.*

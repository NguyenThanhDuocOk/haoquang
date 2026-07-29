<div align="center">
  <h1>🤖 Smart Advisory Chatbot</h1>
  <p>Hệ thống hội thoại thông minh tích hợp LLM & RAG với kiến trúc Microservices</p>

  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/OpenAI_LLM-412991?style=for-the-badge&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
</div>

<br/>

## 🎯 Tổng quan (Overview)
Dự án **Chatbot Tư vấn Thông minh** được phát triển nhằm mục đích cung cấp giải pháp hỗ trợ giải đáp thắc mắc và tư vấn khách hàng tự động, liên tục 24/7. Thay vì sử dụng kịch bản cứng nhắc (Rule-based), hệ thống được ứng dụng công nghệ **Generative AI** kết hợp với kiến trúc **RAG (Retrieval-Augmented Generation)** để đảm bảo chatbot không bị ảo giác (hallucination) và luôn trả lời dựa trên kho dữ liệu tri thức nội bộ chuẩn xác nhất.

## 🏗️ Kiến trúc Hệ thống (Architecture)
Hệ thống được thiết kế theo chuẩn **Microservices**, cho phép dễ dàng mở rộng (scale) và bảo trì độc lập:

1. **API Gateway & Routing (FastAPI):** Tiếp nhận luồng tin nhắn đầu vào, xử lý hàng đợi và phân luồng.
2. **LLM Engine:** Tích hợp mô hình ngôn ngữ lớn (OpenAI / Claude) để phân tích ý định (Intent Recognition) và sinh câu trả lời tự nhiên.
3. **Knowledge Base (Vector Database):** Sử dụng cơ sở dữ liệu Vector (như ChromaDB/Pinecone) để thực hiện quy trình nhúng (Embedding) tài liệu và truy xuất (Retrieve) thông tin bối cảnh.
4. **Memory Management:** Quản lý bối cảnh đoạn hội thoại (Conversation History) để chatbot có khả năng "nhớ" ngữ cảnh trò chuyện với người dùng.

## ✨ Tính năng Nổi bật (Key Features)
- Trả lời ngôn ngữ tự nhiên cực kỳ mượt mà, hiểu thấu đáo ý định người dùng (NLU).
- **Zero-Hallucination:** Nhờ RAG, chatbot chỉ sinh câu trả lời dựa trên tài liệu đã cung cấp.
- Kiến trúc API tối ưu hóa bằng `asyncio`, tốc độ phản hồi cực nhanh dưới 2s.
- Hỗ trợ triển khai nhanh chóng qua **Docker**.

## 🚀 Hướng dẫn Cài đặt (Setup Instructions)

```bash
# 1. Clone dự án
git clone https://github.com/NguyenThanhDuocOk/chatbot.git
cd chatbot

# 2. Cài đặt các thư viện cần thiết
pip install -r requirements.txt

# 3. Cấu hình biến môi trường
cp .env.example .env
# Nhập API Key (OpenAI API, VectorDB, v.v...) vào file .env

# 4. Khởi động server (Mặc định: cổng 8000)
uvicorn main:app --reload
```

## 📈 Định hướng Tương lai
- Tích hợp thêm Voice-to-Text để tư vấn bằng giọng nói.
- Phân tích cảm xúc khách hàng (Sentiment Analysis) để chuyển tiếp cho nhân viên tư vấn con người khi cần.

---
*Được phát triển bởi Nguyễn Thành Được - Mobile Game Playtester & AI Enthusiast.*

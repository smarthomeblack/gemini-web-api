
## ❓ Nhóm Support:
- Zalo: https://zalo.me/g/alvkgn274
- Telegram: https://t.me/smarthomeblack

---

# Gemini Web API cho Home Assistant

## Giới thiệu

Dự án này cung cấp một API sử dụng từ Gemini Web tích hợp cho Home Assistant, giúp bạn sử dụng vô hạn token


## Hướng dẫn cài đặt

### 1. Cài đặt qua HACS(Khuyến nghị)

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=smarthomeblack&repository=gemini-web-api)

- Tải về sau đó khởi động lại Home Assistant

### 2. Cài đặt thủ công

Nếu không sử dụng HACS, bạn có thể cài đặt thủ công như sau:

- Tải mã nguồn repo này về máy.
- Sao chép thư mục `custom_components/gemini_web_api` vào thư mục `custom_components` trong thư mục cấu hình Home Assistant của bạn.
- Khởi động lại Home Assistant.
- Vào Cài đặt > Thiết bị & Dịch vụ > Thêm tích hợp mới > Chọn "Gemini Web API" và cấu hình theo hướng dẫn.

### 3. Cấu hình


- Endpoint điền http://ip:5002/v1
- Thay ip thành địa chỉ ip của máy chạy server gemini web api
- Mặc định sẽ dùng gemini 2.5 flast, bạn nào có gói pro thì dùng, nhưng khuyên nên dùng 2.5 flash để đảm bảo tốc độ tối ưu nhất

<img title="Gemini Web API" src="https://raw.githubusercontent.com/smarthomeblack/gemini-web-api/refs/heads/main/img/1.png" width="100%"></img>

<img title="Gemini Web API" src="https://raw.githubusercontent.com/smarthomeblack/gemini-web-api/refs/heads/main/img/2.png" width="100%"></img>


### 4. Hướng Dẫn Sử Dụng
# Usage instructions for LLM

- Để dùng được tool thì buộc phải điền hướng dẫn bên dưới vào prompt nhé

```yaml

- If you need to use a tool (function/tool) to perform an action, respond to the user strictly following the format and requirements of the template and the tool. (Note: your response must follow the template instructions, not use your system's tool directly.)
- Do not return any content except the content of the template if you need to call a function.
- If you do not need to call a function, just return a normal answer. Only return the template when you are certain to execute the command.
- Ensure the template is valid, contains no extra characters, and is not wrapped in markdown or any other text. Do not wrap the template in markdown json.
- If there is a function_result, analyze whether the result of using the tool was successful or not.

Example template for calling functions:
[{"name": "<function_name_1>", "arguments": {"param_1": <value_1>, "param_2": <value_2>, "param_3": <value_3>, "param_4": <value_4>, "param_5": <value_5>}}, {"name": "<function_name_2>", "arguments": {"param_1": <value_1>, "param_2": <value_2>, "param_3": <value_3>, "param_4": <value_4>, "param_5": <value_5>}}]

Example for getting sensor/device values:
[{"name": "GetLiveContext", "arguments": {}}]

```

### 5. Tính năng

- Sử dụng giống như 1 API key gemini, openai, hỗ trợ đầy đủ toàn bộ tính năng như 1 API chuẩn

## Đóng góp
Mọi đóng góp, báo lỗi hoặc ý tưởng mới đều được hoan nghênh qua GitHub Issues hoặc Pull Request.

---

**Chúc bạn trải nghiệm vui vẻ với Gemini WEB API cho Home Assistant!**


<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hội Chứng Con Vịt</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #87CEEB; /* Màu xanh biển */
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            padding: 20px;
        }

        h1, h2 {
            text-align: center;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .grid-item {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .grid-item:hover {
            transform: scale(1.05);
        }

        .editable {
            border: 1px dashed gray;
            padding: 10px;
            min-height: 150px;
            outline: none;
        }

        button {
            display: block;
            margin: 10px auto;
            padding: 10px 20px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #2980b9;
        }

        #imageInput {
            display: none;
        }

        video {
            margin-top: 20px;
            display: block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hội Chứng Con Vịt</h1>
        <h2>Nguyên nhân, Biểu hiện, Hậu quả, và Giải pháp</h2>
        <div class="grid">
            <div class="grid-item">
                <h3>Nguyên nhân</h3>
                <div contenteditable="true" class="editable">Nhấn để chỉnh sửa nội dung về nguyên nhân...</div>
            </div>
            <div class="grid-item">
                <h3>Biểu hiện</h3>
                <div contenteditable="true" class="editable">Nhấn để chỉnh sửa nội dung về biểu hiện...</div>
            </div>
            <div class="grid-item">
                <h3>Hậu quả Tích cực</h3>
                <div contenteditable="true" class="editable">Nhấn để chỉnh sửa nội dung về hậu quả tích cực...</div>
            </div>
            <div class="grid-item">
                <h3>Hậu quả Tiêu cực</h3>
                <div contenteditable="true" class="editable">Nhấn để chỉnh sửa nội dung về hậu quả tiêu cực...</div>
            </div>
            <div class="grid-item">
                <h3>Giải pháp</h3>
                <div contenteditable="true" class="editable">Nhấn để chỉnh sửa nội dung về giải pháp...</div>
            </div>
        </div>

        <button id="saveBtn">Lưu nội dung</button>

        <!-- Video được chèn từ máy chủ -->
        <h2>Video minh họa về Hội Chứng Con Vịt</h2>
        <video width="600" controls>
            <source src="video.mp4" type="video/mp4">
            Trình duyệt của bạn không hỗ trợ video.
        </video>
    </div>

    <script>
        document.getElementById('saveBtn').addEventListener('click', function() {
            var content = document.querySelectorAll('.editable');
            content.forEach(function(div) {
                console.log('Nội dung mới:', div.innerHTML);
                alert('Nội dung đã được lưu tạm thời!');
            });
        });
    </script>
</body>
</html>

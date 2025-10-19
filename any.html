<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>📋 مشروع PIE - OFPPT Offshore</title>
  <style>
    body {
      background: linear-gradient(120deg, #1e90ff, #f0f8ff);
      font-family: 'Tajawal', sans-serif;
      color: #002b5b;
      margin: 0;
      padding: 0;
    }
    header {
      text-align: center;
      background: #002b5b;
      color: white;
      padding: 20px 0;
      font-size: 22px;
      letter-spacing: 1px;
    }
    .container {
      max-width: 700px;
      background: white;
      margin: 40px auto;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    label {
      font-weight: bold;
      display: block;
      margin-bottom: 6px;
      margin-top: 15px;
    }
    input, textarea, select {
      width: 100%;
      padding: 10px;
      border: 1px solid #b0c4de;
      border-radius: 10px;
      outline: none;
      transition: 0.3s;
      font-size: 15px;
    }
    input:focus, textarea:focus, select:focus {
      border-color: #1e90ff;
      box-shadow: 0 0 5px rgba(30,144,255,0.5);
    }
    textarea {
      resize: none;
      height: 80px;
    }
    button {
      background: #1e90ff;
      color: white;
      border: none;
      border-radius: 10px;
      padding: 12px 25px;
      cursor: pointer;
      font-size: 16px;
      transition: 0.3s;
      margin-top: 20px;
    }
    button:hover {
      background: #005bbb;
    }
    .hidden { display: none; }

    .issue {
      background: #f4f9ff;
      border-radius: 10px;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #dce9ff;
    }

    .admin-btn {
      position: fixed;
      top: 20px;
      left: 20px;
      background: transparent;
      border: none;
      font-size: 26px;
      cursor: pointer;
      color: #fff;
    }
  </style>
</head>
<body>

  <header>
    🧭 منصة جمع مشاكل الطلبة - OFPPT Offshore
  </header>

  <button class="admin-btn" id="adminEye">👁️</button>

  <div class="container">
    <h2>📨 أرسل المشكل الذي تواجهه</h2>
    <form id="issueForm">
      <label>🔢 رقمك (استعمل رقم تسلسلي فقط)</label>
      <input type="number" id="userNumber" required min="1" placeholder="مثال: 12">

      <label>🏫 المؤسسة</label>
      <input type="text" id="school" value="OFPPT - Offshore" readonly>

      <label>📝 وصف المشكل</label>
      <textarea id="problem" placeholder="اكتب هنا المشكل الذي تواجهه..." required></textarea>

      <label>💡 حلول ممكنة (من 1 إلى 3)</label>
      <textarea id="solutions" placeholder="اكتب حلولك المقترحة..." required></textarea>

      <button type="submit">إرسال ✅</button>
    </form>
  </div>

  <!-- لوحة المشرف -->
  <div class="container hidden" id="adminPanel">
    <h2>🧑‍💼 لوحة المشرف</h2>
    <div id="adminArea"></div>
  </div>

  <script>
    const ADMIN_CODE = "pie102";
    const adminEye = document.getElementById("adminEye");
    const adminPanel = document.getElementById("adminPanel");
    const adminArea = document.getElementById("adminArea");
    const form = document.getElementById("issueForm");

    // عند إرسال المشكلة
    form.addEventListener("submit", (e) => {
      e.preventDefault();

      const problem = document.getElementById("problem").value.trim();
      const solutions = document.getElementById("solutions").value.trim();
      const user = document.getElementById("userNumber").value;

      // منع الكلمات الممنوعة
      const banned = ["transport","bus","tobis","tobisat","treq","tronspor"];
      const lower = problem.toLowerCase();
      if (banned.some(w => lower.includes(w))) {
        alert("🚫 يمنع الحديث عن مشكل النقل أو المواضيع المشابهة.");
        return;
      }

      const issue = {
        user: `المستخدم رقم ${user}`,
        school: "OFPPT - Offshore",
        text: problem,
        solutions: solutions,
        date: new Date().toLocaleString()
      };

      const data = JSON.parse(localStorage.getItem("issuesData") || "[]");
      data.push(issue);
      localStorage.setItem("issuesData", JSON.stringify(data));

      alert("✅ تم حفظ المشكلة بنجاح!");
      form.reset();
    });

    // وظيفة عرض لوحة المشرف
    adminEye.addEventListener("click", ()=>{
      const code = prompt("رمز المشرف:");
      if(code === ADMIN_CODE){
        adminPanel.classList.remove("hidden");
        renderAdmin();
        alert("✅ مرحبًا بك أيها المشرف");
        adminPanel.scrollIntoView({behavior:"smooth"});
      } else {
        alert("❌ الكود غير صحيح");
      }
    });

    // عرض الملاحظات وتحميل JSON
    function renderAdmin(){
      const issues = JSON.parse(localStorage.getItem("issuesData") || "[]");
      adminArea.innerHTML = `
        <h3>📋 الملاحظات المسجلة (${issues.length})</h3>
        <button id="downloadJson">💾 تحميل JSON</button>
        <div id="issuesList">
          ${issues.length ? issues.map(i => `
            <div class="issue">
              <p><strong>${i.user}</strong> (${i.date})</p>
              <p>📍 المؤسسة: ${i.school}</p>
              <p>📝 ${i.text}</p>
              <p>💡 حلول: ${i.solutions}</p>
            </div>
          `).join('') : "<p>🚫 لا توجد مشاكل مسجلة بعد.</p>"}
        </div>
      `;

      document.getElementById("downloadJson").addEventListener("click", ()=>{
        const blob = new Blob([JSON.stringify(issues, null, 2)], {type:"application/json"});
        const url = URL.createObjectURL(blob);
        const a = document.createElement("a");
        a.href = url;
        a.download = "issues_ofppt_offshore.json";
        a.click();
        URL.revokeObjectURL(url);
      });
    }
  </script>
</body>
</html>

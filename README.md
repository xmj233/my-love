---

# To You - Romantic Confession Page / 浪漫表白网页

[English](#english) | [中文指南](#中文指南)

---

<a name="english"></a>
## English Description

A beautiful, responsive, static HTML5 confession webpage featuring glassmorphism UI, typewriter text effects, and a floating heart animation.

Since this is a **static page** (no backend database), it uses a clever combination of **LocalStorage** and **Hardcoding** to record the exact moment your partner says "Yes".

### ✨ Features
- **Responsive Design**: Looks great on both mobile and desktop.
- **Glassmorphism UI**: Modern frosted glass aesthetic.
- **Typewriter Effect**: The love letter types itself out character by character.
- **Love Timer**: Calculates how long you've known each other and the duration of your relationship.
- **Heart Animation**: HTML5 Canvas background animation.

### 🚀 How to Use (The Workflow)

This project is designed to be used in two phases.

#### Phase 1: Preparation (Before sending it)

1.  Open `index.html`.
2.  Find the `config` object in the `<script>` section.
3.  **Customize the content**:
    *   `startDate`: Change this to the date you first met.
    *   `letter`: Write your own heartfelt letter. `\n` creates a new line.
    *   `loveStartDate`: **Keep this empty** (`""`) for now.
    ```javascript
    const config = {
        startDate: "2023-01-01", // Date you met
        loveStartDate: "",       // Keep empty for Phase 1
        letter: "Your message here..."
    };
    ```
4.  Deploy this page to GitHub Pages (or Vercel/Netlify).
5.  Send the link to your special someone.

#### Phase 2: The Confession (The Interaction)

1.  When she opens the link, she will see the letter and a "Yes, I Do" button.
2.  **The Moment**: When she clicks the button:
    *   The page transitions to the "Time in Love" timer.
    *   The current timestamp is saved to her browser's `LocalStorage` (so the timer keeps running even if she refreshes).
    *   The exact start time will be displayed on the screen (e.g., `Since: 2025/12/19 00:20:00`).

#### Phase 3: Commitment (Hardcoding the Time)

To make this page permanent for everyone (and to ensure the "Yes" button never appears again):

1.  **Note down the exact time** displayed on the screen after she accepted.
2.  Go back to your local code.
3.  Paste that time string into the `loveStartDate` field:
    ```javascript
    const config = {
        // ...
        loveStartDate: "2025-12-19 00:20:00", // Paste the time here
        // ...
    };
    ```
4.  **Commit and Push** the changes to GitHub.
5.  Now, the page is permanently set to "In Love" mode for anyone who visits it.

---

<a name="中文指南"></a>
## 中文指南

这是一个唯美、响应式的静态表白网页。它采用了毛玻璃（Glassmorphism）风格，包含打字机文字效果和 Canvas 爱心雨动画。

由于这是一个 **静态页面**（没有后端数据库），它使用 **本地存储（LocalStorage）** 配合 **代码硬编码** 的方式来记录并永久保存确立关系的那一刻。

### ✨ 特性
- **响应式设计**：完美适配手机端和电脑端。
- **毛玻璃 UI**：现代感的高级视觉效果。
- **打字机效果**：情书内容逐字显现，深情且具仪式感。
- **爱情计时器**：自动计算相识天数，精确记录相恋时长。
- **爱心动画**：基于 HTML5 Canvas 的背景动态效果。

### 🚀 使用步骤（工作流）

为了实现最佳效果，请按照以下三个阶段操作：

#### 第一阶段：准备工作（表白前）

1.  打开 `index.html` 文件。
2.  在底部的 `<script>` 标签中找到 `config` 配置项。
3.  **修改内容**：
    *   `startDate`: 修改为你们 **相识/相遇** 的日期。
    *   `letter`: 写下你想对她说的情话。使用 `\n` 来换行。
    *   `loveStartDate`: **此时请保持为空字符串** (`""`)。
    ```javascript
    const config = {
        startDate: "2023-01-01", // 你们相识的日期
        loveStartDate: "",       // 第一阶段保持为空
        letter: "这里写你的情书..."
    };
    ```
4.  将代码提交并部署到 GitHub Pages（或其他静态托管服务）。
5.  将链接发给她。

#### 第二阶段：表白时刻（交互）

1.  当她打开链接时，会看到打字机效果的情书和“Yes, I Do”按钮。
2.  **点击确认**：当她点击按钮后：
    *   页面会自动切换为“Time in Love”计时器状态。
    *   确立关系的时间会被立即记录在浏览器的 `LocalStorage` 中（防止刷新丢失）。
    *   屏幕下方会显示具体的开始时间（例如：`Since: 2025/12/19 00:20:00`）。

#### 第三阶段：永久固化（修改代码）

为了让这个网页对所有人都显示为“恋爱中”状态（并且不再显示表白按钮），你需要将那个时间写入代码：

1.  **直接记下屏幕上显示的时间**。
2.  回到你的本地代码，将其填入 `loveStartDate` 字段：
    ```javascript
    const config = {
        // ...
        loveStartDate: "2025-12-19 00:20:00", // 把记下的时间填在这里
        // ...
    };
    ```
3.  **提交（Commit）并推送（Push）** 代码到 GitHub。
4.  大功告成！现在无论谁打开这个链接，都会直接显示属于你们的恋爱计时器。

---

### 🛠️ 技术栈 / Tech Stack
*   HTML5
*   CSS3 (Animations, Flexbox)
*   JavaScript (ES6+)
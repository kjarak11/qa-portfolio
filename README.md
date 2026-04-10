# QA Portfolio – Kristijan

## 👨‍💻 About Me
QA Engineer with hands-on experience in manual and automation testing.  
Focused on betting platforms, KYC flows, payments, and API validation.  
Experienced in identifying issues, writing clear bug reports, and working with developers to resolve defects.

---

## 🧠 Skills
- Manual Testing
- API Testing (DevTools / HAR)
- Automation Testing (Playwright)
- Bug Reporting (Jira-style)
- Network & Request Analysis
- Regression Testing
- Basic SQL

---

## 🛠️ Tools
- Playwright  
- Chrome DevTools  
- Jira  
- Postman  
- Kibana  
- RabbitMQ (basic)

---

## 📁 Projects

---

### 🔹 1. Bug Reports

#### 🐞 Cashdesk Scroll Issue
**Description:**  
When scrolling to the bottom of the cashdesk page, content becomes misaligned or partially hidden.

**Steps to Reproduce:**
1. Open Cashdesk  
2. Scroll to the bottom  

**Expected Result:**  
All elements should remain visible and properly aligned.

**Actual Result:**  
Some elements are hidden or incorrectly positioned.

---

#### 🐞 Ticket Payout Shows Incorrect Info
**Description:**  
After ticket payout, printed ticket still displays "possible winnings".

**Steps to Reproduce:**
1. Create ticket  
2. Pay out ticket  
3. Print ticket  

**Expected Result:**  
Only final payout information should be shown.

**Actual Result:**  
"Possible winnings" is still visible.

---

#### 🐞 Player Creation Modal Keeps Error
**Description:**  
Modal retains previous error message even after reopening.

**Steps to Reproduce:**
1. Open "Create Player"  
2. Trigger validation error  
3. Close modal  
4. Reopen modal  

**Expected Result:**  
Modal should reset.

**Actual Result:**  
Old error is still displayed.

---

#### 🐞 KYC / Terms Issue
**Description:**  
Using player card for a user who hasn’t accepted Terms & Conditions blocks the UI.

**Steps to Reproduce:**
1. Use player card as cashier  
2. Select player without accepted terms  

**Expected Result:**  
User should be prompted to accept terms.

**Actual Result:**  
Nothing is shown; page becomes unusable until refresh.

---

### 🔹 2. Automation Testing (Playwright)

Automated key user flows on a betting platform.

**Covered:**
- Login flow  
- Ticket creation  
- Basic validation  

**Example:**
```javascript
test('User login', async ({ page }) => {
  await page.goto('https://example.com');
  await page.fill('#username', 'test');
  await page.fill('#password', 'password');
  await page.click('#login');
  await expect(page).toHaveURL('/dashboard');
});

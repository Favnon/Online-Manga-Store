# SIA Online Manga (ระบบจำหน่ายมังงะออนไลน์)
โปรเจกต์ระบบจำหน่ายการ์ตูน/มังงะออนไลน์ในรูปแบบ **E-commerce Platform** ครบวงจร ที่ออกแบบมาเพื่อให้ลูกค้าเลือกซื้อหนังสือมังงะที่ต้องการได้อย่างง่ายดาย พร้อมระบบจัดการหลังบ้านที่มีประสิทธิภาพสำหรับพนักงานและผู้ดูแลระบบ
---
## 📖 1. หลักการและเหตุผล (Background & Rationale)
ในยุคปัจจุบันที่เทคโนโลยีก้าวหน้าและอินเทอร์เน็ตเข้ามาเป็นส่วนหนึ่งของชีวิตประจำวัน พฤติกรรมการบริโภคสื่อบันเทิงของคนรุ่นใหม่ โดยเฉพาะ "มังงะ (Manga)" หรือการ์ตูนญี่ปุ่น ได้เปลี่ยนจากการซื้อรูปแบบเล่มกระดาษแบบดั้งเดิมไปสู่ช่องทางออนไลน์ที่รวดเร็วและเข้าถึงง่ายมากขึ้น
อย่างไรก็ตาม ผู้ใช้บริการระบบจำหน่ายออนไลน์ทั่วไปมักประสบปัญหาต่างๆ เช่น ระบบค้นหาสินค้าที่ไม่แม่นยำ ขั้นตอนการสั่งซื้อที่ซับซ้อน ความล่าช้าในการตรวจสอบสถานะคำสั่งซื้อ ตลอดจนความไม่มั่นคงปลอดภัยในการทำธุรกรรมชำระเงิน ในขณะเดียวกัน ฝั่งผู้ดูแลระบบก็มักขาดเครื่องมือหลังบ้านที่มีประสิทธิภาพในการบริหารจัดการสต็อกสินค้าและการติดตามรายการคำสั่งซื้ออย่างเป็นระบบ
คณะผู้จัดทำจึงได้เล็งเห็นถึงโอกาสในการพัฒนา **"ระบบจำหน่ายมังงะออนไลน์ (SIA Online Manga)"** ขึ้น เพื่อแก้ไขปัญหาดังกล่าว โดยพัฒนาแพลตฟอร์มร้านค้าที่ทันสมัย ใช้งานสะดวก ปลอดภัย และมีประสิทธิภาพสูงตามหลัก SLA (Service Level Agreement) ที่ชัดเจน เพื่อตอบสนองความพึงพอใจสูงสุดของผู้อ่าน และช่วยลดข้อผิดพลาดในการดำเนินงานของพนักงาน
---
## 🎯 2. วัตถุประสงค์ของโครงงาน (Project Objectives)
1. เพื่อออกแบบและพัฒนาระบบจำหน่ายมังงะออนไลน์สไตล์ E-commerce ที่ใช้งานง่าย มีฟังก์ชันตะกร้าสินค้า สั่งซื้อสินค้า และช่องทางการชำระเงินที่รวดเร็วและปลอดภัยสำหรับลูกค้า
2. เพื่อพัฒนาแผงจัดการหลังบ้าน (Back-office panel) ที่ช่วยให้พนักงานสามารถแก้ไขข้อมูลมังงะ ตรวจสอบสต็อก และอัปเดตสถานะคำสั่งซื้อของลูกค้าได้อย่างมีประสิทธิภาพ
3. เพื่อสร้างระบบจัดทำรายงานวิเคราะห์ยอดขายและประสิทธิภาพหน้าเว็บสำหรับพนักงานและผู้ดูแลระบบในการติดตามการทำงาน
4. เพื่อศึกษา พัฒนา และติดตั้งระบบที่มีเสถียรภาพและคุณภาพบริการสอดคล้องตามข้อตกลงระดับบริการ (SLA) และแผนการซ่อมบำรุงที่กำหนดไว้
---
## 👥 3. โครงสร้างทีมและบทบาทหน้าที่ (Team Structure & Roles Allocation)
เพื่อประสิทธิภาพสูงสุดในการดำเนินการ สมาชิกในทีมได้รับการแบ่งสัดส่วนความรับผิดชอบหลักตามสายงาน (Role-based) ดังนี้:
* **นาย เมธวิน ปิติสกุลรัตน์ (Project Manager / System Analyst)**
  * *บทบาทหน้าที่*: บริหารจัดการเวลาของโปรเจกต์ วาดแผนภาพโครงสร้างระบบ (Use Case, Class Diagram, Sequence Diagram) รวบรวมความต้องการของระบบ (Requirements) และดูแลขอบเขตการทำงานร่วมกันนน
* **นาย พงศภัค ผิวทอง (Full-stack Developer)**
  * *บทบาทหน้าที่*: ออกแบบและเขียนโค้ดหน้าบ้าน (Frontend UI/UX) ตามแบบ Mockup เชื่อมโยงกับ Backend API ออกแบบฟังก์ชันระบบชำระเงินและตะกร้าสินค้า รวมถึงจัดการระบบความปลอดภัยของบัญชีผู้ใช้งาน
* **นาย ชัยวัฒน์ ธนวัฒน์สิริกุล (Database Administrator / QA Tester)**
  * *บทบาทหน้าที่*: ออกแบบความสัมพันธ์ของฐานข้อมูล (Database Schema) ตรวจสอบความถูกต้องและปรับปรุงความเร็วการคิวรีข้อมูล ทำการทดสอบระบบ (Manual & Automated Testing) และจัดทำรายงานเมื่อพบปัญหาการใช้งาน
---
## 🎨 4. ตัวอย่างหน้าจอระบบ (UI Mockup)
หน้าหลักของระบบจำหน่ายมังงะออนไลน์สไตล์ **Dark Mode + Glassmorphism** ทันสมัย เน้นการแสดงผลการ์ดมังงะโปร่งแสงและการไล่โทนสีทองแดง (Copper) ตัดกับสีดำชาร์โคล
![SIA Online Manga UI Mockup](./assets/manga_store_ui_mockup.jpg)
---
## ⚙️ 5. ขอบเขตของระบบ (System Scope)
ระบบแบ่งขอบเขตและสิทธิ์ของกลุ่มผู้ใช้งานออกเป็น 3 กลุ่มหลัก ดังนี้:
### 5.1 ขอบเขตสำหรับลูกค้า (Customer Area)
* **สมัครสมาชิก (Register)**: ลงทะเบียนเพื่อสร้างบัญชีผู้ใช้ใหม่ในระบบ
* **เข้าสู่ระบบ (Login)**: ยืนยันตัวตนเข้าสู่ระบบก่อนทำรายการซื้อขายหรือดูประวัติส่วนตัว
* **ค้นหามังงะและดูรายละเอียด (Search & View Details)**: ค้นหามังงะตามชื่อ เรื่อง นักเขียน หรือหมวดหมู่ พร้อมแสดงราคา จำนวนคงเหลือ และหน้าปก
* **จัดการตะกร้าสินค้า (Cart Management)**: เลือกมังงะใส่ตะกร้า แก้ไขจำนวนมังงะ หรือคัดสินค้าที่ไม่ต้องการออก
* **สั่งซื้อและชำระเงิน (Order & Payment)**: สั่งซื้อหนังสือมังงะ แนบหลักฐานการโอนเงินหรือชำระผ่านระบบ Payment Gateway
* **ตรวจสอบสถานะ (Track Status)**: ติดตามสถานะจัดส่งสินค้าหรือประวัติคำสั่งซื้อของตนเอง
### 5.2 ขอบเขตสำหรับพนักงาน (Staff Area)
* **จัดการข้อมูลมังงะ (Manage Products)**: เพิ่ม แก้ไข และลบข้อมูลหนังสือมังงะ อัปเดตราคา สต็อก และหมวดหมู่
* **จัดการคำสั่งซื้อ (Manage Orders)**: ตรวจสอบหลักฐานการชำระเงิน อนุมัติออเดอร์ และอัปเดตสถานะจัดส่งสินค้า
* **ดูสถิติและรายงาน (View Reports)**: ดูรายงานสรุปยอดขายรายวัน/รายเดือนเพื่อใช้บริหารจัดส่งสินค้าได้ง่ายขึ้น
### 5.3 ขอบเขตสำหรับผู้ดูแลระบบ (Admin Area)
* **จัดการข้อมูลของระบบ**: สิทธิ์เข้าถึงและจัดการข้อมูลทุกส่วนเทียบเท่าพนักงาน พร้อมทั้งจัดการสิทธิ์การเข้าถึงของบัญชีพนักงานในระบบ
* **แสดงรายงานเชิงลึก (Advanced Reports)**: ดูรายงานสถิติประสิทธิภาพการโหลดเว็บ สถิติการเกิดข้อผิดพลาดของระบบ และความมั่นคงปลอดภัยเพื่อดำเนินการซ่อมบำรุงตาม SLA
---
## 🛠️ 6. เครื่องมือและเทคโนโลยีที่ใช้ (Tools & Technologies)
* **Frontend**: HTML5, Vanilla CSS (เพื่อควบคุมสไตล์สถาปัตยกรรมแบบ Custom), Modern JavaScript (ES6+), React/Vite
* **Backend**: Node.js & Express.js
* **Database**: PostgreSQL (สอดคล้องตามโครงสร้างข้อมูลเชิงสัมพันธ์ใน Class Diagram)
* **Design & Collaboration**: Figma (สำหรับออกแบบ UI และ Wireframe), Miro (สำหรับจัดทำ Diagrams)
* **Testing Tools**: Postman (สำหรับทดสอบ API endpoint), Jest (สำหรับทำ Unit Test), Cypress (สำหรับทำ End-to-End Test)
* **Version Control & Deploy**: Git & GitHub, Render (สำหรับ Deploy Server), Vercel (สำหรับ Deploy Frontend)
---
## 🧪 7. แนวทางการทดสอบระบบ (System Testing Guidelines)
เพื่อรับประกันความเสถียรและป้องกันความเสียหายของระบบ ทีมงานกำหนดแนวทางการทดสอบดังนี้:
1. **Unit Testing**: เขียนสคริปต์ทดสอบฟังก์ชันย่อยทีละโมดูลด้วย **Jest** เช่น ฟังก์ชันการตรวจสอบรูปแบบรหัสผ่านการสมัครสมาชิก, การคำนวณภาษีและค่าส่งในหน้าตะกร้าสินค้า
2. **Integration Testing**: ทดสอบการไหลของข้อมูลและการทำงานร่วมกันระหว่าง API และฐานข้อมูล เช่น เมื่อมีการเปลี่ยนสถานะการจ่ายเงินเป็น "ชำระเงินแล้ว" ระบบจะต้องทำการลดจำนวนมังงะในตารางสต็อก (Stock Count) โดยอัตโนมัติ
3. **End-to-End (E2E) Testing**: ทดสอบการเดินทางของผู้ใช้งานจริงตั้งแต่ต้นจนจบ (User Journey) ผ่านโปรแกรม **Cypress** เพื่อทดสอบว่าผู้ใช้อื่นๆ สามารถทำรายการชำระเงินและสมัครใช้งานได้สมบูรณ์ในทุกขั้นตอน
4. **User Acceptance Testing (UAT)**: ทำแบบฟอร์มการทดสอบจำลอง (Test Case Matrix) เพื่อให้กลุ่มตัวอย่างทดลองใช้งานระบบและแจ้งบั๊ก เพื่อประเมินความสอดคล้องตามความต้องการและขอบเขตงานก่อนส่งมอบจริง
---
## 📊 8. แผนภาพการทำงานของระบบ (System Diagrams)
> [!NOTE]
> GitHub รองรับการแสดงผลรูปภาพไดอะแกรมด้านล่างนี้ผ่าน Mermaid Syntax โดยอัตโนมัติ
### 8.1 แผนภาพยูสเคส (Use Case Diagram)
```mermaid
graph LR
    Customer((ลูกค้า))
    Staff((พนักงาน))
    Admin((ผู้ดูแลระบบ))
    subgraph SIA_Online_Manga ["SIA Online Manga (System Boundary)"]
        UC1("สมัครสมาชิก<br>(Register)")
        UC2("เข้าสู่ระบบ<br>(Login)")
        UC3("ค้นหามังงะ<br>(Search Manga)")
        UC4("ดูรายละเอียดสินค้า<br>(View Details)")
        UC11("แสดงรายงานและสถิติ<br>(View Reports)")
        UC5("เพิ่มสินค้าในตะกร้า<br>(Add to Cart)")
        UC12("จัดการสินค้าในตะกร้า<br>(Manage Cart)")
        UC6("สั่งซื้อสินค้า<br>(Place Order)")
        UC7("ชำระเงิน<br>(Payment)")
        UC8("ตรวจสอบสถานะการสั่งซื้อ<br>(Track Order Status)")
        UC9("จัดการข้อมูลมังงะ/สินค้า<br>(Manage Products)")
        UC10("จัดการคำสั่งซื้อ<br>(Manage Orders)")
    end
    Customer --> UC1
    Customer --> UC2
    Customer --> UC3
    Customer --> UC4
    Customer --> UC5
    Customer --> UC12
    Customer --> UC6
    Customer --> UC8
    Staff --> UC2
    Staff --> UC9
    Staff --> UC10
    Staff --> UC11
    Admin --> UC2
    Admin --> UC9
    Admin --> UC10
    Admin --> UC11
    UC6 -.->|"<<include>>"| UC7
    UC5 -.->|"<<include>>"| UC2
    UC6 -.->|"<<include>>"| UC2
    UC8 -.->|"<<include>>"| UC2
```
### 8.2 แผนภาพคลาส (Class Diagram)
```mermaid
classDiagram
    User <|-- Customer
    User <|-- Employee
    Customer "1" --> "1" Cart : มีตะกร้าสินค้า
    Cart "1" *-- "0..*" CartItem : ประกอบด้วย
    Manga "1" --> "0..*" CartItem : อ้างอิงในรายการตะกร้า
    Customer "1" --> "0..*" Order : ทำการสั่งซื้อ
    Order "1" *-- "1..*" OrderItem : ประกอบด้วย
    Manga "1" --> "0..*" OrderItem : อ้างอิงในรายการสั่งซื้อ
    
    Order "1" --> "1" Payment : ชำระเงินผ่าน
    Employee "1" --> "0..*" SalesReport : ตรวจสอบ/ออกรายงาน
    class User {
        +int userId
        +string username
        +string password
        +string email
        +string phone
        +string userType
        +datetime createdAt
        +login() bool
        +logout() bool
    }
    class Customer {
        +string shippingAddress
        +register() bool
        +viewCart() Cart
        +placeOrder() Order
        +trackOrderStatus(int orderId) string
    }
    class Employee {
        +string department
        +string role
        +manageProduct(Manga manga) bool
        +manageOrder(Order order) bool
        +viewReports() SalesReport
    }
    class Manga {
        +int mangaId
        +string title
        +string author
        +string description
        +double price
        +int stockQuantity
        +string coverImageUrl
        +string category
        +updateStock(int qty) bool
        +updateDetails() bool
    }
    class Cart {
        +int cartId
        +int customerId
        +double totalPrice
        +addItem(int mangaId, int qty) bool
        +removeItem(int mangaId) bool
        +updateQuantity(int mangaId, int qty) bool
        +clearCart() bool
    }
    class CartItem {
        +int cartItemId
        +int cartId
        +int mangaId
        +int quantity
        +double pricePerUnit
    }
    class Order {
        +int orderId
        +int customerId
        +datetime orderDate
        +string status
        +double totalAmount
        +string shippingAddress
        +createOrder() bool
        +updateStatus(string newStatus) bool
    }
    class OrderItem {
        +int orderItemId
        +int orderId
        +int mangaId
        +int quantity
        +double unitPrice
    }
    class Payment {
        +int paymentId
        +int orderId
        +datetime paymentDate
        +string paymentMethod
        +double amount
        +string paymentProofUrl
        +string status
        +processPayment() bool
    }
    class SalesReport {
        +int reportId
        +int generatedBy
        +datetime startDate
        +datetime endDate
        +double totalSales
        +generateReport() bool
    }
```
### 8.3 แผนภาพลำดับขั้นตอนการสั่งซื้อและชำระเงิน (Ordering & Payment Sequence Flow)
```mermaid
sequenceDiagram
    autonumber
    actor Customer as ลูกค้า (Customer)
    participant UI as ระบบหน้าบ้าน (Web/App UI)
    participant Cart as ตะกร้าสินค้า (Cart System)
    participant OrderMgr as ตัวจัดการคำสั่งซื้อ (Order Manager)
    participant OrderDB as ฐานข้อมูลคำสั่งซื้อ (Order Database)
    participant PaymentGW as ระบบชำระเงิน (Payment Gateway / Verification)
    Customer->>UI: 1. กดสั่งซื้อสินค้าจากหน้าตะกร้า (Place Order)
    activate UI
    UI->>Cart: 2. ขอข้อมูลสินค้าและยอดรวม (getCartItems)
    activate Cart
    Cart-->>UI: 3. รายการมังงะ และยอดเงินรวมทั้งหมด
    deactivate Cart
    UI-->>Customer: 4. แสดงหน้าสรุปคำสั่งซื้อและปุ่มชำระเงิน
    deactivate UI
    Customer->>UI: 5. ยืนยันคำสั่งซื้อและเลือกช่องทางชำระเงิน
    activate UI
    UI->>OrderMgr: 6. ร้องขอการสร้าง Order (createOrder)
    activate OrderMgr
    OrderMgr->>OrderDB: 7. บันทึกข้อมูลคำสั่งซื้อ (สถานะ: รอชำระเงิน / Pending)
    activate OrderDB
    OrderDB-->>OrderMgr: 8. ส่งเลขที่ใบสั่งซื้อกลับมา (orderId)
    deactivate OrderDB
    OrderMgr-->>UI: 9. ส่งข้อมูล orderId และ ยอดชำระเงินกลับมา
    deactivate OrderMgr
    UI-->>Customer: 10. แสดงช่องทางการชำระเงินและหน้าแนบหลักฐาน
    deactivate UI
    Customer->>UI: 11. อัปโหลดหลักฐานหรือชำระเงินผ่าน API (Submit Payment)
    activate UI
    UI->>PaymentGW: 12. ส่งข้อมูลยอดเงินและหลักฐานชำระเงิน (processPayment)
    activate PaymentGW
    PaymentGW->>PaymentGW: 13. ตรวจสอบข้อมูลความถูกต้อง (verifyPayment)
    
    alt การชำระเงินถูกต้องสำเร็จ
        PaymentGW->>OrderMgr: 14. อัปเดตสถานะชำระเงินสำเร็จ (updateStatusToPaid)
        activate OrderMgr
        OrderMgr->>OrderDB: 15. บันทึกประวัติและเปลี่ยนสถานะ Order เป็น "ชำระเงินแล้ว (Paid)"
        activate OrderDB
        OrderDB-->>OrderMgr: 16. ยืนยันการบันทึกสำเร็จ
        deactivate OrderDB
        OrderMgr-->>PaymentGW: 17. ตอบรับสถานะสำเร็จ
        deactivate OrderMgr
        PaymentGW-->>UI: 18. ส่งผลชำระเงินสำเร็จ (Payment Success)
        UI-->>Customer: 19. แสดงหน้าจอ "สั่งซื้อสินค้าและชำระเงินสำเร็จ"
    else การชำระเงินไม่ถูกต้อง / ล้มเหลว
        PaymentGW-->>UI: 20. ส่งผลชำระเงินไม่สำเร็จ (Payment Failed)
        UI-->>Customer: 21. แจ้งเตือนข้อผิดพลาดและให้ลองใหม่อีกครั้ง
    end
    deactivate PaymentGW
    deactivate UI
```
---
## 🎯 9. ผลลัพธ์ที่คาดว่าจะได้รับ (Expected Outcomes)
1. ได้รับระบบ e-commerce จำหน่ายมังงะออนไลน์ต้นแบบ (Prototype) ที่มีความมั่นคงปลอดภัยและเสถียรตามเงื่อนไขข้อตกลง SLA
2. พนักงานขายสามารถบันทึกข้อมูลมังงะ อัปเดตราคา สินค้าคงคลัง และตรวจสอบหลักฐานการโอนเงินเพื่อจัดเตรียมสินค้าได้อย่างแม่นยำ
3. ผู้ดูแลระบบและผู้บริหารร้านสามารถตรวจสอบและนำข้อมูลสถิติ/รายงานยอดขายของร้านไปทำการตลาดเพื่อเพิ่มรายได้ในอนาคตได้อย่างถูกต้อง
4. สมาชิกในกลุ่มผู้พัฒนาได้เรียนรู้ขั้นตอนการทำงานและการประสานงานพัฒนาโปรเจกต์ซอฟต์แวร์เสมือนการทำงานจริงในระดับองค์กร
---
## 🛠️ 10. ข้อตกลงระดับการบริการและการบำรุงรักษา (SLA & Maintenance Plan)
### ระดับความรุนแรงของปัญหาและการตอบกลับ (SLA)
* **ระดับ 1**: ระบบล่ม ไม่สามารถเข้าเว็บได้ 
  * *การตอบกลับ*: ภายใน 15 นาที / แก้ไขให้เสร็จสิ้นภายใน 2 ชั่วโมง
* **ระดับ 2**: ไม่สามารถ Login ได้ / ชำระเงินไม่ได้ 
  * *การตอบกลับ*: ภายใน 1 ชั่วโมง / แก้ไขให้เสร็จสิ้นภายใน 6 ชั่วโมง
* **ระดับ 3**: รูปภาพสินค้าไม่ขึ้น ค้นหาสินค้าไม่พบ 
  * *การตอบกลับ*: ภายใน 4 ชั่วโมง / แก้ไขให้เสร็จสิ้นภายใน 24 ชั่วโมง
* **ระดับ 4**: ไม่สามารถแก้ไขข้อความหรือรูปภาพประกอบย่อยได้ 
  * *การตอบกลับ*: ภายใน 12 ชั่วโมง / แก้ไขให้เสร็จสิ้นภายใน 3 วัน
### แผนการบำรุงรักษา (Maintenance Schedule)
* **ทุกวัน**: เคลียร์แคชของระบบ และตรวจสอบสถานะความเสถียรของ API สำหรับช่องทางการชำระเงิน
* **ทุกสัปดาห์**: จัดระเบียบและปรับปรุงประสิทธิภาพของฐานข้อมูล, อัปเดตแพตช์ความปลอดภัยซอฟต์แวร์ระบบ และทดสอบระบบตรวจสอบบัญชีความปลอดภัยของผู้ใช้
* **ทุกเดือน**: อัปเดตและเช็คความถูกต้องของรายการการ์ตูนที่จะออกใหม่ประจำสัปดาห์ และตรวจวิเคราะห์หาสาเหตุหน้าเว็บที่ดาวน์โหลดช้าเกินขีดจำกัดมาตรฐาน
---

# SIA Online Manga (ระบบจำหน่ายมังงะออนไลน์)
โปรเจกต์ระบบจำหน่ายการ์ตูน/มังงะออนไลน์ในรูปแบบ **E-commerce Platform** ครบวงจร ที่ออกแบบมาเพื่อให้ลูกค้าเลือกซื้อหนังสือมังงะที่ต้องการได้อย่างง่ายดาย พร้อมระบบจัดการหลังบ้านที่มีประสิทธิภาพสำหรับพนักงานและผู้ดูแลระบบ
---
## 👥 สมาชิกทีมพัฒนา (Team Members)
* **นาย เมธวิน ปิติสกุลรัตน์**
* **นาย พงศภัค ผิวทอง**
* **นาย ชัยวัฒน์ ธนวัฒน์สิริกุล**
---
## 🎨 ตัวอย่างหน้าจอระบบ (UI Mockup)
หน้าหลักของระบบจำหน่ายมังงะออนไลน์สไตล์ **Dark Mode + Glassmorphism** ทันสมัย เน้นการแสดงผลการ์ดมังงะโปร่งแสงและการไล่โทนสีทองแดง (Copper) ตัดกับสีดำชาร์โคล
![SIA Online Manga UI Mockup](./assets/manga_store_ui_mockup.jpg)
---
## ⚙️ ขอบเขตการให้บริการของระบบ (System Scope)
ระบบแบ่งขอบเขตและฟังก์ชันการทำงานหลักออกเป็น 5 ส่วนสำคัญ:
1. **ระบบสมัครสมาชิกและเข้าสู่ระบบ (Membership & Authentication)**
   * การสมัครสมาชิกสำหรับลูกค้าใหม่ (Register)
   * การเข้าสู่ระบบของ ลูกค้า, พนักงาน และผู้ดูแลระบบ (Login)
2. **ระบบแสดงรายงานและค้นหา (Search & Report System)**
   * ค้นหามังงะตามชื่อ เรื่อง หรือหมวดหมู่ (Search Manga)
   * ดูรายละเอียดสินค้า ราคา และสต็อกสินค้า (View Details)
   * แสดงรายงานยอดขาย สถิติการใช้งาน และหน้าเว็บที่ดาวน์โหลดช้าสำหรับพนักงาน/ผู้ดูแลระบบ (View Reports)
3. **ระบบตะกร้าสินค้า (Shopping Cart System)**
   * เพิ่มสินค้าลงในตะกร้าชั่วคราว (Add to Cart)
   * จัดการสินค้า แก้ไขจำนวน หรือลบมังงะในตะกร้า (Manage Cart)
4. **ระบบสั่งซื้อและชำระเงิน (Order & Payment System)**
   * ดำเนินการสั่งซื้อสินค้าจากตะกร้า (Place Order)
   * การชำระเงินแนบสลิป หรือชำระผ่าน API ช่องทางต่างๆ (Payment)
   * ติดตามและตรวจสอบสถานะการจัดส่งสินค้า (Track Order Status)
5. **ระบบจัดการสินค้าและคำสั่งซื้อ (Management System)**
   * การเพิ่ม/ลบ/แก้ไขข้อมูลมังงะและจำนวนสต็อกคงเหลือ (Manage Products)
   * การอนุมัติการชำระเงินและตรวจสอบสถานะใบสั่งซื้อ (Manage Orders)
---
## 📊 แผนภาพการทำงานของระบบ (System Diagrams)
> [!NOTE]
> GitHub รองรับการแสดงผลรูปภาพไดอะแกรมด้านล่างนี้ผ่าน Mermaid Syntax โดยอัตโนมัติ
### 1. แผนภาพยูสเคส (Use Case Diagram)
แสดงปฏิสัมพันธ์ระหว่างผู้ใช้ (Actors) ทั้ง 3 กลุ่มกับฟังก์ชันหลักของระบบ
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
---
### 2. แผนภาพคลาส (Class Diagram)
แสดงโครงสร้างฐานข้อมูล ความสัมพันธ์เชิงวัตถุ (Inheritance, Composition, Association) ของระบบ
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
---
### 3. แผนภาพลำดับขั้นตอน (Sequence Diagrams)
#### 3.1 ขั้นตอนการสั่งซื้อและชำระเงิน (Ordering & Payment Flow)
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
## 🛠️ ข้อตกลงระดับการบริการและการบำรุงรักษา (SLA & Maintenance Plan)
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

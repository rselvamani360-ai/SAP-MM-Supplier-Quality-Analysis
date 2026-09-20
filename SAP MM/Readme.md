# SAP MM – End-to-End Procurement Process

This section documents my practical SAP MM activities performed during the procurement and material management process. Each transaction is explained briefly along with the corresponding SAP screenshot.

---

# 1. Material Creation – MM01

Material Creation is one of the fundamental activities in SAP MM. A material master is created to maintain the important information required for purchasing, inventory management, material planning, and other business processes.

Using transaction **MM01**, material-related details such as material type, industry sector, base unit of measure, material group, and other organizational or purchasing-related information can be maintained.

In this project, the following raw materials were created and used in the procurement process:

- **RM05 – Industrial Bearing**
- **RM07 – Hex Bolt M12 x 50**
- **RM08 – Flat Washer**
- **RM09 – Metal Bracket**

### RM05 – Industrial Bearing

![RM05 Material Master](MM01%20Rm05.png)

### RM07 – Hex Bolt M12 x 50

![RM07 Material Master](MM01%20Rm07.png)

### RM08 – Flat Washer

![RM08 Material Master](MM01%20Rm08.png)

### RM09 – Metal Bracket

![RM09 Material Master](MM01%20Rm09.png)

---

# 2. Request for Quotation – RFQ

A Request for Quotation (RFQ) is created to obtain price and other commercial details from potential suppliers.

The RFQ allows the purchasing team to communicate the material requirement to multiple vendors and collect their quotations for comparison. This helps in evaluating supplier offers before selecting a suitable vendor.

### RFQ 1

![RFQ 1](RFQ%201.png)

### RFQ 2

![RFQ 2](RFQ%202.png)

### RFQ 3

![RFQ 3](RFQ%203.png)

---

# 3. Vendor Quotation Comparison

Vendor quotation comparison is performed to evaluate the quotations received from different suppliers.

The comparison can be based on factors such as material price, total quotation value, and material-wise pricing differences. This analysis helps identify the lowest quotation for the required materials and supports the purchasing decision.

![Vendor Comparison](Vendor%20Comparison.png)

---
# 4. Purchase Requisition – ME53N

A Purchase Requisition is an internal purchasing request used to communicate the requirement for materials or services.

It represents the initial requirement before the purchasing department proceeds with vendor sourcing and procurement activities. The requisition contains information such as the required material, quantity, delivery requirement, and other purchasing details.

Transaction **ME53N** is used to display the purchase requisition created in SAP.

![Purchase Requisition](Me53n%20Purchase%20Requisition.png)

---

# 5. Purchase Order – ME23N

A Purchase Order is a formal purchasing document issued to the selected supplier for procuring materials or services.

It contains important purchasing information such as vendor details, material, quantity, price, delivery information, and other agreed conditions. The Purchase Order acts as the main reference document for subsequent goods receipt and invoice verification activities.

Transaction **ME23N** is used to display the purchase order.

![Purchase Order](Me23n%20Purchase%20Order.png)

---

# 6. Goods Receipt – MIGO

Goods Receipt is the process of recording the physical receipt of materials against a purchase order.

When materials are received from the supplier, the goods receipt transaction is used to update the inventory and create the corresponding material document. The transaction records information such as received quantity, material, movement type, plant, and storage location.

Transaction **MIGO** is used for goods receipt and material movement processing.

![Goods Receipt](MIGO%20-%20Goods%20Receipt.png)

---

# 7. Material Document – MB03

A Material Document is generated in SAP when a material movement is posted. It records important details such as the material, quantity, movement type, posting date, and other relevant information related to the material movement.

The Material Document acts as a reference for tracking and reviewing the inventory movement created during the procurement process.

![Material Document](MB03%20Display%20Material%20Document.png)

---

# 8. Cancellation of Material Document – MIGO

Material Document Cancellation is used to reverse a previously posted material movement when a correction or reversal is required.

In this practical process, the cancellation reverses the previously posted goods receipt movement. This helps maintain accurate inventory and material movement records in SAP.

![Cancellation of Material Document](A03%20Cancellation%20MIGO.png)

---

# 9. Return Defective Material to Vendor

When received materials are identified as defective or unacceptable, the defective quantity can be returned to the vendor.

The Return Delivery process records the movement of the rejected material back to the supplier and helps maintain accurate inventory records. In this practical scenario, the defective quantity is excluded from the accepted quantity before invoice verification.

![Return Defective Material to Vendor](Defective%20Return%20Product%20To%20vendor.png)

---

# 10. Invoice Verification – MIRO / MIR4

Invoice Verification is performed to verify the supplier invoice against the relevant purchasing and goods receipt information.

In this practical scenario, the accepted quantity after excluding the returned defective quantity is considered for invoice verification. This helps ensure that the invoice corresponds to the quantity accepted from the procurement process.

![Invoice Verification](MIR4%20-MIRO.png)

---

## 🔄 End-to-End SAP MM Procurement Flow

```text
Material Creation
        ↓
Request for Quotation
        ↓
Vendor Quotation & Comparison
        ↓
Purchase Requisition
        ↓
Purchase Order
        ↓
Goods Receipt
        ↓
Material Document
        ↓
Cancellation of Material Document
        ↓
Return Delivery to Vendor
        ↓
Invoice Verification (MIRO)

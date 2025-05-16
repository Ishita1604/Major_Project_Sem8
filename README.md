
# 📘 SmartSale Ltd. — SAP SD Process Standardization

- This project is a custom SAP application developed to streamline the Sales and Distribution (SD) process for SmartSale Ltd., an automobile manufacturing company.
- The system covers customer registration, login, order processing, quotations, invoicing, and administrative workflows, built using ABAP Module Pool Programming, SAP SD Standard Screens, ALV Grids, and SmartForms. SAP played a central role in this project as the core ERP platform.
- It provided the integrated environment needed to manage and optimize SmartSale Ltd.’s sales and distribution processes.

## 📁 Folder Structure


    ZFAG2_SMARTSALE/
    ├── doc/                             # Documentation files (e.g., functional specs)
    │   ├── project_story.md
    │   ├── data_model.md
    │   ├── screen_flow.md
    │   └── test_plan.md
    ├── src/                             # ABAP source components
    │   ├── Types/                       # Type definitions
    │   ├── Fields/                      # Field definitions
    │   ├── Macros/                      # Macro programs
    │   ├── PBO_Modules/                 # Process Before Output modules
    │   ├── PAI_Modules/                 # Process After Input modules
    │   ├── Subroutines/                 # FORM sub-routines
    │   ├── classes/                     # OOP Classes
    │   │   ├── ZCL_CUSTOMER_HANDLER.abap
    │   │   ├── ZCL_ADMIN_HANDLER.abap
    │   │   ├── ZCL_ORDER_PROCESSOR.abap
    │   │   └── ZCL_MAIL_UTILITY.abap
    ├── ddic/                            # Data Dictionary objects
    │   ├── ZFAG2_CUSTOMER.abap          # Customer table
    │   ├── ZFAG2_PROD.abap              # Product table
    │   ├── ZFAG2_ORDER.abap             # Order Header table
    │   ├── ZFAG2_ORDER_ITEM.abap        # Order Items table
    │   └── ZFAG2_QUOTATION.abap         # Quotation table
    ├── bdc/                             # BDC screen recordings and reports
    │   ├── ZG2_RECCUST.abap             # Screen recording for Customer
    │   ├── ZFAG2_BDC_CUST.abap          # BDC for Customer
    │   ├── ZG2_RECPROD.abap             # Product screen recording
    │   ├── ZFAG2_BDC_PRODUCT.abap       # BDC for Product
    │   ├── ZG2_RECORD.abap              # Order header screen recording
    │   ├── ZFAG2_BDC_ORD.abap           # BDC for Order header
    │   ├── ZG2_ORDITEM.abap             # Order item screen recording
    │   ├── ZFAG2_BDC_ORDITEM.abap       # BDC for Order items
    │   ├── ZG2_QUOT.abap                # Quotation screen recording
    │   └── ZFAG2_BDC_QUOT.abap          # BDC for Quotation
    ├── smartforms/                      # SmartForm objects
    │   ├── ZFAG2_SM_INVOICE.abap        # Invoice SmartForm
    │   └── ZFAG2_QUOTATION.abap         # Quotation SmartForm
    ├── smartforms_fm/                   # SmartForm Function Modules
    │   ├── ZFMFAG2_INVOICE_FM.abap      # FM for Invoice
    │   └── ZFMFAG2_QUOTATION_FM.abap    # FM for Quotation
    ├── function_groups/                 # Function Groups
    │   ├── ZFAG2_FG.abap                # For send quotation/invoice
    │   └── ZFG_ZFAG2_ORDER.abap         # For order-related actions
    ├── function_modules/                # Custom Function Modules
    │   ├── ZFM_SEND_FOLLOWUP.abap
    │   ├── ZFM_SEND_CANCELLATION.abap
    │   ├── ZFM_QUOTATION_ACCEPTED.abap
    │   ├── ZFM_QUOTATION_REJECTED.abap
    │   └── ZFM_RESET_CREDENTIALS.abap
    ├── Screens/                         # Dynpro screens
    │   ├── 0100_Login_Screen/
    │   ├── 0200_Registration_Screen/
    │   ├── 0201_Forgot_Password_Screen/
    │   ├── 0202_Change_Password/
    │   ├── 0300_Admin_Screen/
    │   ├── 0400_Customer_Screen/
    │   ├── 0401_ALV_Popup/
    │   ├── 0402_Customer_Popup/
    │   ├── 0403_Admin_Tabstrip_Screen/
    │   ├── 0501_Open_Status/
    │   ├── 0502_Cancelled_Status/
    │   ├── 0503_Completed_Status/
    │   └── 0504_User_Account_Recovery/
    ├── gui_status/                      # GUI status definitions (menus, toolbars)
    ├── gui_title/                       # GUI title bar definitions
    ├── transactions/                    # Custom transaction code definitions
    │   └── ZFAG2_ENTRY.abap             # Main transaction code for entry point
    ├── includes/                        # Include programs
    │   ├── ZFAG2_F01.abap
    │   ├── ZFAG2_I01.abap
    │   ├── ZFAG2_O01.abap
    │   └── ZFAG2_TOP.abap
    ├── LICENSE
    └── README.md                        # Overview of the project


## 📌 Features
- 🔐 **Secure Login System:** Login for both Customers and Admins with password validation and account recovery options.

- 📝 **Customer Registration:** New users can register using a form with security questions and auto-generated Customer ID.

- 📦 **Product Catalog Management:** Admins can view and manage stock, pricing, and unit information for all automobile parts.

- 🛒 **Order Management (ALV Grid):** Customers can view, select, and track their orders with real-time status updates.

- 📧 **Email Notifications:** Automatic email triggers for inquiries, follow-ups, cancellations, quotations, and invoices.

- 🧾 **Quotation & Invoice Generation:** SmartForms used to generate and send professional quotations and invoices in PDF format.

- ✅ **Quotation Actions:** Customers can accept or reject quotations, with changes reflected in order status.

- 📊 **Admin Dashboard:** Tabbed screen to view Open, Cancelled, and Completed Orders with actionable options.

- 🔄 **Stock & Fulfillment Checks:** Order fulfillment based on available product stock with unit and price validation.

- 💡 **Modular OOP Design:** Built using Object-Oriented ABAP and follows SAP naming conventions and modular structure.

- 🔄 **BDC-Based Data Upload:** Customer, product, order, and quotation data populated using BDC techniques — no TMG insertions.

- 🖼️ **SAP GUI Screens:** Custom dynpro screens built to SAP UI standards with intuitive navigation and popups.


## 🧮 Technologies

- SAP ABAP (Module Pool, OOPS)
- ALV Grid Display
- Smartforms
- BDC / LSMW for data load
- SAP Standard SD Screens and Tables


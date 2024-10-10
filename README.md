<div align="center">
	<h2>Custom ERPNext Customizations</h2>
	<p>Open Source, modern, and easy-to-use Software for all organizations.</p>
</div>

## Introduction

This project includes a series of customizations developed for ERPNext, aimed at enhancing functionalities across different modules like Material Request, Stock Entry, Sales Invoice, Purchase Invoice, and Budget management. Additionally, it introduces a Bulk Journal Entry custom doctype to streamline the creation of multiple journal entries.

## Table of Contents
- Material Request
- Sales Invoice
- Purchase Invoice
- Custom Doctypes[Bulk Journal Entry]
- Installation and Setup
- License

## Material Request

### Item Availability During Material Transfer

This customization ensures that users cannot transfer more items than are available in the specified warehouses during a Material Transfer in a Material Request. This feature prevents inventory discrepancies and maintains stock accuracy.

#### Features:
- **Real-time Quantity Calculation:** Automatically calculates available quantity based on requested quantity during material transfers.
- **Validation on Submission:** Upon validation, the script checks if the requested quantity exceeds the available stock.
- **Error Handling:** Displays an error if the requested quantity surpasses the available quantity, prompting users to adjust the request or select a different warehouse.

## Sales Invoice

### Enhanced Sales Invoice Management

This customization improves sales invoice processing by dynamically filtering items and automatically updating fields to prevent errors and ensure consistency.

#### Features:
- **Dynamic Item Group Filtering:** Filters item groups based on the selected invoice type and revenue type, reducing the risk of incorrect item selection.
- **Automatic Clearing of Item Table:** Clears the item table when the invoice type changes to prevent mismatched entries.
- **Cost Center and Accounting Department Propagation:** Automatically populates these fields in the item table based on the values in the parent document.

## Purchase Invoice

### Advanced Purchase Invoice Customizations

Similar to the sales invoice, the purchase invoice is enhanced with features that streamline item group filtering and automatic data propagation.

#### Features:
- **Dynamic Item Group Filtering:** Filters item groups based on invoice and revenue type, ensuring accuracy.
- **Automatic Clearing of Item Table:** Clears the item table on invoice type change, preventing errors.
- **Cost Center and Accounting Department Propagation:** Automatically updates these fields in the item table based on the parent document.

## Custom Doctypes

### Bulk Journal Entry

The Bulk Journal Entry doctype allows users to create multiple journal entries at once, providing a more efficient way to manage financial transactions.

#### Features:
- **Multi-Entry Creation:** Allows users to create a batch of journal entries, reducing repetitive data entry tasks.

## Installation

### Manual Installation

1. [Install bench](https://github.com/frappe/bench).
2. [Install ERPNext](https://github.com/frappe/erpnext#installation).
3. Once ERPNext is installed, add the hrms app to your bench by running

	```sh
	$ bench get-app hrms
	```
4. Then add the custom-erpnext app to your bench by running

	```sh
	$ bench get-app https://github.com/your-repo/custom-erpnext.git
	```
5. After that, you can install the hrms and om_hrms app on the required site by running
	```sh
	$ bench --site sitename install-app custom-erpnext
	```
 
## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

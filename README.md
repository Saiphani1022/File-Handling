# File Handling in Python: E-Commerce Product Management System

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)

## 📋 Overview

This project demonstrates comprehensive file handling techniques in Python for managing e-commerce product data across multiple file formats. It provides a practical implementation of reading, modifying, and writing data to CSV, JSON, and TXT files, making it an excellent learning resource for understanding file I/O operations in real-world applications.

## 🎯 Project Objectives

The system is designed to manage product information efficiently by:
- Loading and parsing data from multiple file formats (CSV, JSON, TXT)
- Performing CRUD operations on product information
- Maintaining data persistence with proper file structure organization
- Implementing automated data backup and recovery mechanisms

## 📊 Dataset Description

The project utilizes a structured e-commerce dataset organized into three main components:

### 1. **Sales Data** (`sales_data.csv`)
- Contains 14-day sales history for products
- Each row represents a unique product identified by SKU (Stock Keeping Unit)
- Columns: `Product_SKU`, `Day1` through `Day14`

### 2. **Product Details** (`product_details/`)
- JSON files containing detailed product attributes
- File naming convention: `details_{SKU}.json`
- Includes specifications, pricing, brand, model, and availability

### 3. **Product Descriptions** (`product_descriptions/`)
- Text files with product descriptions
- File naming convention: `description_{SKU}.txt`
- Contains marketing and descriptive information

## 🏗️ Project Structure

```
File_Handling_Project/
│
├── File_Handling.ipynb          # Main project notebook
├── README.md                     # Project documentation
│
└── mainfolder/                   # Data directory
    ├── sales_data.csv
    ├── product_details/
    │   └── details_{SKU}.json
    └── product_descriptions/
        └── description_{SKU}.txt
```

## 🚀 Features

### Stage 1: Environment Setup and Data Loading
- Import required Python libraries (`os`, `json`, `csv`)
- Load data from multiple file formats
- Explore and validate data structure

### Stage 2: Data Manipulation
- **Add/Update Sales Data**: Modify 14-day sales records
- **Add/Update Product Details**: Edit product specifications and pricing
- **Add/Update Descriptions**: Update product marketing content
- **Unified Update Function**: Streamlined interface for all operations

### Stage 3: Data Persistence
- Automated data dumping to original file formats
- Maintain folder structure integrity
- Ensure data consistency across all file types

## 💻 Technical Implementation

### Key Functions

#### `load_data(main_folder)`
Loads all product data from the specified directory structure.

**Returns:**
- `sales_data`: Dictionary with SKU as keys and 14-day sales list as values
- `product_details`: Dictionary containing product specifications
- `product_descriptions`: Dictionary with product descriptions

#### `update(sku, sales_data, product_details, product_descriptions, **kwargs)`
Updates product information based on provided parameters.

**Parameters:**
- `sku`: Product Stock Keeping Unit
- `sales_data`: Sales data dictionary
- `product_details`: Product details dictionary
- `product_descriptions`: Product descriptions dictionary
- `**kwargs`: Flexible key-value pairs for updates

#### `dump_data(sales_data, product_details, product_descriptions, main_folder)`
Persists all data back to the file system in their respective formats.

## 🛠️ Technologies Used

- **Python 3.7+**
- **Standard Libraries:**
  - `os` - File system navigation and directory management
  - `json` - JSON file parsing and serialization
  - `csv` - CSV file reading and writing
- **Environment:** Jupyter Notebook / Google Colaboratory

## 📦 Installation & Setup

1. **Clone the repository:**
```bash
git clone https://github.com/Saiphani1022/file-handling-project.git
cd File-handling
```

2. **Ensure Python 3.7+ is installed:**
```bash
python --version
```

3. **Launch Jupyter Notebook:**
```bash
jupyter notebook File_Handling.ipynb
```

Or use Google Colaboratory for cloud-based execution.

## 💡 Usage Example

```python
# Import required libraries
import os
import json
import csv

# Load data
sales_data, product_details, product_descriptions = load_data('mainfolder')

# Update a product
update(
    sku='AISJDKFJW93NJ',
    sales_data=sales_data,
    product_details=product_details,
    product_descriptions=product_descriptions,
    name='Updated Product Name',
    price=99.99,
    description='New product description'
)

# Save changes
dump_data(sales_data, product_details, product_descriptions, 'mainfolder')
```

## 🎓 Learning Outcomes

By completing this project, you will gain practical experience in:
- Working with multiple file formats in Python
- Implementing file I/O operations
- Managing directory structures programmatically
- Data serialization and deserialization
- Building data persistence layers
- Handling real-world e-commerce data structures

## 📈 Use Cases

This project demonstrates skills applicable to:
- E-commerce product management systems
- Inventory tracking applications
- Data migration tools
- ETL (Extract, Transform, Load) pipelines
- Product catalog management
- Sales analytics platforms

## 🔧 Best Practices Implemented

- **Error Handling**: Robust file reading and writing operations
- **Code Organization**: Modular function design
- **Data Validation**: Ensuring data integrity across operations
- **Documentation**: Comprehensive docstrings and comments
- **Scalability**: Efficient handling of multiple products

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**Karri Saiphani Reddy**
- GitHub: [@Saiphani1022](https://github.com/Saiphani1022)
- LinkedIn: [Karri Saiphani Reddy](https://www.linkedin.com/in/karri-saiphani-reddy-1b6255266/)
- Location: Hyderabad, India

## 🙏 Acknowledgments

- Project structure inspired by real-world e-commerce data management requirements
- Dataset designed for educational purposes

## 📞 Contact

For questions or feedback, please reach out through:
- GitHub: [@Saiphani1022](https://github.com/Saiphani1022)
- Email: saiphanireddy7777@gmail.com

---

⭐ **Star this repository if you found it helpful!**
ANDROID GETTER AND SETTER
=========================

[![Aubrey Ocenar](https://miro.medium.com/v2/da:true/resize:fill:88:88/0*cHZfkTAAXEIzEvPC)](https://medium.com/@aubreyocenar)


[Aubrey Ocenar](https://medium.com/@aubreyocenar)


Group Activity No. 5

[https://github.com/Bree0321/GroupAct5-Getter-and-Setter](https://github.com/Bree0321/GroupAct5-Getter-and-Setter)

Home Page
---------

```
        btnProductPage.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, ProductPage.class);
            startActivity(intent);
        });
        btnEmployeePage.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, EmployeePage.class);
            startActivity(intent);
        });
        btnBookPage.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, BooksPage.class);
            startActivity(intent);
        });
        btnUniversityPage.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, UniversityPage.class);
            startActivity(intent);
        });
        btnRestaurantPage.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, RestaurantPage.class);
            startActivity(intent);
        });
```

Product Page
------------

```
public class Product {
    private int price;
    private String name;
    public Product() {}
    public Product(int price, String name) {
        this.price = price;
        this.name = name;
    }
    public int getPrice() {
        return price;
    }
    public void setPrice(int price) {
        this.price = price;
    }
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
}
``````
```
        productObject = new Product();
        stringBuilder = new StringBuilder();
        etName = findViewById(R.id.et_name);
        etPrice = findViewById(R.id.et_price);
        btnAddItem = findViewById(R.id.btn_add_item);
        tvResults = findViewById(R.id.tv_results);
        btnAddItem.setOnClickListener(v -> addFunction());
    }
    private void addFunction(){
        productObject.setName(etName.getText().toString());
        productObject.setPrice(Integer.parseInt(etPrice.getText().toString()));
        Log.d("MAIN", "name: " + productObject.getName() + ", prices: " + productObject.getPrice());
        stringBuilder.append("\n\n Name: ").append(productObject.getName());
        stringBuilder.append("\n Price: ").append(productObject.getPrice());
        tvResults.setText(stringBuilder.toString());
    }
``````

Employee Page
-------------

```

public class Employee {
    private String name;
    private  String department;
    public Employee(String name, String department) {
        this.name = name;
        this.department = department;
    }
    public Employee() {}
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    public String getDepartment() {
        return department;
    }
    public void setDepartment(String department) {
        this.department = department;
    }
}
``````
```
        employeeObject = new Employee();
        stringBuilder = new StringBuilder();
        etName = findViewById(R.id.et_name);
        etDepartment = findViewById(R.id.et_department);
        btnAddItem = findViewById(R.id.btn_add_item);
        tvResults = findViewById(R.id.tv_results);
        btnAddItem.setOnClickListener(v -> addFunction());
    }
    private void addFunction(){
        employeeObject.setName(etName.getText().toString());
        employeeObject.setDepartment(etDepartment.getText().toString());
        Log.d("MAIN", "name: " + employeeObject.getName() + ", department: " + employeeObject.getDepartment());
        stringBuilder.append("\n\n Name: ").append(employeeObject.getName());
        stringBuilder.append("\n Department: ").append(employeeObject.getDepartment());
        tvResults.setText(stringBuilder.toString());
    }
``````

Books Page
==========

```
public class Book {
    private String title;
    private String author;
    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }
    public Book() {}
    public String getTitle() {
        return title;
    }
    public void setTitle(String title) {
        this.title = title;
    }
    public String getAuthor() {
        return author;
    }
    public void setAuthor(String author) {
        this.author = author;
    }
}
``````
```
        bookObject = new Book();
        stringBuilder = new StringBuilder();
        etTitle = findViewById(R.id.et_title);
        etAuthor = findViewById(R.id.et_author);
        btnAddItem = findViewById(R.id.btn_add_item);
        tvResults = findViewById(R.id.tv_results);
        btnAddItem.setOnClickListener(v -> addFunction());
    }
    private void addFunction(){
        bookObject.setTitle(etTitle.getText().toString());
        bookObject.setAuthor(etAuthor.getText().toString());
        Log.d("MAIN", "title: " + bookObject.getTitle() + ", author: " + bookObject.getAuthor());
        stringBuilder.append("\n\n Title: ").append(bookObject.getTitle());
        stringBuilder.append("\n Author: ").append(bookObject.getAuthor());
        tvResults.setText(stringBuilder.toString());
    }
``````

University Page
===============

```
public class University {
    private String name;
    private String type;
    public University(String name, String type) {
        this.name = name;
        this.type = type;
    }
    public University() {}
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    public String getType() {
        return type;
    }
    public void setType(String type) {
        this.type = type;
    }
}
``````
```
        universityObject = new University();
        stringBuilder = new StringBuilder();
        etName = findViewById(R.id.et_name);
        etType = findViewById(R.id.et_type);
        btnAddItem = findViewById(R.id.btn_add_item);
        tvResults = findViewById(R.id.tv_results);
        btnAddItem.setOnClickListener(v -> addFunction());
    }
    private void addFunction(){
        universityObject.setName(etName.getText().toString());
        universityObject.setType(etType.getText().toString());
        Log.d("MAIN", "name: " + universityObject.getName() + ", type: " + universityObject.getType());
        stringBuilder.append("\n\n School Name: ").append(universityObject.getName());
        stringBuilder.append("\n Type: ").append(universityObject.getType());
        tvResults.setText(stringBuilder.toString());
    }
``````

Restaurant Page
===============

```
    public class Restaurant {
    private String name;
    private String type;
    public Restaurant(String name, String type) {
        this.name = name;
        this.type = type;
    }
    public Restaurant() {}
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    public String getType() {
        return type;
    }
    public void setType(String type) {
        this.type = type;
    }
}
``````
```
        restaurantObject = new Restaurant();
        stringBuilder = new StringBuilder();
        etName = findViewById(R.id.et_name);
        etType = findViewById(R.id.et_type);
        btnAddItem = findViewById(R.id.btn_add_item);
        tvResults = findViewById(R.id.tv_results);
        btnAddItem.setOnClickListener(v -> addFunction());
    }
    private void addFunction(){
        restaurantObject.setName(etName.getText().toString());
        restaurantObject.setType(etType.getText().toString());
        Log.d("MAIN", "name: " + restaurantObject.getName() + ", type: " + restaurantObject.getType());
        stringBuilder.append("\n\n Restaurant Name: ").append(restaurantObject.getName());
        stringBuilder.append("\n Type: ").append(restaurantObject.getType());
        tvResults.setText(stringBuilder.toString());
    }
``````

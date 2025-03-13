-- Tạo bảng Sinh viên
CREATE TABLE Students (
    student_id VARCHAR(10) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    phone VARCHAR(15)
);

-- Tạo bảng Sách
CREATE TABLE Books (
    book_id INT PRIMARY KEY AUTO_INCREMENT,
    title VARCHAR(200) NOT NULL,
    author VARCHAR(100),
    isbn VARCHAR(13) UNIQUE,
    stock INT DEFAULT 0
);

-- Tạo bảng Nhân viên
CREATE TABLE Staff (
    staff_id VARCHAR(10) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    role VARCHAR(50)
);

-- Tạo bảng Giao dịch mượn sách
CREATE TABLE Loans (
    loan_id INT PRIMARY KEY AUTO_INCREMENT,
    student_id VARCHAR(10),
    book_id INT,
    staff_id VARCHAR(10),
    loan_date DATE NOT NULL,
    return_date DATE,
    status ENUM('Borrowed', 'Returned') DEFAULT 'Borrowed',
    FOREIGN KEY (student_id) REFERENCES Students(student_id),
    FOREIGN KEY (book_id) REFERENCES Books(book_id),
    FOREIGN KEY (staff_id) REFERENCES Staff(staff_id)
);

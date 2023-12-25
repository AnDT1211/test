# day la muc 1

## day la muc 1a

## `Stream` api

# Compiling java

de compile duoc file java ta dung lenh:

```sh
javac -d out App.java
```

# Run file java

```sh
java -cp out App
```

Multi-Module Compilation: đây là 1 kỹ thuật compile nhiều module 1 lúc nhưng với điều kiện: 

- các source file java phải để đúng cấu trúc package
- tất cả các module phải gói thành 1 folder có **tên là tên của module luôn** (module tên `com.abc` thì folder tên com.abc luôn chứ không phân tầng giống package)
- các folder module này phải nằm trong 1 folder tổng (đây là module source path)

ta sẽ dùng 2 option:

- `--module-source-path`: chỉ đến các folder tổng chứa nhiều folder module
- `--module` hay `-m`: chỉ ra cái module nào cần compile, nó sẽ auto compile luôn các module khác cần thiết cho module đang được chỉ ra hoặc compile luôn cái package nào mà module được chỉ ra đang `exports`, `requires`

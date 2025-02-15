### **. `bzip`**

`bzip` is a high-compression tool that compresses files using the Burrows-Wheeler algorithm. It typically creates `.bz` files.

### **Basic Compression Command**:

```bash
bzip filename
```

This compresses `filename` into `filename.bz`.

### **Decompress a `.bz` File**:

```bash
bzip2 -d filename.bz2
```

This decompresses `filename.bz` back to the original `filename`.

### **Other Useful Options**:

- **`k`**: Keep the original file after compression.
    
    ```bash
    bzip2 -k filename
    ```
    
- **`v`**: Verbose mode to show compression details.
    
    ```bash
    bzip2 -v filename
    ```
    

### **`gzip`**

`gzip` is one of the most commonly used compression utilities, especially in Linux. It uses the Lempel-Ziv coding (LZ77) compression algorithm and produces `.gz` files.

### **Basic Compression Command**:

```bash
gzip filename
```

This compresses `filename` into `filename.gz`.

### **Decompress a `.gz` File**:

```bash
gzip -d filename.gz
```

This decompresses `filename.gz` back to the original `filename`.

### **Other Useful Options**:

- **`k`**: Keep the original file after compression.
    
    ```bash
    gzip -k filename
    ```
    
- **`r`**: Recursively compress all files in a directory.
    
    ```bash
    gzip -r /path/to/directory/
    ```
    
- **`v`**: Verbose output, showing compression details.
    
    ```bash
    gzip -v filename
    ```
    

### **`zip`**

`zip` is a file compression and archiving tool that bundles multiple files and compresses them into a single `.zip` file. It’s commonly used for compressing directories or multiple files into one archive.

### **Basic Compression Command**:

```bash
zip archive.zip file1 file2
```

This creates a compressed archive `archive.zip` containing `file1` and `file2`.

### **Compress an Entire Directory**:

```bash
zip -r archive.zip /path/to/directory/
```

This command recursively compresses the entire directory into `archive.zip`.

### **Unzip a `.zip` Archive**:

```bash
unzip archive.zip
```

This extracts all files from `archive.zip`.

### **Other Useful Options**:

- **`e`**: Create a password-protected zip file.
    
    ```bash
    zip -e archive.zip file1 file2
    ```
    
- **`v`**: Verbose mode to show compression progress.
    
    ```bash
    zip -v archive.zip file1 file2
    ```
    
- **`r`**: Recursively add files from a directory.
    
    ```bash
    zip -r archive.zip /path/to/directory/
    ```
    

### **`7z` (7-Zip)**

`7z` is a high-compression tool that supports many formats, such as `.7z`, `.zip`, `.gzip`, and others. It uses the LZMA compression algorithm and is known for high compression ratios.

### **Install `7z` on CentOS**:

First, you need to install the `p7zip` package if it’s not already installed:

```bash
sudo yum install p7zip p7zip-plugins
```

### **Basic Compression Command**:

```bash
7z a archive.7z file1 file2
```

This creates a compressed archive `archive.7z` containing `file1` and `file2`.

### **Compress an Entire Directory**:

```bash
7z a archive.7z /path/to/directory/
```

This command compresses the entire directory into `archive.7z`.

### **Extract a `.7z` Archive**:

```bash
7z e archive.7z
```

This extracts all files from `archive.7z`.

### **Other Useful Options**:

- **`p`**: Password-protect the archive.
    
    ```bash
    7z a -p archive.7z file1 file2
    ```
    
- **`v`**: Split archive into volumes.
    
    ```bash
    7z a -v100m archive.7z file1 file2
    ```
    
    This creates volumes of 100MB chunks of the `archive.7z`.
    
- **`tzip`**: Create a `.zip` archive using `7z`.
    
    ```bash
    7z a -tzip archive.zip file1 file2
    ```
    

### **Summary of Commands**

| Tool | Basic Compression Command | Decompression Command | Archive Extension |
| --- | --- | --- | --- |
| **bzip2** | `bzip2 filename` | `bzip2 -d filename.bz2` | `.bz2` |
| **gzip** | `gzip filename` | `gzip -d filename.gz` | `.gz` |
| **zip** | `zip archive.zip file1 file2` | `unzip archive.zip` | `.zip` |
| **7z** | `7z a archive.7z file1 file2` | `7z e archive.7z` | `.7z` |

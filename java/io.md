#JAVA IO

## 流
- java.io.*

**按照数据流方向**

- 输入流
- 输出流

**按照数据处理的单位**

- 字节流
- 字符流

**按照功能**

- 节点流
- 处理流

>java.io.* 里面的所有流都是继承自下面四个抽象类

        |    字节流    | 字符流
 -------|-------------|:----:|
 输入流  | InputStream | Reader |
 输出流  | OutputStream| Writer |
 
 **字节流 构造函数和方法**
 
 ```
 FileInputStream(File file)
 FileInputStream(String name)
 
 FileOutputStream(File file, boolean append)
 FileOutputStream(String name, boolean append)
 
 int read() throws IOException
 int read(byte[] buffer) throws IOException
 int read(byte[] buffer, int offset, int length) throws IOException 
 void close() throws IOException
 
 int write(int b) throws IOException
 int write(byte[] b) throws IOException
 int write(byte[] b, int offset, int length) throws IOException
 void flush() throws IOException
 void close() throws IOException
 ```
 
 **字符流 方法**
 ```
 int read() throws IOException
 int read(char[] cbuf) throws IOException
 int read(char[] cbuf, int offset, int length) throws IOException
 void close() throws IOException
 ```
 
 类型        |字节流|字符流
 ---------- |-------------|----
 File（文件）| FileInputStream FileOutputStream |FileReader FileWriter
 Memory Array (内存数组) | ByteArrayInputStream ByteArrayOutputStream | CharArrayReader CharArrayWriter
 Memory String(内存字符串)| |StringReader StringWriter 
 Pipe(管道)| PipedInputStream PipedOutputStream | PipedReader PipedWriter
 
 **DataInputStream**
 
 ```
 DataInputStream din = 
      new DataInputStream(new FileInputStream("a.txt"));
 double s = din.readDouble();
 
 DataInputStream din = new DataInputStream(
 		new BufferedInputStream(
 				new FileInputStream("a.txt")));
 din.readDouble();
 
 ```
 
 **缓冲流**
 
 **转换流**
 
 - InputStreamReader
 - OutputStreamWriter
 
 **数据流**

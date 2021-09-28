```
import java.io.BufferedReader
import java.io.InputStreamReader
import java.lang.StringBuilder
import java.util.*

fun main() = with(BufferedReader(InputStreamReader(System.`in`))){
    val n = readLine().toInt()
    for(i in 0 until n){
        val data = readLine().split(" ")
        val stack = Stack<Char>()
        val stringBuilder = StringBuilder()
        data.forEach { st ->
            st.forEach {
                stack.push(it)
            }
            while(stack.isNotEmpty()){
                stringBuilder.append(stack.pop())
            }
            stringBuilder.append(" ")
        }
        println(stringBuilder.toString())
    }
}
```

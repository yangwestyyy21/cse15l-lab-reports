# This is the lab report for lab 4

  link to homepage: [title](https://yangwestyyy21.github.io/cse15l-lab-reports/index.html)
  
## Expected outputs:

![test1](https://user-images.githubusercontent.com/33038975/155639890-224ae17e-3866-4350-b0cd-f95ffdc2593e.png)

Test snippet 1 results would be [`google.com]

![test2](https://user-images.githubusercontent.com/33038975/155639898-a5309eeb-9afe-4956-8cc4-ae4e19f2d42b.png)

Test snippet 2 results would be [a.com, a.com(()), example.com]

![test3](https://user-images.githubusercontent.com/33038975/155639905-c355b12b-4a7f-45fa-bfe3-5682c113b8ab.png)

Test snippet 3 results would be [https://ucsd-cse15l-w22.github.io/]


## Running cases on my code

[Link to MarkdownParse](https://github.com/yangwestyyy21/markdown-parse)

My MarkdownParseTest: 

```import static org.junit.Assert.*;```
import org.junit.*;
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.util.ArrayList;
public class MarkdownParseTest {
    @Test
    public void parse1() throws IOException {
        ArrayList<String> list = new ArrayList<String>();
        list.add("`google.com");
        String file = load("snippet1.md");
        assertEquals(list, MarkdownParse.getLinks(file));
    }
    @Test
    public void parse2() throws IOException {
        ArrayList<String> list = new ArrayList<String>();
        list.add("a.com");
        list.add("a.com(())");
        list.add("example.com");
        String file = load("snippet2.md");
        assertEquals(list, MarkdownParse.getLinks(file));
    }
    @Test
    public void parse3() throws IOException {
        ArrayList<String> list = new ArrayList<String>();
        list.add("https://ucsd-cse15l-w22.github.io/");
        String file = load("snippet3.md");
        assertEquals(list, MarkdownParse.getLinks(file));
    }
    private String load(String words) throws IOException {
		Path fileName = Path.of(words);
	    String contents = Files.readString(fileName);
        return contents;
    }
}

## Running cases on the reviewed code

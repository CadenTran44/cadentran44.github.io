---
layout: project
type: project
image: img/Csym.png
title: "Character Counter"
date: 2025
published: true
labels:
  - Java
  - Text Processing
  - HashMap
summary: "A program that reads a String and counts the frequency of each character."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

This is a program I made in ICS 211 during summer of 2025 and in short is a Java app that counts the frequency of each character in a string, treating upper and lowercase letters as the same. This was built with a HashMap for more efficient tracking, as it demonstrates string manipulation, and basic algorithmic logic. This is good for text analysis and also was a good way for me to learn data structures in Java.

This is the raw code. Just change string "sampleText" to your own text:

```cpp
import java.util.HashMap;
import java.util.Map;

public class CharacterCounter {

    public static Map<Character, Integer> countCharacters(String text) {
        Map<Character, Integer> charCountMap = new HashMap<>();

        for (int i = 0; i < text.length(); i++) {
            char c = Character.toLowerCase(text.charAt(i));

            if (charCountMap.containsKey(c)) {
                int currentCount = charCountMap.get(c);
                charCountMap.put(c, currentCount + 1);
            } else {
                charCountMap.put(c, 1);
            }
        }

        return charCountMap;
    }

    public static void main(String[] args) {
        String sampleText = "Hello World!"; // CHANGE THIS
        Map<Character, Integer> characterCounts = countCharacters(sampleText);

        if (characterCounts != null) {
            System.out.println("Character Frequencies for \"" + sampleText + "\":");
            for (Map.Entry<Character, Integer> entry : characterCounts.entrySet()) {
                System.out.println("'" + entry.getKey() + "': " + entry.getValue());
            }
        } else {
            System.out.println("Error: The countCharacters method returned null.");
        }
    }
}
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).

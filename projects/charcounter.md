---
layout: project
type: project
image: img/javasym.png
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
  <img width="600px" src="../img/charcounterout.png" class="img-thumbnail" >
</div>

CharacterCounter is a Java program I developed in ICS 211 during the summer of 2025. The program takes an input string and analyzes it to determine the frequency of each character, treating uppercase and lowercase letters as equivalent. By using a HashMap to efficiently track character occurrences, the program demonstrates several fundamental programming concepts, including string manipulation, iteration, and the effective use of collections. Users can input any text, and the program would output a clear frequency breakdown of each character.

Beyond its immediate functionality, CharacterCounter can also serve as a learning platform for exploring algorithmic thinking and data structures in Java. It provides hands-on experience with mapping data to keys, counting occurrences, and handling user input dynamically, which are foundational skills in software development. By working with this project, I gained a deeper understanding of designing efficient programs, handling edge cases, and presenting output in a user-friendly format. Overall, I believe it's a simple yet insightful example of how core Java concepts can be applied to solve real-world problems.

**Code Sample:**

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

// Change the string "sampleText" to your own text
```

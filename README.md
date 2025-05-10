#codealpha AI-CHATBOT
It's my 3rd task
import java.util.*;

public class ChatBot {

    private static final Map<String, String> responseMap = new HashMap<>();

    static {
        responseMap.put("hi", "Hello! How can I help you?");
        responseMap.put("hello", "Hi there! What can I do for you?");
        responseMap.put("how are you", "I'm just a bunch of code, but I'm functioning as expected!");
        responseMap.put("what is your name", "I am your friendly chatbot.");
        responseMap.put("bye", "Goodbye! Have a great day!");
    }

    public static String getResponse(String input) {
        input = input.toLowerCase().trim();
        for (String key : responseMap.keySet()) {
            if (input.contains(key)) {
                return responseMap.get(key);
            }
        }
        return "I'm sorry, I don't understand. Can you please rephrase?";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("ChatBot: Hello! I am your virtual assistant. Type 'bye' to exit.");
       
        while (true) {
            System.out.print("You: ");
            String userInput = scanner.nextLine();

            if (userInput.equalsIgnoreCase("bye")) {
                System.out.println("ChatBot: " + responseMap.get("bye"));
                break;
            }

            String response = getResponse(userInput);
            System.out.println("ChatBot: " + response);
        }
        scanner.close();
    }
}
output :
ChatBot: Hello! I am your virtual assistant. Type 'bye' to exit.
You: hey hi
ChatBot: Hello! How can I help you?
You: i want a help in my assignment
ChatBot: I'm sorry, I don't understand. Can you please rephrase?
You: what is your name
ChatBot: I am your friendly chatbot.
You: thanku
ChatBot: I'm sorry, I don't understand. Can you please rephrase?
You: bye
ChatBot: Goodbye! Have a great day!

=== Code Execution Successful ===


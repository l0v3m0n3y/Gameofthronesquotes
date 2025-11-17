# Attackontitanapi
api for gameofthronesquotes.xyz site for game of thrones quotes
# main
```cpp
#include "Gameofthronesquotes.h"
#include <iostream>

int main() {
   Gameofthronesquotes api;

    auto character = api.random_character().then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    character.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```

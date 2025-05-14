# patent-search-agent
Using ADK Java SDK to perform the popular Patent Search (Contextual Search)  use case.

1. Get API KEY from Google AI Studio for your active GCP project
   
2. Set env variables:
   
export GOOGLE_GENAI_USE_VERTEXAI=FALSE
export GOOGLE_API_KEY=AIzaSyB2-DNQcffzdpab5wvlyhF1zoTEoTw44Oc

3. Update the placeholders in the code with values from your project (like PROJECT_ID etc.)

4. Set up AlloyDB for Patents Data by following the codelab below:
   https://codelabs.developers.google.com/patent-search-alloydb-gemini
   
6. Create Cloud Run Function (CRF) to access AlloyDB for patents data (code in this repo)
   Follow codelab step #7 for setting up the CRF for this: [https://codelabs.developers.google.com/patent-search-alloydb-gemini step #](https://codelabs.developers.google.com/patent-search-alloydb-gemini?hl=en#6)

7. Deploy and the CRF endpoint
  
8. In cloud Shell Terminal, navigate into the project folder
   
9. Run the following command to kickoff agent interaction:
   mvn compile exec:java -Dexec.mainClass="cloudcode.patentsearch.web.App"

10. Start interacting with the agent with inputs like:

    Hi.
    
    I want to search about NLP related patents.

    Can you give more details about this patent #*****
   

   

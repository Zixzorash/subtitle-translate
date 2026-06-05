# SRT Translator (Using Gemini API)

This web tool allows you to translate SubRip Subtitle (.srt) files or pasted SRT content into another language using Google's Gemini AI models. The translation process happens entirely in your browser, requiring your own Gemini API key.

---

## English

### Live Demo

**You can access the live version of this tool here:**

**[https://zixzorash.github.io/JAVTH-SUB/](https://zixzorash.github.io/JAVTH-SUB/)**

### Features

*   Translate `.srt` files or pasted SRT text.
*   Supports various Google Gemini models.
*   Client-side processing (your API key stays in your browser).
*   Option to remember API key locally (using browser's Local Storage).
*   Configurable translation parameters (temperature, Top-P, Top-K, etc.).
*   Adjustable request delays and chunking for handling rate limits.
*   Optional proxy support for regions with restricted API access.
*   Manual retry option for specific chunks that fail during translation.
*   Light/Dark theme support.
*   Basic Translation Memory (stores successful translations locally to avoid re-translating identical lines).
*   Language toggle (English/Persian interface).

### How to Use

1.  **Open the Tool:** Go to [https://itsyebekhe.github.io/subtitle-translate/](https://itsyebekhe.github.io/subtitle-translate/).
2.  **Select Input Method:**
    *   **Upload File:** Click the "Upload File" radio button, then drag & drop your `.srt` file onto the designated area or click it to browse.
    *   **Paste Text:** Click the "Paste Text" radio button and paste your complete SRT content into the text area.
3.  **Enter API Key:** Go to the "Settings & API Key" section (you might need to click to expand it). Paste your Google Gemini API key into the "Gemini API Key" field.
    *   You can get an API key from [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   Check the "Remember API key" box if you want your browser to store it locally for future use (use with caution on shared computers).
4.  **Choose Target Language:** Enter the desired target language (e.g., "Spanish", "Japanese", "Persian") in the "Target Language" field. Be specific (e.g., "Brazilian Portuguese" instead of just "Portuguese" if needed).
5.  **(Optional) Configure Advanced Settings:** Expand the "Settings & API Key" section to adjust:
    *   **Gemini Model:** Select the desired AI model. Performance and cost may vary.
    *   **Proxy:** Enable if you are in a region where direct access to the Gemini API is blocked (like Iran). *Requires the proxy URL to be correctly configured.*
    *   **Delays:** Adjust `Base Delay` (between successful requests) and `Quota Delay` (after hitting rate limits). Defaults are generally safe.
    *   **Chunks:** Set how many parts the SRT file should be split into for processing. Higher numbers can sometimes help with very long files or strict rate limits, but increase overhead.
    *   **Generation Parameters:** Fine-tune `Temperature`, `Top-P`, `Top-K`, `Max Output Tokens`, and `Stop Sequences` to control the AI's output style. Hover over or consult Gemini documentation for details. **Modifying these significantly can impact translation quality or cause errors.**
    *   **System Prompt:** Modify the instructions given to the AI model (use with caution).
6.  **Translate:** Click the "Translate" button.
7.  **Progress:** Monitor the progress bar and status text below the form.
8.  **Download / Retry:**
    *   Once complete, a "Download Translated SRT" button will appear. Click it to save the file.
    *   If any chunks failed during the process, "Retry Chunk X" buttons will appear below the download link. Clicking these will attempt to re-translate only that specific failed part using the same settings. The download link will update automatically if a retry is successful.
9.  **Clear Memory (Optional):** Click the trash can icon (<i class="fa fa-trash"></i>) in the header to clear the locally stored translation memory.

### Important Notes

*   **API Key Security:** Your API key is processed in your browser and sent directly to Google (or the proxy). While not stored on any external server by *this tool*, be mindful of browser extensions or local security. Use the "Remember Me" feature cautiously.
*   **API Costs:** Using the Gemini API may incur costs based on your usage. Refer to Google AI pricing.
*   **Rate Limits:** Google enforces rate limits (requests per minute). The tool attempts to handle this with delays, but excessive requests or very large files might still hit limits. Adjusting delays can help.
*   **Translation Quality:** AI translation quality varies depending on the model, language pair, context, and the specific text. Review translations for accuracy.
*   **Browser Storage:** API Key remembrance and Translation Memory use your browser's Local Storage. Clearing your browser data will remove these.

### Troubleshooting / Reporting Issues

*   **Errors during translation:** Check the error message displayed. Ensure your API key is valid and has access to the selected model. If using the proxy, ensure it's operational. Check the browser's developer console (F12) for more detailed error messages (especially network errors).
*   **Incorrect Output:** Try adjusting the "System Prompt" or using a different Gemini model.
*   **File Issues:** Report bugs or suggest improvements via the project's issue tracker (if available, e.g., on GitHub).

### Credits

Created with ❤️ by [IDOL_CHAMP](https://x.com/)

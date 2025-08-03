# Test

## Deploying OpenHands on a Self-Hosted Server

### Prerequisites
- Python 3.10 or higher
- Poetry (for dependency management)
- Git (for version control)

### Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Zwire-code/Test.git
   cd Test
   ```

2. **Install Dependencies**
   ```bash
   poetry install
   ```

3. **Set Up Environment Variables**
   Create a `.env` file in the root directory and add the necessary environment variables:
   ```plaintext
   GITHUB_TOKEN=<your_github_token>
   GITLAB_TOKEN=<your_gitlab_token>
   ```

4. **Run the Application**
   ```bash
   poetry run python app.py
   ```

   By default, the server will run on `http://0.0.0.0:5000`. You can access it from any host.

5. **Configure CORS and Iframes**
   Ensure your server is configured to allow CORS requests and iframes. This can typically be done in the server configuration file (e.g., `vite.config.js` for Vite projects):
   ```javascript
   export default defineConfig({
     server: {
       host: true,
       allowedHosts: true,
       cors: true,
     },
   });
   ```

6. **Access the Application**
   Open your web browser and navigate to `http://localhost:5000` to access the OpenHands application.

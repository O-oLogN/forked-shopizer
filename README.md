<h2>1. Run backend</h2>
<code>docker run -p 8080:8080 shopizerecomm/shopizer:latest</code>

<h2>2. Run the administration tool (requires the java backend to be running)</h2>
<code>docker run -e "APP_BASE_URL=http://localhost:8080/api" -p 80:80 shopizerecomm/shopizer-admin</code>
</br>

<h3>Access: Once the site is running, you can access it at http://localhost:80.</h3>
<p><code>username</code>: admin@shopizer.com</p>
<p><code>password</code>: password</p>

<h2>3. Run React Shop Sample Site (requires the Java backend to be running)</h2>

<p>The React Shop sample site interacts with the backend API to retrieve and display products, handle customer authentication, and process orders. Without the backend running, the frontend will not be able to fetch necessary data or execute actions.</p>

<code>docker run -e "APP_MERCHANT=DEFAULT" -e "APP_BASE_URL=http://localhost:8080" -p 81:80 shopizerecomm/shopizer-shop-reactjs</code>

<p>Access: Once the site is running, you can access it at http://localhost:81.</p>

API documentation:
https://app.swaggerhub.com/apis-docs/shopizer/shopizer-rest-api/3.0.1#/

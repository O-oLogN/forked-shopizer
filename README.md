1. Run backend:
docker run -p 8080:8080 shopizerecomm/shopizer:latest

2. Run the administration tool
⋅⋅⋅ Requires the java backend to be running

docker run -e "APP_BASE_URL=http://localhost:8080/api" -p 80:80 shopizerecomm/shopizer-admin

Access: Once the site is running, you can access it at http://localhost:80.
username: admin@shopizer.com
password: password

3. Run React Shop Sample Site
⋅⋅⋅ Requires the Java backend to be running.

Reason: The React Shop sample site interacts with the backend API to retrieve and display products, handle customer authentication, and process orders. Without the backend running, the frontend will not be able to fetch necessary data or execute actions.

Ensure the backend is running using the steps outlined in the previous section.
Run the following Docker command to start the React Shop sample site:
docker run -e "APP_MERCHANT=DEFAULT" -e "APP_BASE_URL=http://localhost:8080" -p 81:80 shopizerecomm/shopizer-shop-reactjs
Access: Once the site is running, you can access it at http://localhost:81.

API documentation:
https://app.swaggerhub.com/apis-docs/shopizer/shopizer-rest-api/3.0.1#/

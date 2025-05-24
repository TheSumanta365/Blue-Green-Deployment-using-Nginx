# Local Blue-Green Deployment with Docker and Nginx

This is a sample project demonstrating how to perform Blue-Green Deployment locally using Docker and Nginx.

## How to Use

### Step 1: Build both app images

```bash
docker build -t blue-app ./app_blue
docker build -t green-app ./app_green
Step 2: Start the services

docker-compose up -d
Step 3: Visit
Open your browser and go to: http://localhost

You will see the Blue app by default.

Step 4: Switch between Blue and Green
Edit nginx/nginx.conf

Comment out the blue-app line.

Uncomment the green-app line.

Then restart nginx:

docker-compose restart nginx
Now you’ll see the Green app!

✅ Blue-Green deployment lets you test new versions (Green) without affecting the live (Blue) environment and switch instantly when ready.
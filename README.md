The project contains four containers, the Nginx, prometheus and altermanger containers that were required and a 4th container running nginx-prometheus-exporter which was added
to stop parsing errors when prometheus checks the status of nginx. Prometheus is set to check http://host.docker.internal/metrics which redirects to
http://host.docker.internal:9113/metrics .

Changes/Improvements <br />
The first major change would be to create the images from an alpine version. This would reduce the size of the nginx image by around 80%.
Second building the nginx container to include and run the ngionx-prometheus-exporter would allow dropping of one container and not require an extra port open.

Nginx Prometheus exporter : https://github.com/nginxinc/nginx-prometheus-exporter

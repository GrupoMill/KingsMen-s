web: gunicorn setup.wsgi:application \
  --bind 0.0.0.0:$PORT \
  --workers 2 \
  --access-logfile '-' \
  --error-logfile '-' \
  --log-level info \
  --capture-output \
  --enable-stdio-inheritance \
  --timeout 120 \
  --preload \
  --forwarded-allow-ips '*' \
  --secure-scheme https \
  --secure-proxy-ssl-header X-Forwarded-Proto \
  --static-map /static= /static/ \
  --static-map /media= /media/ \
  --check-config

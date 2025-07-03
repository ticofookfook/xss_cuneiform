# Usar com ffuf
ffuf -u "http://target.com/search?q=FUZZ" -w xss_cuneiform.txt -mc 200 -fs 1234

# Para POST requests
ffuf -u "http://target.com/search" -X POST -d "query=FUZZ" -w xss_cuneiform.txt -mc 200

# Com headers customizados
ffuf -u "http://target.com/api/search" -H "Content-Type: application/json" -d '{"q":"FUZZ"}' -w xss_cuneiform.txt

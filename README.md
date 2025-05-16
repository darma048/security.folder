# security.folder
Here is a digital security project that I designed myself
# Contoh: Gunakan API ip-api.com (gratis)
import requests

def get_location_from_ip(ip_address):
    response = requests.get(f"http://ip-api.com/json/{ip_address}").json()
    if response["status"] == "success":
        return {
            "city": response["city"],
            "country": response["country"],
            "lat": response["lat"],
            "lon": response["lon"]
        }
    return None

# Contoh pemakaian:
user_ip = "192.158.1.38"  # Ganti dengan IP request login
location = get_location_from_ip(user_ip)
print(f"Lokasi login: {location}")

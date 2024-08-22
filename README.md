import math

# Öklid Hesaplama
#1.adım euclideanDistance adında bir fonksiyon tanımladım.
#Burada pointlerin karelerinin çıkarılıp iki kenarın toplanıp karekökünün alınmasını belirttim.
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0])**2 + (point2[1] - point1[1])**2)

# 2. adım Points adında bir liste oluşturdum.
points = [(1, 2), (4, 6), (5, 8), (2, 1), (7, 3)]

# Mesafeleri saklayacak liste oluşturdum.
distances = []

# Tüm nokta çiftleri arasındaki mesafeleri hesaplama
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Minimum mesafeyi bulma
min_distance = min(distances)

# Sonucu yazdırma
print("Minimum mesafe:", min_distance)


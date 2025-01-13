# min-oklid-mesafe
Minimum Öklid mesafesinin hesaplanması için python kodu
import math

# Noktaların tanımlanması
points = [(1, 2), (4, 6), (7, 8), (2, 1)]

# Öklid mesafesini tanımlayan bir fonksiyon tanımlama
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0])**2 + (point2[1] - point1[1])**2)

# Mesafelerin hesaplanması
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        point1 = points[i]
        point2 = points[j]
        distance = euclideanDistance(point1, point2)
        distances.append(distance)

# Minimum mesafenin hesaplanması ve yazdırılması
min_distance = min(distances)
print(f"The minimum distance is {min_distance:.2f}")

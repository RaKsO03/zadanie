pensje = [4200, 5100, 4800, 4500, 4700, 5300, 4900, 35000, 4400]
n = len(pensje)

for i in range(n - 1):
    for j in range(n - 1 - i):
        if pensje[j] > pensje[j + 1]:
            pensje[j], pensje[j + 1] = pensje[j + 1], pensje[j]
    print(pensje)

srednia = sum(pensje) / n
mediana = pensje[n // 2]
rozstep = max(pensje) - min(pensje)
licznik = 0

for p in pensje:
    if p < srednia:
        licznik += 1

print("Minimum:", min(pensje))
print("Maksimum:", max(pensje))
print("Srednia:", srednia)
print("Mediana:", mediana)
print("Rozstep:", rozstep)
print("Ponizej sredniej:", licznik)
print("Srednia bez prezesa:", (sum(pensje) - max(pensje)) / (n - 1))

pensje.append(6000)

n = len(pensje)
for i in range(n - 1):
    for j in range(n - 1 - i):
        if pensje[j] > pensje[j + 1]:
            pensje[j], pensje[j + 1] = pensje[j + 1], pensje[j]

print("Nowa mediana:", (pensje[n // 2 - 1] + pensje[n // 2]) / 2)

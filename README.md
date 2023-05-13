- 👋 Hi, I’m @togar12
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
togar12/togar12 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---->


import time

# Fungsi untuk menghitung faktorial
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

# Fungsi untuk menghitung deret Taylor sin(x)
def sin_taylor(x, n):
    result = 0
    for i in range(n):
        sign = (-1) ** i
        term = x ** (2*i + 1) / factorial(2*i + 1)
        result += sign * term
    return result

# Menghitung nilai sin(1) menggunakan deret Taylor hingga 10000 suku
start_time = time.time()
result = sin_taylor(1, 10000)
end_time = time.time()

print("Hasil:", result)
print("Waktu yang dibutuhkan:", end_time - start_time, "detik")

# MiPrimerModulo

def Suma5(a, b, c, d, e):
    return a + b + c + d + e

def Potencia5(a, b, c, d, e):
    return a**2, b**2, c**2, d**2, e**2

def Raiz5(a, b, c, d, e):
    return math.sqrt(a), math.sqrt(b), math.sqrt(c), math.sqrt(d), math.sqrt(e)

def Varianza5(a, b, c, d, e):
    data = [a, b, c, d, e]
    return statistics.variance(data)

def asimetria_curtosis5(a, b, c, d, e):
    data = [a, b, c, d, e]
    media = statistics.mean(data)
    varianza = statistics.variance(data)
    momentos = [(x - media)**3 for x in data]
    asimetria = sum(momentos) / (len(data) * varianza**1.5)
    momentos = [(x - media)**4 for x in data]
    curtosis = sum(momentos) / (len(data) * varianza**2)
    return asimetria, curtosis

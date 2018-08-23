# Taller_1_PBG3
Primer taller programación básica. 

def calcular_precio_producto(coste_producto):
    '''
    (num) -> num

    Calcular el precio de un producto

    >>> calcular_precio_producto(100)
    150.0

    >>> calcular_precio_producto(500)
    750.0

    :param coste_producto: Costo neto del producto
    :return: Prcecio total del producto
    '''

    return coste_producto + (coste_producto*0.5)

def calcular_precio_servicio(cantidad_horas):

    '''
    (num) -> num

    Calcula el precio total del servicio

    >>> calcular_precio_servicio(50)
    5000000

    >>> calcular_precio_servicio(40)
    4000000

    :param cantidad_horas: Cantidad de horas laboradas
    :return: Precio total por servicio
    '''

    return cantidad_horas*100000

def calcular_precio_servicio_extras(cantidad_horas):
    """
    (num) -> num
    Calcula el precio de servicio por cada hora extra

    >>> calcular_precio_servicio_extras(10)
    1250000.0

    >>> calcular_precio_servicio_extras(30)
    3750000.0

    :param cantidad_horas: Horas laboradas
    :return: Precio por servicio de horas extra
    """
    return calcular_precio_servicio(cantidad_horas)+(calcular_precio_servicio(cantidad_horas)*0.25)

def calcular_costo_envio(kilometros):
    '''
    (num) -> num
    Calcula el costo de envío

    >>> calcular_costo_envio(5)
    575

    >>> calcular_costo_envio(10)
    1150

    :param kilometros: Kilometros a recorrer
    :return: Costo de envio productos
    '''
    return kilometros * 115

def calcular_precio_producto_fuera(coste_producto,kilometros):
    '''
    (num, num) -> num

    Calcular el precio de producto enviados fuera de la ciudad

    >>> calcular_precio_producto_fuera(4, 6)
    696.0

    :param coste_producto: Valor del producto
    :param kilometros: Kilometros recorridos fuera de la ciudad
    :return: Precio del prodcuto fuera de la ciudad
    '''

    return calcular_precio_producto(coste_producto) +  calcular_costo_envio(kilometros)

def calcular_iva_producto(coste_producto, tasa):
    '''
    (num,num) -> num

    Calcula el IVA del producto

    >>> calcular_iva_producto(15, 14)
    3.1500000000000004

    :param coste_producto: Valor del producto
    :param tasa: IVA establecido del producto
    :return: IVA del producto
    '''

    return (calcular_precio_producto(coste_producto) * (tasa/100))

def calcular_iva_servicio(cantidad_horas, tasa):
    '''
    (num, num) -> num

    Calcula el iva del servicio

    >>> calcular_iva_servicio(3, 15)
    45000.0

    :param cantidad_horas: Horas laboradas
    :param tasa: IVA estipulada
    :return: IVA del servivio
    '''
    return calcular_precio_servicio(cantidad_horas)*(tasa/100)


def calcular_iva_envio(kilometros, tasa):
    '''
    (num, num) -> num

    Calcula el iva de envío

    >>> calcular_iva_envio(6, 15)
    103.5

    :param kilometros: kilometros recorridos
    :param tasa: IVA estipulado
    :return: IVA delñ envío
    '''

    return calcular_costo_envio(kilometros) * (tasa/100)


def calcular_iva_servicio_fuera(cantidad_horas, tasa, kilometros):
    '''
    (num. num, num) -> num

    Calcula el IVA de servicio por fuera

    >>> calcular_iva_servicio_fuera(10, 15, 40)
    150690.0

    :param cantidad_horas: Cantidad de horas trabajadas
    :param tasa: IVA tasa definida
    :return: Iva del servicio fuera
    '''

    return (calcular_precio_servicio(cantidad_horas) + calcular_costo_envio(kilometros)) * (tasa/100)

def calcular_recaudo_locales(coste_producto_1, coste_producto_2, coste_producto_3):
    '''
    (num, num, num) -> num

    Calcula el recaudo local

    >>> calcular_recaudo_locales(4, 6, 7)
    25.5

    :param coste_producto_1: Valor producto 1
    :param coste_producto_2: Valor producto 2
    :param coste_producto_3: Valor producto 3
    :return: Calcula el recaudo local
    '''

    return calcular_precio_producto(coste_producto_1) + calcular_precio_producto(coste_producto_2) + calcular_precio_producto(coste_producto_3)

def calcular_recaudo_horas_extra(horas_1, horas_2, horas_3, horas_4):
    '''
    (num, num, num, num) -> num

    >>> calcular_recaudo_horas_extra(4, 6, 5, 8)
    2875000.0

    :param horas_1: Horas 1
    :param horas_2: Horas 2
    :param horas_3: Horas 3
    :param horas_4: Horas 4
    :return: Recaurdo horas extras
    '''

    return calcular_precio_servicio_extras(horas_1) + calcular_precio_servicio_extras(horas_2) + \
           calcular_precio_servicio_extras(horas_3) + calcular_precio_servicio_extras(horas_4)


def calcular_recaudo_mixto_local(coste_producto_1,
                                 coste_producto_2,
                                 horas_1,
                                 horas_2):
    pass

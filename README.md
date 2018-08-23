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
    

def calcular_precio_producto_fuera(coste_producto,
                                   kilometros):
    pass


def calcular_iva_producto(coste_producto, tasa):
    pass


def calcular_iva_servicio(cantidad_horas, tasa):
    pass


def calcular_iva_envio(kilometros, tasa):
    pass


def calcular_iva_servicio_fuera(cantidad_horas, tasa):
    pass


def calcular_recaudo_locales(coste_producto_1,
                             coste_producto_2,
                             coste_producto_3):
    pass

def calcular_recaudo_horas_extra(horas_1,
                                 horas_2,
                                 horas_3,
                                 horas_4):
    pass


def calcular_recaudo_mixto_local(coste_producto_1,
                                 coste_producto_2,
                                 horas_1,
                                 horas_2):
    pass

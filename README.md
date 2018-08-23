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
    0

    >>> calcular_costo_envio(10)
    0

    :param kilometros: Kilometros a recorrer
    :return: Costo de envio productos
    '''
    return kilometros * 0

def calcular_costo_envio_fuera(kilometros):
    '''
    (num) -> num
    Calcula el costo de envío por fuera

    >>> calcular_costo_envio(5)
    575.0

    >>> calcular_costo_envio(10)
    1150.0

    :param kilometros: Kilometros a recorrer
    :return: Costo de envio productos
    '''
    return kilometros * 115

def calcular_precio_producto_fuera(coste_producto,kilometros):
    '''
    (num, num) -> num

    Calcular el precio de producto enviados fuera de la ciudad

    >>> calcular_precio_producto_fuera(4)
    9

    :param coste_producto: Valor del producto
    :param kilometros: Kilometros recorridos fuera de la ciudad
    :return: Precio del prodcuto fuera de la ciudad
    '''

    return calcular_precio_producto(coste_producto) +  calcular_costo_envio_fuera(kilometros)

def calcular_iva_producto(coste_producto, tasa):
    '''
    (num,num) -> num

    Calcula el IVA del producto

    >>> calcular_iva_producto(15)
    pass
    
    :param coste_producto: Valor del producto
    :param tasa: IVA establecido del producto
    :return: IVA del producto
    '''

    return (calcular_precio_producto(coste_producto) * (tasa/100))

def calcular_iva_servicio(cantidad_horas, tasa):
    '''
    (num, num) -> num
    
    Calcula el iva del servicio
    
    >>> calcular_iva_servicio(3)
    5
    
    :param cantidad_horas: Horas laboradas
    :param tasa: IVA estipulada
    :return: IVA del servivio
    '''
    return calcular_precio_servicio(cantidad_horas)*(tasa/100)


def calcular_iva_envio(kilometros, tasa):
    '''
    (num, num) -> num
    
    Calcula el iva de envío
    
    >>> calcular_iva_envio(6)
    1
    
    :param kilometros: kilometros recorridos 
    :param tasa: IVA estipulado
    :return: IVA delñ envío
    '''
    
    return calcular_costo_envio(kilometros) * (tasa/100)


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

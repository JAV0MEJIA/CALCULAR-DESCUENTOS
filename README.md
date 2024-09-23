# CALCULAR-DESCUENTOS
CALCUALR DESCUENTOS
def calcular_descuento(monto_total, porcentaje_descuento=10):
    """
    Calcula el descuento aplicando el porcentaje al monto total de la compra.

    Args:
        monto_total (float): El monto total de la compra.
        porcentaje_descuento (float, opcional): El porcentaje de descuento. Por defecto es 10.

    Returns:
        float: El monto del descuento calculado.
    """
    # Validar que el monto total sea un número positivo
    if monto_total <= 0:
        raise ValueError("El monto total debe ser un número positivo")

    # Validar que el porcentaje de descuento sea un número entre 0 y 100
    if porcentaje_descuento < 0 or porcentaje_descuento > 100:
        raise ValueError("El porcentaje de descuento debe estar entre 0 y 100")

    # Calcular el descuento
    descuento = (monto_total / 100) * porcentaje_descuento

    return descuento

# Ejemplos de uso:
monto_total = 1200
porcentaje_descuento = 15

descuento1 = calcular_descuento(monto_total)
print(f"Descuento con porcentaje por defecto (10%): {descuento1}")

descuento2 = calcular_descuento(monto_total, porcentaje_descuento)
print(f"Descuento con porcentaje personalizado ({porcentaje_descuento}%): {descuento2}")


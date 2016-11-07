# calculadora-swift

Pequeño demo usando swift en linux

Prerequisitos:

- Tener instalador Swift (2.2 o 3) y exportado la variable

Compilación:

- Clonar el proyecto (git clone https://github.com/EParedez/calculadora-swift.git)
- Desde el path del proyecto clonado, ejecutar :
  * swiftc -emit-library Operacion.swift -module-name operacion
  * swiftc -emit-module -module-name operacion Operacion.swift
  * swiftc -I. -c Calculadora.swift
  * swiftc -o Calculadora.exe Calculadora.o -L. -loperacion
  * LD_LIBRARY_PATH=.:$LD_LIBRARY_PATH ./Calculadora.exe

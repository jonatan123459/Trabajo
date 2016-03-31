# Trabajo
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package simulador;

import javax.swing.JOptionPane;

/**
 *
 * @author WINDOWS 8.1
 */
public class Menu2 {

    public void MenuSec() {
        int opt2; 
        int convertidor2; r
        String tab1 = ""; 
        String tab2 = ""; 

        //Proceso de Definición de las Instancias: 
        Simulacion miSimulacion = new Simulacion();
        Producto miProducto = new Producto();
        Convertidor miConvertidor = new Convertidor();
        Menu2 men2 = new Menu2();

        do { //Ciclo de Accesos al Menú

            //Concatenación y Orden del Menú de Opciones:
            tab1 += "SELECCIONE UNA OPCIÓN:\n\n"
                    + "\n1) Modificar parametros...\n"
                    + "\n2) Ingresar o modificar caracteristicas de las maquinas...\n"
                    + "\n3) Ejecutar la simulacion...\n"
                    + "\n4) Ver resultados de la simulacion mas reciente...\n"
                    + "\n5) Salir del programa...\n";

            //Proceso del Switch que Permite la Escogencia del Menú
            do { //Ciclo de Acceso, para el cierre del Programa

                JOptionPane.showMessageDialog(null, tab1); //Despliegue del Menú Concatenado
                opt2 = Integer.parseInt(JOptionPane.showInputDialog("Digite Una Opción: ")); //Toma del Número de Opción Elegida

                if ((opt2 > 9) || (opt2 < 1)) { //Condiciones de Acceso al Menú
                    //Aviso de Error en Caso de No Cumplirse la Condición
                    JOptionPane.showMessageDialog(null, "Error de Dígito", "ERROR!", JOptionPane.ERROR_MESSAGE);
                    System.err.println("Error de Dígito");

                } else { //De Sí Cumplirse la Condición; se deberá proceder con el siguiente proceso:

                    switch (opt2) { //Lectura de la Opción Escogida para el Acceso al Menú

                        //Casos de Acción,según la Opción del Menú
                        case 1: 
                            Menu1 men1 = new Menu1();
                            men1.MenuPri();

                            break; //Fin del Caso 1

                        case 2: 

                            break; //Fin del Caso 2

                        case 3: 

                            break; //Fin del Caso 3

                        case 4: 
                            break; //Fin del Caso 4

                        case 5:
                            System.exit(0);
                            tab2 += "Las Horas a Trabajar Son:\n" + miConvertidor.getHoras() + "\n"
                                    + "Los Días a Trabajar Son:\n" + miConvertidor.converHoras() + "\n"
                                    + "Las Semanas a Trabajar Son:\n" + miConvertidor.converDias() + "\n"
                                    + "Los Meses a Trabajar Son:\n" + miConvertidor.converSemanas() + "\n"
                                    + "Los Años a Trabajar Son:\n" + miConvertidor.converMeses() + "\n";
                            JOptionPane.showMessageDialog(null, tab2); //Despliegue del Menú Concatenado

                            break; //Fin del Caso 5

                        default: //Acción por Defecto si se escoge otro Número NO Provisto en el Menú
                            //Despliegue de Mensajes de Errores:
                            JOptionPane.showMessageDialog(null, "Número Incorrecto", "ERROR!", JOptionPane.ERROR_MESSAGE);
                            System.err.println("Número Incorrecto");
                    } //Fin del Switch del Menú
                } //Fin del Else de la Condición de Entrada al Menú del If

            } while (opt2 != 6); //Fin del Ciclo de Clausura que Cierra el Menú

        } while (opt2 < 5); //Fin del Ciclo de Acceso al Menú
    }

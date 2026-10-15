
DJANGO Framework
DEBUG = True

`https://noc-apps.telconet.ec/ws/rest/procesar/tareas`
al estar la opcion  de DEBUG  puedes listar las rutas de la API

1. ws/rest/procesar/
2. ws/rest/procesar<drf_format_suffix:format>
3. ws/rest/procesar/tareas
4. ws/rest/procesar/tareas<drf_format_suffix:format>
5. ws/rest/procesar/token
6. ws/rest/procesar/token<drf_format_suffix:format>
7. ws/rest/procesar/<int:pk>/
8. ws/rest/procesar/<int:pk><drf_format_suffix:format>
9. ws/rest/procesar/casos
10. ws/rest/procesar/casos<drf_format_suffix:format>
11. ws/rest/procesar/CasoTarea
12. ws/rest/procesar/CasoTarea<drf_format_suffix:format>
13. ws/rest/procesar/umProactivo
14. ws/rest/procesar/umProactivo<drf_format_suffix:format>
15. ws/rest/procesar/lsProactivo
16. ws/rest/procesar/lsProactivo<drf_format_suffix:format>
17. ws/consultarai
18. ws/consultarai<drf_format_suffix:format>
19. ws_pruebas/rest/procesar/
20. ws_pruebas/rest/procesar<drf_format_suffix:format>
21. ws_pruebas/rest/procesar/tareas
22. ws_pruebas/rest/procesar/tareas<drf_format_suffix:format>
23. ws_pruebas/rest/procesar/<int:pk>/
24. ws_pruebas/rest/procesar/<int:pk><drf_format_suffix:format>
25. ws_pruebas/rest/procesar/casos
26. ws_pruebas/rest/procesar/casos<drf_format_suffix:format>
27. admin/
28. ws_telcograf/
29. ws_telcograf<drf_format_suffix:format>
30. ws_telcograf/<int:pk>/
31. ws_telcograf/<int:pk><drf_format_suffix:format>
32. ws_telcogra/getRuc/
33. ws_telcogra/getRuc<drf_format_suffix:format>
34. ws_telcogra/getRuc/<n>
35. ws_telcogra/getRuc/<n><drf_format_suffix:format>
36. ws_pruebas_telcograf/
37. ws_pruebas_telcograf<drf_format_suffix:format>
38. ws_pruebas_telcograf/<int:pk>/
39. ws_pruebas_telcograf/<int:pk><drf_format_suffix:format>
40. login/ [name='login']
41. register/ [name='register']
42. logout/ [name='logout']
43. ^.*\.html [name='pages']
44. [name='home']
45. pendientes-municipio/ [name='pendientes-municipio']
46. pendientes-municipio/agregar [name='pendientes-municipio-agregar']
47. pendientes-municipio/editar/<int:pk>/ [name='pendientes-municipio-editar']
48. pendientes-municipio/cerrar/<int:pk>/ [name='pendientes-municipio-cerrar']
49. pendientes-municipio/caso/<int:pk>/ [name='pendientes-municipio-caso-editar']
50. pendientes-municipio/detalle/<int:pk>/ [name='pendientes-municipio-detalle']
51. agregar-observacion/<int:pk> [name='agregar-observacion']
52. eliminar-observacion/<int:pk> [name='eliminar-observacion']
53. agregar-caso/<int:pk> [name='agregar-caso']
54. detalle/<int:pk> [name='detalle']
55. password/ [name='password']
56. tareas_programadas_r1/ [name='casos_handsontable']
57. tareas_programadas_r1/update/<int:pk> [name='casos_handsontable-update']
58. tareas_programadas_r1/crear [name='casos_handsontable-agregar']
59. tareas_programadas_r1/detalles/<int:pk> [name='casos_handsontable-detalles']
60. tareas_programadas_r1/finalizar/<int:pk> [name='casos_handsontable-finalizar']
61. tareas_programadas_r2/ [name='casos_handsontable_r2']
62. tareas_programadas_r2/update/<int:pk> [name='casos_handsontable-update_r2']
63. tareas_programadas_r2/crear [name='casos_handsontable-agregar_r2']
64. tareas_programadas_r2/detalles/<int:pk> [name='casos_handsontable-detalles_r2']
65. tareas_programadas_r2/finalizar/<int:pk> [name='casos_handsontable-finalizar_r2']
66. pendientes-municipio/reportes [name='reportes-municipio']
67. validaciones/ [name='validaciones']
68. validaciones/detalles/<int:pk> [name='validaciones-detalles']
69. validaciones/update/<int:pk> [name='validaciones-update']
70. validaciones/finalizar/<int:pk> [name='validaciones-finalizar']
71. validaciones/crear/ [name='validaciones-crear']
72. salidas_internacionales/ [name='casos_handsontable_salidasinternacionales']
73. salidas_internacionales/detalles/<int:pk> [name='casos_handsontable_salidasinternacionales-detalles']
74. salidas_internacionales/crear [name='casos_handsontable_salidasinternacionales-agregar']
75. calendar/ [name='calendar']
76. calendar/crear/ [name='calendar-crear']
77. calendar/detallesNOC/ [name='calendar-detalles-NOC']
78. calendar/detallesNOCMIMG/ [name='calendar-detalles-NOCMIMG']
79. calendar/update/<int:pk> [name='calendar-update']
80. calendar/borrar/<int:pk> [name='calendar-borrar']
81. calendar/gestionar/<int:pk> [name='calendar-gestionar']
82. calendar/rechazar/<int:pk> [name='calendar-rechazar']
83. calendar/ [name='calendar']
84. calendar/descarga_excel [name='descarga_excel']
85. calendar/excel [name='excel']
86. inventario/ [name='inventario']
87. inventario/tareas/<user_filter> [name='tareas']
88. inventario/equipos/<user_filter> [name='equipos']
89. inventario/editar_tareas/<tarea_filter> [name='editar_tareas']
90. inventario/editar_equipos/<equipo_filter> [name='editar_equipos']
91. inventario/crear_usuario [name='crear_usuario']
92. inventario/eliminar_usuarios/<user_filter> [name='eliminar_usuarios']
93. inventario/editar_usuario/<user_filter> [name='editar_usuario']
94. inventario/crear_zabbix/<user_filter> [name='crear_zabbix']
95. inventario/descarga_excel [name='descarga_excel']
96. inventario/descarga_excel [name='descarga_excel']
97. inventario/descarga_excel_tarea [name='descarga_excel_tarea']
98. reportes_clientes/ [name='presentacion_tabla_casos']
99. reportes_clientes/crear_caso/ [name='crear_caso_1']
100. reportes_clientes/actualizar_caso/<cas> [name='avances_caso']
101. reportes_clientes/finaliza_caso/<cas> [name='finaliza_caso']
102. reportes_clientes/reportes/ [name='reportes']
103. reportes_clientes/consolidado/ [name='consolidado']
104. calculador/sw [name='calcular']
105. calculador/ro [name='calcular1']
106. calculador/ro1 [name='calcular2']
107. KPI/enviar/ [name='Enviar_KPI']
108. KPI/Enviado/ [name='KPI_Enviado']
109. KPI/Ausuario/ [name='Ausuario']
110. KPI/enviar_global/ [name='Enviar_KPI_global']
111. KPI/Enviado_global/ [name='KPI_Enviado_global']
112. bitacoras/ [name='bitacoras']
113. reporte_consumo_l1/ [name='reporte_consumo_l1']
114. reporte_consumo_l1/consulta [name='consulta']
115. reporte_consumo_l1/generar_pdf [name='generar_pdf']
116. reporte_consumo/historico [name='reporte_historico']
117. reporte_consumo/consulta_historico [name='consulta_historico']
118. reporte_consumo/generarpdf_historico [name='generarpdf_historico']
119. reportesnoc/descarga [name='descarga_excel']
120. directorio/ingresard [name='ingresar_departamentos']
121. directorio/departamento [name='presentacion_departamentos']
122. directorio/cliente [name='presentacion_clientes']
123. directorio/departamento/<n> [name='presentacion_contacto']
124. directorio/ingresarc [name='ingresar_contacto']
125. directorio/actualizars/<n> [name='actualizar_standby']
126. directorio/actualizarc/<n> [name='actualizar_contacto']
127. directorio/jefes/<n> [name='presentacion_jefes']
128. directorio/eliminarc/<n> [name='eliminar_contacto']
129. directorio/get_contactos/<n> [name='get_contactos']
130. directorio/ingresar_contactos/ [name='create_multiple_contactos']
131. formulario_inspeccion/ [name='formulario_inspeccion_principal']
132. formulario_inspeccion/crear_nodo/ [name='crear_nodo']
133. formulario_inspeccion/crear_tecnico/ [name='crear_tecnico']
134. casos_dmq/ [name='casos_dmq']
135. cerrar_caso2/<str:caso>/ [name='cerrar_caso']
136. casos_mimg/ [name='casos_mimg']
137. cerrar_caso_mimg/<str:caso>/ [name='cerrar_caso_mimg']
138. casotelcos/crear [name='crear_caso']
139. casotelcos/principal [name='presentacion_tabla_casos']
140. casotelcos/avances/<cas> [name='avances_caso']
141. casotelcos/descarga [name='consolidado']
142. casotelcos/cerrar/<cas> [name='cerrar_caso']

```php
var widget = document.querySelector('.overlay-dialogue.modal.modal-popup');
var widgetHead = widget.querySelector('.dashbrd-widget-head');
var radioSegment1 = new RadioSegment("Clientes", ["Vip", "Apagan Equipos"]);
var radioSegment2 = new RadioSegment("Accion", ["Caso", "Tarea"]);
var texto1 = new Text("Caso", 1, "xxxxxxxx-xxxxx");
var texto2 = new Text("Tarea", 2, "xxxxxxxx");

var checkboxVipC1 = new CheckBox("Problema telconet");
var checkboxVipC2 = new CheckBox("Caso de backbone");
var checkboxVipC3 = new CheckBox("Principal");
var checkboxVipC4 = new CheckBox("Backup");
var checkboxVipC5 = new CheckBox("Principal Electrico");
var checkboxVipC6 = new CheckBox("Backup Electrico");
var checkboxVipC7 = new CheckBox("IPV6");

var checkboxVipT1 = new CheckBox("Cliente no contesta");
var checkboxVipT2 = new CheckBox("Nodo en baterias");
var checkboxVipT3 = new CheckBox("Estado in-corte");
var checkboxVipT4 = new CheckBox("Tarea programada");
var checkboxVipT5 = new CheckBox("Cliente contesta");
var checkboxVipT6 = new CheckBox("IPV6");
var checkboxVipT7 = new CheckBox("Interfaz caida");
var checkboxVipT8 = new CheckBox("Caida VPN");

// var checkboxBancoC1 = new CheckBox("Eléctrico Principal");
// var checkboxBancoC2 = new CheckBox("Eléctrico Backup");
// var checkboxBancoC3 = new CheckBox("Principal");
// var checkboxBancoC4 = new CheckBox("Backup");
// var checkboxBancoC5 = new CheckBox("Eléctrico Bolivariano");

var dropDown1 = new DropDown("notificacion", "Notificación", ["Si", "No"]);
var dropDown2 = new DropDown("notificacion_telegram", "Notificación Telegram", ["Si", "No"]);

var allCheckBox = checkboxVipC1.html() + checkboxVipC2.html() + checkboxVipC3.html() + checkboxVipC4.html()  + checkboxVipT1.html() + checkboxVipT2.html() + checkboxVipT3.html() + checkboxVipT4.html() + checkboxVipT5.html() + checkboxVipT6.html() + checkboxVipC5.html() + checkboxVipC6.html()  + checkboxVipC7.html()+ checkboxVipT7.html() + checkboxVipT8.html();

var container_html = '<div class="filter-container" id="filter-space"><div class="table filter-forms"><div class="row"><div class="cell" style="padding-right: 520px;padding-top: 5px;"><button id="telconet" type="button" class="btn-apply">Crear Caso</button></div><div class="cell" style="padding-top: 5px;"><button id="aplicar" type="button" class="btn-apply">Apply</button>  <button type="button" class="btn-alt">Reset</button></div></div></div></div>';
var table_html = '<div class="table filter-forms"> <div class="row"> <div class="cell"></div><div class="cell"></div></div></div>'
var celda_html = '<ul class="table-forms" style="width: 350px;"></ul>';

var overlay_html = '<div id="overlay_bg" class="overlay-bg" data-dialogueid="afg124"></div>'
var loader_html = '<div id="overlay_dialogue" class="overlay-dialogue modal modal-popup modal-popup-generic" data-dialogueid="afg124" role="dialog" aria-modal="true" aria-labeledby="dashbrd-widget-head-title-i1qwwp" style="position: fixed;left: 50%; top:50%;margin-right: -50%; transform: translate(-50%, -50%);"><button id="cerrar_icon" class="overlay-close-btn" title="Close"></button><div class="dashbrd-widget-head"></div><div class="overlay-dialogue-body" style="overflow-y: hidden;"><div id="carga" class="is-loading" style="height: 68px;"></div></div><div class="overlay-dialogue-footer"></div></div>'

if (widgetHead.textContent == "Update problem") {
    /* Construcción del boton filter */
    widget.querySelector('.overlay-dialogue-body').insertAdjacentHTML('afterbegin', container_html);
    //widgetHead.insertAdjacentHTML('afterend', container_html);

    /* Construcción del container */
    var container = document.querySelector("#filter-space");
    container.insertAdjacentHTML('afterbegin', table_html);

    /* Construcción de las celdas en html */
    var celdas = document.querySelectorAll("#filter-space .table.filter-forms .row .cell");
    celdas[0].insertAdjacentHTML('afterbegin', celda_html);
    celdas[1].insertAdjacentHTML('afterbegin', celda_html);

    var columnas = document.querySelectorAll("#filter-space .table-forms");
    columnas[0].insertAdjacentHTML('afterbegin', radioSegment1.html() + texto1.html() + texto2.html() + dropDown1.html() + dropDown2.html());
    columnas[1].insertAdjacentHTML('afterbegin', radioSegment2.html() + allCheckBox);

    /* Definicion de los event listeners */

    var radioClientes = document.querySelectorAll("#Clientes.radio-list-control li");
    var radioAccion = document.querySelectorAll("#Accion.radio-list-control li");
    var items = document.querySelectorAll("#filter-space .filter-forms .table-forms li");
    /* console.log(items); */

    radioClientes[0].addEventListener("click", vip);
    // radioClientes[1].addEventListener("click", bancos);
    radioClientes[1].addEventListener("click", apagan);

    radioAccion[0].addEventListener("click", caso);
    radioAccion[1].addEventListener("click", tarea);

    document.querySelector("#aplicar").addEventListener("click", function () {
        var checkbox = document.querySelectorAll("#filter-space .checkbox-radio");
        var mensaje = "";
        var caso_msg = document.querySelector("#txt_select1").value;
        var tarea_msg = document.querySelector("#txt_select2").value;


        for (i = 0; i < checkbox.length; i++) {

            if (checkbox[i].checked == true) {
                switch (checkbox[i].name) {
                    /* CASOS VIP*/
                    case "Problema telconet":
                        mensaje = 'el caso: ' + caso_msg + ' para realizar el soporte.';
                        break;
                    case "Caso de backbone":
                        mensaje = 'el caso: ' + caso_msg + '. Al momento se tiene un problema masivo que afecta el enlace mencionado.';
                        break;
                    case "Principal":
                        if(document.querySelector("#Accion_0").checked == true){
                            mensaje = 'el caso: ' + caso_msg + ', para realizar el soporte del enlace principal.';
                        } else if (document.querySelector("#Accion_1").checked == true){
                            mensaje = 'la tarea: ' + tarea_msg + ', para realizar el soporte del enlace principal.';
                        }
                        break;
                    case "Backup":
                        if(document.querySelector("#Accion_0").checked == true){
                            mensaje = 'el caso: ' + caso_msg + ', para realizar el soporte del enlace backup.';
                        } else if (document.querySelector("#Accion_1").checked == true){
                            mensaje = 'la tarea: ' + tarea_msg + ', para realizar el soporte del enlace backup.';
                        }
                        break;
                    case "Principal Electrico":
                        mensaje = 'el caso: ' + caso_msg + ', para realizar el soporte del enlace principal.<br><br>Por  favor confirmar si tiene algún problema eléctrico o apagaron sus equipos  de no ser así favor indicar un número de contacto para comunicarnos.';
                        break;
                    case "Backup Electrico":
                        mensaje = 'el caso: ' + caso_msg + ', para realizar el soporte del enlace backup.<br><br>Por  favor confirmar si tiene algún problema eléctrico o apagaron sus equipos  de no ser así favor indicar un número de contacto para comunicarnos.';
                        break;
                    case "IPV6":
                        if(document.querySelector("#Accion_0").checked == true){
                            mensaje = 'el caso: ' + caso_msg + ', para realizar el soporte del enlace IPV6.';
                        } else if (document.querySelector("#Accion_1").checked == true){
                            mensaje = 'la tarea: ' + tarea_msg + ', para realizar el soporte del enlace IPV6.';
                        }
                        break;
                    /* TAREAS VIP */
                    case "Cliente no contesta":
                        mensaje = 'la tarea: ' + tarea_msg + ' para realizar el soporte.<br><br>Por  favor confirmar si tiene algún problema eléctrico o apagaron sus equipos  de no ser así favor indicar un número de contacto para comunicarnos.';
                        break;
                    case "Nodo en baterias":
                        mensaje = 'la tarea: ' + tarea_msg + '.<br><br>Se verifica con la empresa eléctrica que al momento no se tiene energía en el sector.';
                        break;
                    case "Estado in-corte":
                        mensaje = 'la tarea: ' + tarea_msg + '.<br><br>Se verifica que el servicio se encuentra suspendido.';
                        break;
                    case "Tarea programada":
                        mensaje = 'la tarea: ' + tarea_msg + '.<br><br> Al momento el enlace se encuentra afectado por  una ventana de mantenimiento.';
                        break;
                    case "Cliente contesta":
                        mensaje = 'la tarea: ' + tarea_msg + ' para realizar el soporte.<br><br>Se confirma con el Sr. Smith Smith cel: 09xxxxxxx que /se están realizando trabajos /se tiene problema eléctrico /se han apagado los equipos/ etc .';
                        break;
                    case "Interfaz caida":
                        mensaje = 'el caso: ' + tarea_msg + ' para realizar el soporte de la interfaz caída.';
                        break;
                    case "Caida VPN":
                            mensaje = 'la tarea: ' + tarea_msg + ' para realizar el soporte de la interfaz VPN caída.';
                            break;
                    /* CASOS BANCOS */
                    case "Eléctrico Principal":
                        mensaje = 'el caso:<br><br>Caso Principal: ' + caso_msg + ', para realizar el soporte Su ayuda confirmando si tiene algún problema eléctrico o apagaron sus equipos, de no ser así favor indicar un número de contacto para comunicarnos';
                        break;
                    case "Eléctrico Backup":
                        mensaje = 'el caso:<br><br>Caso Backup: ' + caso_msg + ', para realizar el soporte Su ayuda confirmando si tiene algún problema eléctrico o apagaron sus equipos, de no ser así favor indicar un número de contacto para comunicarnos';
                        break;
                    case "Principal":
                        mensaje = 'el caso:<br><br>Caso Principal: ' + caso_msg + ', para realizar el soporte del enlace.';
                        break;
                    case "Backup":
                        mensaje = 'el caso:<br><br>Caso Backup: ' + caso_msg + ', para realizar el soporte del enlace.';
                        break;
                    case "Eléctrico Bolivariano":
                            mensaje = 'el caso: ' + caso_msg + ' para realizar el soporte.<br><br>Por  favor confirmar si tiene algún problema eléctrico o apagaron sus equipos  de no ser así favor indicar un número de contacto para comunicarnos.';
                        break;
                    default:
                        break;
                }
            } else if (document.querySelector("#Clientes_1").checked == true) {
                mensaje = 'la tarea: ' + tarea_msg + '.<br><br>Se verifica en el historial de monitoreo que los equipos son apagados a esta hora.';
            }
        }
        if (document.querySelector("#notificacion").value == 1) {
            //document.querySelector("#message").textContent = mensaje;
			document.querySelector("#message").value=mensaje;
        } else {
            //document.querySelector("#message").textContent = '---'+mensaje;
			document.querySelector("#message").value= '---'+mensaje;
            document.querySelector("#notificacion_telegram").value=0
            mensaje='---'+mensaje;
        }
        if (document.querySelector("#notificacion_telegram").value == 1) {
            //document.querySelector("#message").textContent = mensaje;
			document.querySelector("#message").value=mensaje;
        } else {
            //document.querySelector("#message").textContent = '---'+mensaje;
            if(mensaje.includes("---")){
                document.querySelector("#message").value=mensaje
            } else {
			    document.querySelector("#message").value= mensaje+'**';
            }
        }
    });

    document.querySelector("#filter-space .filter-forms .btn-alt").addEventListener("click", function () {
        location.reload();
    });
	
	var selecciones = document.querySelectorAll("#filter-space .checkbox-radio");
	for (i = 0; i < selecciones.length; i++) {
		selecciones[i].addEventListener("change", noSeleccionar);
    }
    
    document.querySelector("#telconet").addEventListener("click", function () {
        /* Construcción del overlay */
        document.querySelector("body").style.overflow = "hidden";

        widget.insertAdjacentHTML('afterend', overlay_html);
        var overlay = document.querySelector("#overlay_bg")
        overlay.insertAdjacentHTML('afterend', loader_html);

        function CargarTexto(texto){
            var h_text = document.querySelector('#telconet').innerHTML
            var carga = document.querySelector("#carga")
            carga.remove();
            var widget_head = document.querySelector("#overlay_dialogue .dashbrd-widget-head");
            var widget_body = document.querySelector("#overlay_dialogue .overlay-dialogue-body");
            var widget_footer = document.querySelector("#overlay_dialogue .overlay-dialogue-footer");

            widget_head.insertAdjacentHTML('beforeend', '<h4>'+h_text+'</h4>');
            if(texto["error"]){
                widget_body.insertAdjacentHTML('beforeend', '<div id="tabs" class="table-forms-container"><div id="scriptTab"><pre><ul><li><b>ERROR: </b></li><li>'+texto["error"]+'</li></ul></pre></div></div>');
            } else if (h_text == "Crear Caso") {
                document.querySelector("#txt_select1").value = texto["result"]["numeroCaso"]
                widget_body.insertAdjacentHTML('beforeend', '<div id="tabs" class="table-forms-container"><div id="scriptTab"><pre><ul><li><b>CASO: </b>'+texto["result"]["numeroCaso"]+'</li><li><b>TAREA: </b>'+texto["result"]["tareas"][0]["numeroTarea"]+'</li><br><li>'+texto["observacion"]+'</li></ul></pre></div></div>');
            } else if (h_text == "Crear Tarea") {
                document.querySelector("#txt_select2").value = texto["resultado"]
                widget_body.insertAdjacentHTML('beforeend', '<div id="tabs" class="table-forms-container"><div id="scriptTab"><pre><ul><li><b>TAREA: </b>'+texto["resultado"]+'</li><br><li>'+texto["observacion"]+'</li></ul></pre></div></div>');
            }
            widget_footer.insertAdjacentHTML('beforeend','<button id="cerrar_btn" type="button" class="btn-alt">Cancel</button>');
            document.querySelector("#cerrar_icon").addEventListener("click", function () {
                document.querySelector("body").style.overflow = "visible";
                document.querySelector("#overlay_dialogue").remove();
                document.querySelector("#overlay_bg").remove();
            });
            document.querySelector("#cerrar_btn").addEventListener("click", function () {
                document.querySelector("body").style.overflow = "visible";
                document.querySelector("#overlay_dialogue").remove();
                document.querySelector("#overlay_bg").remove();
            });   
        }

        var seleccion = document.querySelectorAll("#filter-space .checkbox-radio");
        var radioClientes = document.querySelectorAll("#Clientes.radio-list-control li input");
        var radioAccion = document.querySelectorAll("#Accion.radio-list-control li input");
        var usuario = (document.querySelector(".icon-profile").title).split(" ", 1)[0];
        var eventid = document.querySelector('#eventids_0').value
        var ip = location.host;

        for (i = 0; i < seleccion.length; i++) {
            if (seleccion[i].checked == true) {
                var opcion = seleccion[i].id
            }
        };
        for (i = 0; i < radioClientes.length; i++) {
            if (radioClientes[i].checked == true) {
                var cliente = radioClientes[i].value
            }
        };
        for (i = 0; i < radioAccion.length; i++) {
            if (radioAccion[i].checked == true) {
                var accion = radioAccion[i].value
            }
        };

        var request = new XMLHttpRequest();
        var resultado = {
            "eventid": eventid,
            "opcion": opcion,
            "cliente": cliente,
            "accion": accion,
            "usuario": usuario,
            "ip": ip
        };

        request.open('POST', 'https://noc-apps.telconet.ec/ws/rest/procesar/casos', true);
        request.setRequestHeader('Content-Type', 'application/json;charset=UTF-8');
        request.onload = function() {
            if (this.status >= 200 && this.status < 400) {
              // Success!
              var resp = JSON.parse(this.response);
              CargarTexto(resp)
            } else {
                var respuesta = {};
                respuesta["error"]="Se ha alcanzado al servidor, pero ha ocurrido un error";
                CargarTexto(respuesta);
            }
          };
        request.onerror = function() {
            var respuesta = {};
            respuesta["error"]="Ocurrio un error de conexión";
            CargarTexto(respuesta);
          };
        if(opcion === undefined && cliente!="2"){
            var respuesta = {};
            respuesta["error"]="No se ha seleccionado ninguna opción.";
            CargarTexto(respuesta);
        } else if(opcion == "Caso de backbone") {
            var respuesta = {};
            respuesta["error"]="Solo se pueden crear casos del tipo técnico.";
            CargarTexto(respuesta);
        } else {
            request.send(JSON.stringify(resultado));
        }
    });


    vip();
}




/* Definicion de los javascript constructors para definir los elementos de las celdas */
function RadioSegment(nombre, lista) {
    this.nombre = nombre;
    this.lista = lista;
    var inicio = '<li><div class="table-forms-td-left"><label>' + this.nombre + '</label></div><div class="table-forms-td-right"><ul id="' + this.nombre + '" class="radio-list-control">';
    var fin = '</ul></div></li>';
    var contenido = '';
    this.html = function () {
        for (i = 0; i < lista.length; i++) {
            if (i == 0) {
                contenido += '<li><input type="radio" id="' + this.nombre + '_' + i + '" name="' + this.nombre + '" value="' + (i + 1) + '" checked="checked"><label for="' + this.nombre + '_' + i + '">' + lista[i] + '</label></li>';
            } else {
                contenido += '<li><input type="radio" id="' + this.nombre + '_' + i + '" name="' + this.nombre + '" value="' + (i + 1) + '"><label for="' + this.nombre + '_' + i + '">' + lista[i] + '</label></li>';
            }
        }

        return inicio + contenido + fin;
    };
}

function Text(nombre, id, contenido) {
    this.nombre = nombre;
    this.id = id;
    this.contenido = contenido;
    var inicio = '<li><div class="table-forms-td-left"><label for="txt_select">';
    var fin = '</label></div><div class="table-forms-td-right"><input type="text" id="txt_select' + this.id + '" name="txt_select" value="' + this.contenido + '" maxlength="255" style="width: 150px;"></div></li>';
    this.html = function () {
        return inicio + this.nombre + fin;
    }
}

function CheckBox(nombre) {
    this.nombre = nombre;
    var inicio = '<li><div class="table-forms-td-left"><label for="' + this.nombre + '">';
    var fin = '</label></div><div class="table-forms-td-right"><input type="radio" id="' + this.nombre + '" name="' + this.nombre + '" value="1" class="checkbox-radio"><label for="show_details"><span></span></label></div></li>';
    this.html = function () {
        return inicio + this.nombre + fin;
    }
}

function DropDown(id, nombre, lista) {
    this.id = id;
    this.nombre = nombre;
    this.lista = lista;
    var inicio = '<li><div class="table-forms-td-left"><label for="' + id + '">' + nombre + '</label></div><div class="table-forms-td-right"><select id="' + id + '" name="' + id + '" autocomplete="off">';
    var fin = '</select></div></li>';
    var contenido = '';
    this.html = function () {
        for (i = 0; i < lista.length; i++) {
            if (i == 0) {
                contenido += '<option value="' + (i + 1) + '" selected="selected">' + lista[i] + '</option>';
            } else {
                contenido += '<option value="' + (i + 1) + '">' + lista[i] + '</option>';
            }
        }
        return inicio + contenido + fin;
    };
}

function vip() {
    for (i = 0; i < items.length; i++) {
        items[i].style.display = "none";
    }
    console.log(items);
    items[0].style.display = "";
    items[6].style.display = "";
    items[5].style.display = "";

    items[1].style.display = "";
    //items[2].style.display = "";
    items[2].style.display = "";

    items[7].style.display = "";
    items[8].style.display = "";
    items[9].style.display = "";
    items[9].style.display = "";

    if (document.querySelector("#Accion_0").checked == true) {
        items[3].style.display = "";
        items[9].style.display = "";
        items[10].style.display = "";
        items[11].style.display = "";
        items[12].style.display = "";
        items[13].style.display = "";
        items[19].style.display = "";
        items[20].style.display = "";
        items[21].style.display = "";
        items[23].style.display = "";
        
        
    } else {
        items[4].style.display = "";
        items[11].style.display = "";
        items[12].style.display = "";
        items[12].style.display = "";
        items[14].style.display = "";
        items[15].style.display = "";
        items[16].style.display = "";
        //items[17].style.display = "";
        items[18].style.display = "";        
        items[19].style.display = "";
       
      
    }
}

// function bancos() {
//     for (i = 0; i < items.length; i++) {
//         items[i].style.display = "none";
//     }
//     items[0].style.display = "";
//     items[6].style.display = "";
//     items[7].style.display = "";

//     items[1].style.display = "";
//     items[2].style.display = "";
//     items[3].style.display = "";

//     items[8].style.display = "";
//     items[9].style.display = "";
//     items[10].style.display = "";

//     if (document.querySelector("#Accion_0").checked == true) {
//         items[4].style.display = "";
//         items[19].style.display = "";
//         items[20].style.display = "";
//         items[21].style.display = "";
//         items[22].style.display = "";
//         items[23].style.display = "";
//         items[24].style.display = "";
//     } else {
//         items[5].style.display = "";
//         items[16].style.display = "";
//         items[17].style.display = "";
//         items[25].style.display = "";
//     }
// }

function apagan() {
    document.querySelector('#telconet').innerHTML = 'Crear Tarea';

    var seleccion = document.querySelectorAll("#filter-space .checkbox-radio");
    for (i = 0; i < seleccion.length; i++) {
        seleccion[i].checked = false
    }

    for (i = 0; i < items.length; i++) {
        items[i].style.display = "none";
    }
    items[0].style.display = "";
    items[4].style.display = "";
    items[5].style.display = "";

    items[1].style.display = "";
    //items[2].style.display = "";
    items[2].style.display = "";
    document.querySelector("#notificacion").selectedIndex = "1";
    document.querySelector("#notificacion_telegram").selectedIndex = "1";
}

function caso() {
    document.querySelector('#telconet').innerHTML = 'Crear Caso';

    var seleccion = document.querySelectorAll("#filter-space .checkbox-radio");
    for (i = 0; i < seleccion.length; i++) {
        seleccion[i].checked = false
    }

    for (i = 0; i < items.length; i++) {
        items[i].style.display = "none";
    }
    items[0].style.display = "";
    items[6].style.display = "";
    items[5].style.display = "";

    items[1].style.display = "";
    //items[2].style.display = "";
    items[2].style.display = "";

    items[7].style.display = "";
    items[8].style.display = "";
    items[9].style.display = "";
    items[9].style.display = "";

    if (document.querySelector("#Clientes_0").checked == true) {
        items[3].style.display = "";
        items[9].style.display = "";
        items[10].style.display = "";
        items[11].style.display = "";
        items[12].style.display = "";
        items[13].style.display = "";
        items[19].style.display = "";
        items[20].style.display = "";
        items[21].style.display = "";
        items[23].style.display = "";
        
    }
    /*if (document.querySelector("#Clientes_1").checked == true) {
        items[5].style.display = "";
        items[18].style.display = "";
        items[19].style.display = "";
        items[20].style.display = "";
        items[21].style.display = "";
        items[22].style.display = "";
        items[24].style.display = "";
    }*/
}

function tarea() {
    document.querySelector('#telconet').innerHTML = 'Crear Tarea';

    var seleccion = document.querySelectorAll("#filter-space .checkbox-radio");
    for (i = 0; i < seleccion.length; i++) {
        seleccion[i].checked = false
    }

    for (i = 0; i < items.length; i++) {
        items[i].style.display = "none";
    }
    items[0].style.display = "";
    items[6].style.display = "";
    items[5].style.display = "";

    items[1].style.display = "";
    //items[2].style.display = "";
    items[2].style.display = "";

    items[7].style.display = "";
    items[8].style.display = "";
    items[9].style.display = "";

    if (document.querySelector("#Clientes_0").checked == true) {
        items[4].style.display = "";
        items[12].style.display = "";
        items[13].style.display = "";
        items[14].style.display = "";
        items[15].style.display = "";
        items[16].style.display = "";
        items[17].style.display = "";
        //items[17].style.display = "";
        items[18].style.display = "";
        items[19].style.display = "";
        items[24].style.display = "";
  
    }
    /*if (document.querySelector("#Clientes_1").checked == true) {
        items[4].style.display = "";
        items[15].style.display = "";
        items[16].style.display = "";
        items[23].style.display = "";
    }*/

}

function noSeleccionar () {
	if(this.checked) {
		for (i = 0; i < selecciones.length; i++) {
			selecciones[i].checked = false;
		}
		this.checked = true;
    } else {
        // Checkbox is not checked..
    }
}

$.getScript("./link_status.js");
```


### Error autenticacion telcos
![[Pasted image 20250913093555.png]]



### Error al crear caso tecnico 
![[Pasted image 20260119092744.png]]
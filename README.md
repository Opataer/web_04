<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anuario COBAEH - 6203</title>
    <link rel="stylesheet" href="main.css"

</head>
<body>

    <!-- Video al inicio de la página -->
    <iframe src="https://drive.google.com/file/d/1apsJ1FkshLKYwnM_QaIZyhwf3Srm5B1S/preview" width="640" height="360" allow="autoplay" allowfullscreen></iframe>

    <h1>🎓 Generación 2022 - 2025</h1>

    <img src="https://i.postimg.cc/wBhBdr3h/Screenshot-20250324-144246.png" alt="Nuevo Logo" width="200">

    <div class="big-message">Éxito en tu siguiente paso. ¡Acabas de concluir un paso de muchos! 🎉</div>

    <img src="https://i.postimg.cc/MT2j7RfY/IMG-20250324-WA0019.jpg" alt="Foto de generación">

    <button class="button" id="openGroupBtn" onclick="openStudentList()">📖 Grupo 6203</button>

    <script>
        // Información de los estudiantes
        const students = [
            { name: "Leilani Guadalupe Aranda Gomez", age: 19, motivation: "¡Tu esfuerzo será siempre tu mejor aliado, sigue brillando!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/dtkkx4R9/IMG-20250324-WA0027.jpg" },
            { name: "James Naomi Campos Damas", age: 17, motivation: "Cada paso que tomas te acerca más a tu mejor versión. ¡Sigue adelante!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/6QTDr4xT/IMG-20250324-WA0003.jpg" },
            { name: "Valeria Abigail Ensastiga Ramirez", age: 17, motivation: "Lo más importante es nunca dejar de creer en ti misma. ¡El futuro es tuyo!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/4N9y5nZL/IMG-20250324-WA0022.jpg" },
            { name: "Hugo Emilio Gomez Sanchez", age: 18, motivation: "El esfuerzo tiene recompensa, sigue así. ¡Lo mejor está por venir!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/sD7fW89b/IMG-20250324-WA0013.jpg" },
            { name: "Josmar Hernandez Gutierres", age: 17, motivation: "Tienes una gran capacidad para hacer lo que te propongas. ¡No te detengas!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/s2D3t2dR/IMG-20250324-WA0014.jpg" },
            { name: "Tania Hernandez Hernandez", age: 17, motivation: "Con esfuerzo y dedicación lograrás alcanzar todos tus objetivos.", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/y8hq6CXY/IMG-20250324-WA0016.jpg" },
            { name: "Jorge Eduardo Hernandez Sanchez", age: 20, motivation: "El camino nunca es fácil, pero siempre vale la pena. ¡Sigue adelante!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/d0JbLN4R/IMG-20250324-WA0008.jpg" },
            { name: "Maria Teresa Hernandez Soto", age: 19, motivation: "El trabajo duro siempre tiene su recompensa. ¡Sigue así!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/Y24Crj4r/IMG-20250324-WA0012.jpg" },
            { name: "Rigoberto Martinez Ramos", age: 17, motivation: "El esfuerzo tiene su recompensa, sigue así. ¡Estamos orgullosos de ti!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/gjL5fC2p/IMG-20250324-WA0011.jpg" },
            { name: "Carlos Jair Mendoza Sandoval", age: 19, motivation: "Cada logro es solo el inicio de otro, sigue alcanzando nuevas metas.", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/HLxC6PXY/IMG-20250324-WA0006.jpg" },
            { name: "Saul Mendoza Vazquez", age: 19, motivation: "La disciplina te llevará a alcanzar todos tus sueños. ¡Sigue adelante!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/nVw926mz/IMG-20250324-WA0028.jpg" },
            { name: "Karla Guadalupe Miron Galindo", age: 17, motivation: "No importa cuán difícil sea el camino, tu persistencia te llevará lejos.", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/bwfJF8wz/IMG-20250324-WA0021.jpg" },
            { name: "Abel Morales Vazquez", age: 17, motivation: "Tu dedicación y trabajo duro te harán destacar en cada paso que des.", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/BQMYmZgF/IMG-20250324-WA0010.jpg" },
            { name: "Marcos Patiño Sanchez", age: 17, motivation: "El esfuerzo constante siempre trae resultados positivos. ¡Sigue con todo!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/9FdV09ch/IMG-20250324-WA0015.jpg" },
            { name: "Marely Perez Alcaoter", age: 18, motivation: "Nada es imposible para alguien tan talentoso como tú. ¡Sigue brillando!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/W3YxWKh1/IMG-20250324-WA0024.jpg" },
            { name: "Nancy Perez Alcaoter", age: 19, motivation: "Lo que siembras hoy, será la cosecha de mañana. ¡Sigue adelante!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/xgZ5hJvN/IMG-20250324-WA0025.jpg" },
            { name: "Frida Sofia Pineda Ortiz", age: 18, motivation: "La perseverancia te llevará a cumplir tus sueños. ¡No dejes de luchar!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/pXJbRtBV/IMG-20250324-WA0004.jpg" },
            { name: "Fabian Ramirez Vergara", age: 17, motivation: "Nunca subestimes el poder de tu esfuerzo. ¡Sigue esforzándote!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/YCQ4p0sG/IMG-20250324-WA0026.jpg" },
            { name: "Jesus Santos Santiago Rodriguez", age: 18, motivation: "El esfuerzo tiene siempre su recompensa. ¡No te detengas!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/QtKZ39fv/IMG-20250324-WA0007.jpg" },
            { name: "Aline Amapola Vazquez Hernandez", age: 19, motivation: "Sigue creyendo en ti, porque lo mejor está por venir.", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/3r6Wm2M0/IMG-20250324-WA0023.jpg" },
            { name: "Camila Monserrat Vazquez Ramirez", age: 17, motivation: "¡No hay límites para lo que puedes alcanzar! ¡Sigue luchando por tus sueños!", details: "Buen estudiante de COBAEH", image: "https://i.postimg.cc/yxFqJq4P/IMG-20250324-WA0005.jpg" }
        ];

        // Función para abrir la ventana con la lista de estudiantes
        function openStudentList() {
            const newWindow = window.open("", "_blank", "width=800,height=600");

            newWindow.document.body.style.background = "linear-gradient(135deg, #800020, #a52a2a)";
            newWindow.document.body.style.color = "#fff";
            newWindow.document.body.style.fontFamily = "'Arial', sans-serif";
            newWindow.document.body.style.padding = "20px";

            newWindow.document.write("<h1>Selecciona un Estudiante</h1>");

            const selectElement = newWindow.document.createElement('select');
            selectElement.id = 'studentSelect';
            selectElement.style.padding = "10px";
            selectElement.style.fontSize = "18px";
            selectElement.style.borderRadius = "10px";
            selectElement.style.border = "2px solid #800020";
            selectElement.style.backgroundColor = "#fff";
            selectElement.style.color = "#800020";

            const defaultOption = newWindow.document.createElement('option');
            defaultOption.textContent = "Selecciona un estudiante";
            defaultOption.disabled = true;
            defaultOption.selected = true;
            selectElement.appendChild(defaultOption);

            students.forEach((student, index) => {
                const option = newWindow.document.createElement('option');
                option.value = index;
                option.textContent = student.name;
                selectElement.appendChild(option);
            });

            newWindow.document.body.appendChild(selectElement);

            selectElement.addEventListener('change', function() {
                const selectedStudent = students[selectElement.value];
                displayStudentInfo(newWindow, selectedStudent);
            });
        }

        // Función para mostrar la información del estudiante seleccionado
        function displayStudentInfo(newWindow, student) {
            const studentInfoDiv = newWindow.document.createElement('div');
            studentInfoDiv.classList.add('student-info');

            studentInfoDiv.innerHTML = `
                <h2>${student.name}</h2>
                <img src="${student.image}" alt="${student.name}">
                <p>Edad: ${student.age}</p>
                <p>Frase motivadora: "${student.motivation}"</p>
                <p>${student.details}</p>
            `;

            newWindow.document.body.appendChild(studentInfoDiv);
        }
    </script>

</body>
</html>

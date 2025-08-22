# hsm
Historia Social de la Medicina
<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sapiens Medicus: Un Viaje por la Historia de la Medicina</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -30px;
            top: 50%;
            transform: translateY(-50%);
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: #4f46e5;
            border: 4px solid #e0e7ff;
        }
        .timeline {
            border-left: 4px solid #e0e7ff;
        }
        .modal-content {
            animation: slide-up 0.3s ease-out;
        }
        @keyframes slide-up {
            from {
                transform: translateY(50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
    </style>
</head>

<body class="bg-gray-50 text-gray-800">

    <!-- Header -->
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-2xl font-bold text-indigo-600">Sapiens Medicus</h1>
            <nav>
                <a href="#timeline" class="text-gray-600 hover:text-indigo-600 px-3 py-2 rounded-md text-sm font-medium">Línea de Tiempo</a>
                <a href="#about" class="text-gray-600 hover:text-indigo-600 px-3 py-2 rounded-md text-sm font-medium">Acerca de</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <main class="container mx-auto px-6 py-12">
        <section class="text-center">
            <h2 class="text-4xl md:text-5xl font-extrabold text-gray-900 mb-4">Un Viaje por la Historia Social de la Medicina</h2>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">Explora la evolución de los conceptos de <span class="font-semibold text-indigo-500">salud, enfermedad, vida y muerte</span> a través de los hitos que definieron la medicina moderna.</p>
        </section>

        <!-- Timeline Section -->
        <section id="timeline" class="mt-16">
            <h3 class="text-3xl font-bold text-center mb-12">Línea de Tiempo Interactiva</h3>
            <div class="relative pl-8 timeline">
                <!-- Timeline Item: Medicina Antigua -->
                <div class="mb-12 relative timeline-item">
                    <h4 class="text-2xl font-semibold text-indigo-700">Medicina Antigua</h4>
                    <p class="text-sm text-gray-500 mb-2">~3000 a.C. - 500 d.C.</p>
                    <p class="text-gray-600 mb-4">Desde las concepciones mágico-religiosas en Egipto hasta el nacimiento de la medicina racional con Hipócrates en Grecia.</p>
                    <button onclick="openModal('antigua')" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition duration-300">Explorar Época</button>
                </div>

                <!-- Timeline Item: Edad Media y Renacimiento -->
                <div class="mb-12 relative timeline-item">
                    <h4 class="text-2xl font-semibold text-indigo-700">Edad Media y Renacimiento</h4>
                    <p class="text-sm text-gray-500 mb-2">~500 - 1600 d.C.</p>
                    <p class="text-gray-600 mb-4">Influencia de la medicina árabe, el impacto de las pandemias y el resurgir de la anatomía con Vesalio.</p>
                    <button onclick="openModal('media')" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition duration-300">Explorar Época</button>
                </div>

                <!-- Timeline Item: Revolución Científica -->
                <div class="mb-12 relative timeline-item">
                    <h4 class="text-2xl font-semibold text-indigo-700">Revolución Científica</h4>
                    <p class="text-sm text-gray-500 mb-2">Siglos XVII - XVIII</p>
                    <p class="text-gray-600 mb-4">El método científico aplicado a la medicina. Descubrimientos clave como la circulación sanguínea de Harvey.</p>
                    <button onclick="openModal('cientifica')" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition duration-300">Explorar Época</button>
                </div>

                <!-- Timeline Item: Siglo XIX -->
                <div class="mb-12 relative timeline-item">
                    <h4 class="text-2xl font-semibold text-indigo-700">Siglo XIX: La Clínica Moderna</h4>
                    <p class="text-sm text-gray-500 mb-2">1800 - 1900</p>
                    <p class="text-gray-600 mb-4">La era de la bacteriología con Pasteur y Koch, la anestesia, la antisepsia y el nacimiento de la salud pública.</p>
                    <button onclick="openModal('xix')" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition duration-300">Explorar Época</button>
                </div>

                <!-- Timeline Item: Siglo XX y Contemporánea -->
                <div class="relative timeline-item">
                    <h4 class="text-2xl font-semibold text-indigo-700">Siglo XX y Medicina Contemporánea</h4>
                    <p class="text-sm text-gray-500 mb-2">1900 - Presente</p>
                    <p class="text-gray-600 mb-4">Antibióticos, vacunas, trasplantes, genética y los nuevos dilemas éticos que redefine la tecnología médica.</p>
                    <button onclick="openModal('xx')" class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 transition duration-300">Explorar Época</button>
                </div>
            </div>
        </section>
        
        <!-- About Section -->
        <section id="about" class="mt-20 bg-white p-8 rounded-xl shadow-lg">
             <h3 class="text-3xl font-bold text-center mb-6">Acerca de Sapiens Medicus</h3>
             <p class="text-gray-700 text-center max-w-4xl mx-auto">
                Esta plataforma está diseñada para la cátedra de "Humanística" como una herramienta para comprender que la medicina es tanto una ciencia como un arte profundamente humano. A través de este viaje, buscamos fomentar el pensamiento crítico y la empatía, habilidades esenciales para el médico del futuro.
             </p>
        </section>

    </main>

    <!-- Modal -->
    <div id="modal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50 hidden">
        <div id="modal-content" class="bg-white rounded-2xl shadow-2xl w-full max-w-4xl max-h-[90vh] overflow-y-auto modal-content">
            <!-- Modal content will be injected here by JavaScript -->
        </div>
    </div>

    <script>
        const modal = document.getElementById('modal');
        const modalContent = document.getElementById('modal-content');

        const modalData = {
            antigua: {
                title: "Medicina Antigua",
                content: `
                    <div class="p-8">
                        <h3 class="text-3xl font-bold mb-2 text-indigo-700">Conceptos Clave</h3>
                        <p class="mb-4">La <strong>enfermedad</strong> era vista como un castigo divino o un desequilibrio de los humores corporales. La <strong>salud</strong> era la armonía con los dioses y la naturaleza. La <strong>vida</strong> y la <strong>muerte</strong> estaban en manos de fuerzas superiores.</p>
                        
                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Personajes Importantes</h3>
                        <ul class="list-disc list-inside mb-4">
                            <li><strong>Imhotep (Egipto):</strong> Considerado uno de los primeros médicos de la historia.</li>
                            <li><strong>Hipócrates (Grecia):</strong> Padre de la medicina occidental. Estableció la medicina como una disciplina separada de la teurgia y la filosofía.</li>
                            <li><strong>Galeno (Roma):</strong> Su obra influyó en la medicina occidental durante más de 1300 años.</li>
                        </ul>

                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Instrumental y Avances</h3>
                        <p class="mb-4">Se utilizaban bisturís de obsidiana, ventosas y trepanación. El mayor avance fue el desarrollo de la <strong>teoría de los humores</strong> y la observación clínica sistemática.</p>
                        
                        <div class="mt-8 bg-indigo-50 p-6 rounded-lg">
                            <h4 class="text-xl font-semibold mb-2 text-indigo-800">Actividad Cualitativa: Dilema Ético</h4>
                            <p class="mb-4">Eres un médico griego seguidor de Hipócrates. Un paciente importante te ofrece una gran suma de dinero para que le administres una sustancia que acelere su muerte y termine con su sufrimiento. El Juramento Hipocrático dice: "jamás daré a nadie medicamento mortal, por mucho que me soliciten".</p>
                            <textarea class="w-full p-2 border rounded-md mt-2" rows="4" placeholder="Describe cómo actuarías y justifica tu decisión basándote en la ética y conocimientos de tu época."></textarea>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 mt-2">Enviar Reflexión</button>
                        </div>
                    </div>
                `
            },
            media: {
                title: "Edad Media y Renacimiento",
                content: `
                    <div class="p-8">
                        <h3 class="text-3xl font-bold mb-2 text-indigo-700">Conceptos Clave</h3>
                        <p class="mb-4">La <strong>enfermedad</strong>, especialmente en pandemias como la Peste Negra, era vista como un castigo divino o un fenómeno miasmático. La <strong>muerte</strong> era una experiencia pública y colectiva. El Renacimiento reavivó el interés por el cuerpo humano, viendo la <strong>vida</strong> como un objeto de estudio.</p>
                        
                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Personajes Importantes</h3>
                        <ul class="list-disc list-inside mb-4">
                            <li><strong>Avicena (Mundo Islámico):</strong> Su "Canon de Medicina" fue un texto de referencia durante siglos.</li>
                            <li><strong>Paracelso:</strong> Desafió las enseñanzas galénicas, abogando por la observación y el uso de químicos.</li>
                            <li><strong>Andrés Vesalio:</strong> Revolucionó la anatomía con su obra "De humani corporis fabrica".</li>
                        </ul>

                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Instrumental y Avances</h3>
                        <p class="mb-4">Se desarrollaron herramientas para la cirugía de guerra y la amputación. El avance clave fue la <strong>imprenta</strong>, que permitió la diseminación masiva del conocimiento anatómico y médico.</p>
                        
                        <div class="mt-8 bg-indigo-50 p-6 rounded-lg">
                            <h4 class="text-xl font-semibold mb-2 text-indigo-800">Actividad Cualitativa: Análisis de Fuente</h4>
                            <p class="mb-4">Observa la pintura "El triunfo de la Muerte" de Brueghel el Viejo. Describe cómo la obra representa los conceptos de enfermedad, vida y muerte en el contexto de las grandes plagas. ¿Qué rol parece tener la medicina (o su ausencia) en esta representación?</p>
                            <textarea class="w-full p-2 border rounded-md mt-2" rows="4" placeholder="Escribe tu análisis aquí..."></textarea>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 mt-2">Enviar Análisis</button>
                        </div>
                    </div>
                `
            },
            cientifica: {
                 title: "Revolución Científica",
                 content: `
                    <div class="p-8">
                         <h3 class="text-3xl font-bold mb-2 text-indigo-700">Conceptos Clave</h3>
                         <p class="mb-4">La <strong>enfermedad</strong> comienza a ser entendida como un desarreglo mecánico o químico del cuerpo, observable y medible. La <strong>vida</strong> se ve como un fenómeno explicable por leyes físicas, distanciándose de la pura intervención divina. La <strong>muerte</strong> es un cese de funciones mecánicas.</p>
                        
                         <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Personajes Importantes</h3>
                         <ul class="list-disc list-inside mb-4">
                            <li><strong>William Harvey:</strong> Describió correctamente la circulación sanguínea, un pilar de la fisiología moderna.</li>
                            <li><strong>Antonie van Leeuwenhoek:</strong> Perfeccionó el microscopio y fue el primero en observar microorganismos ("animálculos").</li>
                         </ul>

                         <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Instrumental y Avances</h3>
                         <p class="mb-4">El <strong>microscopio</strong> fue la herramienta revolucionaria, abriendo un mundo invisible. El avance conceptual fue la aplicación rigurosa del <strong>método científico</strong> y la experimentación en medicina.</p>
                        
                         <div class="mt-8 bg-indigo-50 p-6 rounded-lg">
                            <h4 class="text-xl font-semibold mb-2 text-indigo-800">Actividad Cualitativa: Creación de Diario</h4>
                            <p class="mb-4">Imagina que eres el asistente de Antonie van Leeuwenhoek en 1676. Escribe una página de tu diario describiendo tu asombro, dudas y las posibles implicaciones de observar por primera vez los "pequeños animálculos" en una gota de agua. ¿Cómo crees que esto podría cambiar la idea de "enfermedad"?</p>
                            <textarea class="w-full p-2 border rounded-md mt-2" rows="4" placeholder="Fecha: 9 de Octubre de 1676..."></textarea>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 mt-2">Guardar Entrada</button>
                         </div>
                    </div>
                 `
            },
            xix: {
                title: "Siglo XIX: La Clínica Moderna",
                content: `
                    <div class="p-8">
                        <h3 class="text-3xl font-bold mb-2 text-indigo-700">Conceptos Clave</h3>
                        <p class="mb-4">La <strong>enfermedad</strong> se consolida como una entidad causada por agentes externos (bacterias) o fallos internos. La <strong>salud</strong> se convierte en un asunto público y una responsabilidad del Estado. La <strong>muerte</strong> en el hospital se vuelve más común, y se medicaliza.</p>
                        
                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Personajes Importantes</h3>
                        <ul class="list-disc list-inside mb-4">
                            <li><strong>Louis Pasteur & Robert Koch:</strong> Fundadores de la bacteriología, confirmaron la teoría de los gérmenes.</li>
                            <li><strong>Ignaz Semmelweis & Joseph Lister:</strong> Pioneros de la antisepsia y la higiene.</li>
                            <li><strong>Rudolf Virchow:</strong> Padre de la patología moderna ("Omnis cellula e cellula").</li>
                        </ul>

                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Instrumental y Avances</h3>
                        <p class="mb-4">El <strong>estetoscopio</strong>, el desarrollo de la <strong>anestesia</strong> con éter y cloroformo, y las técnicas de <strong>antisepsia</strong> cambiaron la cirugía para siempre.</p>
                        
                        <div class="mt-8 bg-indigo-50 p-6 rounded-lg">
                            <h4 class="text-xl font-semibold mb-2 text-indigo-800">Actividad Cualitativa: Foro de Debate</h4>
                            <p class="mb-4"><strong>Tema:</strong> La historia de Ignaz Semmelweis, cuyo descubrimiento sobre la importancia de lavarse las manos fue ridiculizado por la comunidad médica, nos muestra la resistencia al cambio. ¿Qué barreras (sociales, jerárquicas, cognitivas) existen hoy en la medicina que podrían estar frenando avances similares? Argumenta con un ejemplo actual si es posible.</p>
                            <textarea class="w-full p-2 border rounded-md mt-2" rows="4" placeholder="Inicia tu argumento aquí..."></textarea>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 mt-2">Publicar en el Foro</button>
                        </div>
                    </div>
                `
            },
            xx: {
                title: "Siglo XX y Medicina Contemporánea",
                content: `
                    <div class="p-8">
                        <h3 class="text-3xl font-bold mb-2 text-indigo-700">Conceptos Clave</h3>
                        <p class="mb-4">La <strong>salud</strong> se define por la OMS no solo como ausencia de enfermedad, sino como completo bienestar físico, mental y social. La tecnología redefine los límites entre la <strong>vida</strong> y la <strong>muerte</strong> (soporte vital, trasplantes). La <strong>enfermedad</strong> se aborda a nivel molecular y genético.</p>
                        
                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Personajes Importantes</h3>
                        <ul class="list-disc list-inside mb-4">
                            <li><strong>Alexander Fleming:</strong> Descubridor de la penicilina.</li>
                            <li><strong>Watson y Crick:</strong> Descifraron la estructura del ADN.</li>
                            <li><strong>Christiaan Barnard:</strong> Realizó el primer trasplante de corazón exitoso.</li>
                        </ul>

                        <h3 class="text-2xl font-bold mt-6 mb-2 text-indigo-700">Instrumental y Avances</h3>
                        <p class="mb-4"><strong>Antibióticos</strong>, <strong>vacunas</strong>, <strong>tecnología de imagen</strong> (Rayos X, TAC, RMN), <strong>ingeniería genética</strong> y <strong>terapias génicas</strong>.</p>
                        
                        <div class="mt-8 bg-indigo-50 p-6 rounded-lg">
                            <h4 class="text-xl font-semibold mb-2 text-indigo-800">Actividad Cualitativa: Dilema Ético Moderno</h4>
                            <p class="mb-4">Un paciente con una enfermedad terminal en fase avanzada y con grandes sufrimientos solicita la eutanasia, un procedimiento legal en tu país bajo ciertas condiciones. Sin embargo, tus convicciones personales entran en conflicto con esta práctica. La familia del paciente está dividida. ¿Cómo manejas esta situación, equilibrando la autonomía del paciente, tus propias convicciones y la ética profesional?</p>
                            <textarea class="w-full p-2 border rounded-md mt-2" rows="4" placeholder="Describe tu plan de acción y el razonamiento detrás de él."></textarea>
                            <button class="bg-indigo-600 text-white px-4 py-2 rounded-lg hover:bg-indigo-700 mt-2">Enviar Reflexión</button>
                        </div>
                    </div>
                `
            }
        };

        function openModal(era) {
            const data = modalData[era];
            if (!data) return;

            modalContent.innerHTML = `
                <div class="flex justify-between items-center p-6 bg-gray-100 rounded-t-2xl">
                    <h2 class="text-2xl font-bold text-gray-800">${data.title}</h2>
                    <button onclick="closeModal()" class="text-gray-500 hover:text-gray-800 text-2xl">&times;</button>
                </div>
                ${data.content}
            `;
            modal.classList.remove('hidden');
            document.body.style.overflow = 'hidden'; // Prevent background scrolling
        }

        function closeModal() {
            modal.classList.add('hidden');
            document.body.style.overflow = 'auto';
        }

        // Close modal on escape key press
        window.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && !modal.classList.contains('hidden')) {
                closeModal();
            }
        });

        // Close modal on outside click
        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                closeModal();
            }
        });

    </script>
</body>

</html>

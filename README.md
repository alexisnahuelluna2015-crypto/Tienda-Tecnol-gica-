# Tienda-Tecnol-gica-
Hola bienvenido al emprendimiento estamos trabajando para que sea rápido y seguro🌐
import { useEffect, useState } from "react";

export default function LandingProductoDigital() {
  const [timeLeft, setTimeLeft] = useState({
    hours: 23,
    minutes: 59,
    seconds: 59,
  });

  useEffect(() => {
    const timer = setInterval(() => {
      setTimeLeft((prev) => {
        let { hours, minutes, seconds } = prev;
        if (seconds > 0) {
          seconds--;
        } else {
          if (minutes > 0) {
            minutes--;
            seconds = 59;
          } else {
            if (hours > 0) {
              hours--;
              minutes = 59;
              seconds = 59;
            }
          }
        }
        return { hours, minutes, seconds };
      });
    }, 1000);

    return () => clearInterval(timer);
  }, []);

  return (
    <div className="min-h-screen bg-gradient-to-b from-white to-gray-50 text-gray-800">
      {/* HERO */}
      <section className="max-w-6xl mx-auto px-6 py-20 grid md:grid-cols-2 gap-12 items-center">
        <div>
          <h1 className="text-4xl md:text-5xl font-bold leading-tight mb-6">
            Aprende a dominar [TU RESULTADO] en tiempo récord 🚀
          </h1>
          <p className="text-lg text-gray-600 mb-8">
            El método paso a paso que te ayudará a lograr [beneficio principal] sin
            perder tiempo ni cometer errores innecesarios.
          </p>
          <div className="flex gap-4">
            <button className="bg-black text-white px-8 py-4 rounded-2xl shadow-lg hover:scale-105 transition">
              Comprar ahora
            </button>
            <button className="border border-gray-300 px-8 py-4 rounded-2xl hover:bg-gray-100 transition">
              Ver detalles
            </button>
          </div>
        </div>
        <div className="bg-white p-8 rounded-2xl shadow-xl">
          <div className="h-64 bg-gray-200 rounded-xl flex items-center justify-center">
            <span className="text-gray-500">Imagen / Mockup del Producto</span>
          </div>
        </div>
      </section>

      {/* PROBLEMA */}
      <section className="bg-white py-20">
        <div className="max-w-4xl mx-auto px-6 text-center">
          <h2 className="text-3xl font-bold mb-6">
            ¿Te pasa que intentas [problema] pero no ves resultados?
          </h2>
          <p className="text-gray-600 text-lg">
            La mayoría de las personas fracasan porque no tienen un sistema claro.
            Saltan de estrategia en estrategia sin una guía estructurada.
          </p>
        </div>
      </section>

      {/* SOLUCIÓN */}
      <section className="py-20">
        <div className="max-w-6xl mx-auto px-6 grid md:grid-cols-3 gap-8">
          {["Paso 1", "Paso 2", "Paso 3"].map((item, i) => (
            <div
              key={i}
              className="bg-white p-8 rounded-2xl shadow-md hover:shadow-xl transition"
            >
              <h3 className="text-xl font-semibold mb-4">{item}</h3>
              <p className="text-gray-600">
                Explicación clara y práctica para avanzar de manera estructurada.
              </p>
            </div>
          ))}
        </div>
      </section>

      {/* QUÉ INCLUYE */}
      <section className="bg-white py-20">
        <div className="max-w-5xl mx-auto px-6">
          <h2 className="text-3xl font-bold text-center mb-12">
            ¿Qué incluye el producto?
          </h2>
          <div className="grid md:grid-cols-2 gap-8">
            {["Módulos completos", "Plantillas descargables", "Bonos exclusivos", "Actualizaciones futuras"].map(
              (item, i) => (
                <div key={i} className="flex items-start gap-4">
                  <div className="text-2xl">✔️</div>
                  <p className="text-lg">{item}</p>
                </div>
              )
            )}
          </div>
        </div>
      </section>

      {/* TESTIMONIOS */}
      <section className="py-20">
        <div className="max-w-6xl mx-auto px-6">
          <h2 className="text-3xl font-bold text-center mb-12">
            Lo que dicen nuestros clientes
          </h2>
          <div className="grid md:grid-cols-3 gap-8">
            {[1, 2, 3].map((item) => (
              <div key={item} className="bg-white p-8 rounded-2xl shadow-md">
                <p className="text-gray-600 mb-4">
                  "Este producto cambió completamente mi forma de trabajar."
                </p>
                <p className="font-semibold">Cliente {item}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* PRECIO */}
      <section className="bg-black text-white py-20">
        <div className="max-w-4xl mx-auto px-6 text-center">
          <h2 className="text-3xl font-bold mb-6">Oferta especial por tiempo limitado</h2>
          <p className="text-lg mb-4 line-through text-gray-400">$199</p>
          <p className="text-5xl font-bold mb-8">$49</p>
          <button className="bg-white text-black px-10 py-4 rounded-2xl font-semibold hover:scale-105 transition">
            Obtener acceso inmediato
          </button>
          <p className="text-gray-400 mt-6">Garantía de satisfacción de 7 días</p>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="py-10 text-center text-gray-500 text-sm">
        © {new Date().getFullYear()} Tu Marca. Todos los derechos reservados.
      </footer>
    </div>
  );
}

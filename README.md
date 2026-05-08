# scelo-tuckshop
export default function TuckshopWebsite() {
  const products = [
    { name: 'Chips', price: 'R15' },
    { name: 'Cold Drinks', price: 'R20' },
    { name: 'Chocolate', price: 'R12' },
    { name: 'Instant Noodles', price: 'R18' },
    { name: 'Energy Drinks', price: 'R25' },
    { name: 'Toiletries', price: 'From R10' }
  ];

  return (
    <div className="min-h-screen bg-gray-100 text-gray-900">
      {/* Hero Section */}
      <section className="bg-green-600 text-white py-20 text-center">
        <h1 className="text-5xl font-bold">SCELO'S TUCKSHOP</h1>
        <p className="mt-4 text-xl">Your late-night snack plug at residence 🍫🥤</p>
        <button className="mt-6 bg-white text-green-600 px-6 py-3 rounded-2xl font-semibold shadow-lg hover:scale-105 transition">
          Order Now
        </button>
      </section>

      {/* About */}
      <section className="py-12 px-6 text-center">
        <h2 className="text-3xl font-bold mb-4">About Us</h2>
        <p className="max-w-2xl mx-auto text-lg text-gray-700">
          We serve students with snacks, drinks, toiletries, and essentials when they need them most — especially during late-night study sessions.
        </p>
      </section>

      {/* Products */}
      <section className="py-12 px-6 bg-white">
        <h2 className="text-3xl font-bold text-center mb-8">Popular Products</h2>
        <div className="grid md:grid-cols-3 gap-6 max-w-5xl mx-auto">
          {products.map((product, index) => (
            <div key={index} className="bg-gray-100 p-6 rounded-2xl shadow-md text-center hover:shadow-xl transition">
              <h3 className="text-xl font-semibold">{product.name}</h3>
              <p className="text-green-600 font-bold mt-2">{product.price}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section className="py-12 px-6 text-center">
        <h2 className="text-3xl font-bold mb-4">Order via WhatsApp</h2>
        <p className="text-lg text-gray-700">Need snacks? Place your order instantly.</p>
        <a
          href="https://wa.me/27700000000"
          className="inline-block mt-6 bg-green-500 text-white px-6 py-3 rounded-2xl font-semibold shadow-lg hover:bg-green-600 transition"
        >
          Chat on WhatsApp
        </a>
      </section>

      {/* Footer */}
      <footer className="bg-black text-white text-center py-6 mt-10">
        <p>© 2026 Scelo's Tuckshop | Open Late for Students</p>
      </footer>
    </div>
  );
}

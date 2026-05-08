# Ababasfastfood
  import { useState } from 'react';

export default function AbabasFastFoodWebsite() {
  const [selectedPayment, setSelectedPayment] = useState('prepaid');

  const menuItems = [
    {
      name: 'Momos',
      price:89
      
  import { useState } from 'react';

export default function AbabasFastFoodWebsite() {
  const [selectedPayment, setSelectedPayment] = useState('prepaid');

  const menuItems = [
    {
      name: 'Momos',
      price: '₹79',
      image: 'https://images.unsplash.com/photo-1626082927389-6cd097cdc6ec?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Burger',
      price: '₹89',
      image: 'https://images.unsplash.com/photo-1568901346375-23c9450c58cd?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Fries',
      price: '₹90',
      image: 'https://images.unsplash.com/photo-1573080496219-bb080dd4f877?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Roll',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1530469912745-a215c6b256ea?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Chilly Potato',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1518013431117-eb1465fa5752?q=80&w=1200&auto=format&fit=crop'
    }
  ];

  return (
    <div className="bg-black text-white min-h-screen font-sans">
      {/* Hero Section */}
      <section
        className="relative h-screen flex items-center justify-center text-center bg-cover bg-center"
        style={{
          backgroundImage:
            "url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1600&auto=format&fit=crop')"
        }}
      >
        <div className="absolute inset-0 bg-black/70"></div>

        <div className="relative z-10 px-6 animate-pulse">
          <h1 className="text-5xl md:text-7xl font-extrabold text-yellow-400 drop-shadow-lg">
            Ababas Fast Food Stall
          </h1>

          <p className="mt-6 text-xl md:text-2xl text-gray-200 max-w-2xl mx-auto">
            Taste The Real Street Food Magic 🍔🔥<br />
            Momos • Burger • Fries • Roll • Chilly Potato
          </p>

          <div className="mt-8 flex flex-wrap gap-4 justify-center">
            <a
              href="tel:9917838758"
              className="bg-red-600 hover:bg-red-700 transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Call Now
            </a>

            <button
              className="bg-yellow-500 hover:bg-yellow-600 text-black transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Order Now
            </button>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section className="py-20 px-6 bg-zinc-900 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-6">
          About Us
        </h2>

        <p className="max-w-3xl mx-auto text-lg text-gray-300 leading-8">
          Ababas Fast Food Stall brings delicious and hygienic fast food with
          amazing taste and affordable prices. Enjoy fresh Momos, Burgers,
          Crispy Fries, Rolls and spicy Chilly Potato with family and friends.
        </p>
      </section>

      {/* Menu Section */}
      <section className="py-20 px-6 bg-black">
        <h2 className="text-4xl font-bold text-center text-yellow-400 mb-14">
          Our Special Menu
        </h2>

        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 max-w-7xl mx-auto">
          {menuItems.map((item, index) => (
            <div
              key={index}
              className="bg-zinc-900 rounded-3xl overflow-hidden shadow-2xl hover:scale-105 transition-all duration-500"
            >
              <img
                src={item.image}
                alt={item.name}
                className="h-64 w-full object-cover"
              />

              <div className="p-6 text-center">
                <h3 className="text-3xl font-bold text-white">{item.name}</h3>

                <p className="text-yellow-400 text-2xl mt-2 font-semibold">
                  {item.price}
                </p>

                <div className="mt-5 space-y-3">
                  <button
                    onClick={() => alert(`Order placed for ${item.name}`)}
                    className="w-full bg-red-600 hover:bg-red-700 px-6 py-3 rounded-xl font-bold transition-all duration-300"
                  >
                    Order Now
                  </button>

                  <div className="flex justify-center gap-3 text-sm">
                    <span className="bg-green-600 px-3 py-2 rounded-lg font-semibold">
                      Prepaid Payment
                    </span>

                    <span className="bg-yellow-500 text-black px-3 py-2 rounded-lg font-semibold">
                      Cash on Delivery
                    </span>
                  </div>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Offer Section */}
      <section className="py-20 bg-gradient-to-r from-red-700 to-yellow-500 text-center px-6">
        <h2 className="text-5xl font-extrabold mb-4">
          Special Combo Offer 🎉
        </h2>

        <p className="text-2xl font-semibold">
          Buy 2 Burgers & Get Fries Free
        </p>
      </section>

      {/* Payment & Order Section */}
      <section className="py-20 px-6 bg-zinc-900">
        <div className="max-w-3xl mx-auto bg-black rounded-3xl p-8 shadow-2xl">
          <h2 className="text-4xl font-bold text-center text-yellow-400 mb-8">
            Place Your Order
          </h2>

          <div className="space-y-5">
            <input
              type="text"
              placeholder="Enter Your Name"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <input
              type="tel"
              placeholder="Enter Mobile Number"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <textarea
              placeholder="Enter Delivery Address"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700 h-32"
            ></textarea>

            <div>
              <h3 className="text-xl font-bold mb-4 text-white">
                Select Payment Method
              </h3>

              <div className="flex flex-wrap gap-4">
                <button
                  onClick={() => setSelectedPayment('prepaid')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'prepaid' ? 'bg-green-600' : 'bg-zinc-700'}`}
                >
                  Online Prepaid
                </button>

                <button
                  onClick={() => setSelectedPayment('cod')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'cod' ? 'bg-yellow-500 text-black' : 'bg-zinc-700'}`}
                >
                  Cash On Delivery
                </button>
              </div>
            </div>

            <button
              onClick={() => {
                if (selectedPayment === 'prepaid') {
                  alert('Razorpay Payment Gateway Will Open Here');
                } else {
                  alert('Order Confirmed With Cash On Delivery');
                }
              }}
              className="w-full bg-red-600 hover:bg-red-700 py-4 rounded-2xl text-xl font-bold transition-all duration-300"
            >
              Confirm Order
            </button>

            <p className="text-center text-gray-400 text-sm">
              Razorpay / UPI / Debit Card / COD Supported
            </p>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section className="py-20 px-6 bg-zinc-950 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-8">
          Contact Us
        </h2>

        <div className="space-y-4 text-xl text-gray-300">
          <p>
            📞 Phone: <span className="text-white">99178 38758</span>
          </p>

          <p>
            📍 Visit Ababas Fast Food Stall  shravan Nagar sewla jaat
          </p>
        </div>

        <div className="mt-8 flex flex-col items-center gap-4">
          <button className="bg-red-600 hover:bg-red-700 px-8 py-4 rounded-2xl text-xl font-bold transition-all duration-300 shadow-2xl">
            Place Your Order
          </button>

          <div className="flex gap-4 flex-wrap justify-center">
            <span className="bg-green-600 px-5 py-3 rounded-xl font-semibold">
              Online Prepaid Payment Available
            </span>

            <span className="bg-yellow-500 text-black px-5 py-3 rounded-xl font-semibold">
              Cash On Delivery Available
            </span>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black border-t border-zinc-800 py-6 text-center text-gray-400">
        © 2026 Ababas Fast Food Stall | All Rights Reserved
      </footer>
    </div>
  
      
  import { useState } from 'react';

export default function AbabasFastFoodWebsite() {
  const [selectedPayment, setSelectedPayment] = useState('prepaid');

  const menuItems = [
    {
      name: 'Momos',
      price: '₹89',
      image: 'https://images.unsplash.com/photo-1626082927389-6cd097cdc6ec?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Burger',
      price: '₹89',
      image: 
  import { useState } from 'react';

export default function AbabasFastFoodWebsite() {
  const [selectedPayment, setSelectedPayment] = useState('prepaid');

  const menuItems = [
    {
      name: 'Momos',
      price: '₹79',
      image: 'https://images.unsplash.com/photo-1626082927389-6cd097cdc6ec?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Burger',
      price: '₹89',
      image: 'https://images.unsplash.com/photo-1568901346375-23c9450c58cd?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Fries',
      price: '₹90',
      image: 'https://images.unsplash.com/photo-1573080496219-bb080dd4f877?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Roll',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1530469912745-a215c6b256ea?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Chilly Potato',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1518013431117-eb1465fa5752?q=80&w=1200&auto=format&fit=crop'
    }
  ];

  return (
    <div className="bg-black text-white min-h-screen font-sans">
      {/* Hero Section */}
      <section
        className="relative h-screen flex items-center justify-center text-center bg-cover bg-center"
        style={{
          backgroundImage:
            "url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1600&auto=format&fit=crop')"
        }}
      >
        <div className="absolute inset-0 bg-black/70"></div>

        <div className="relative z-10 px-6 animate-pulse">
          <h1 className="text-5xl md:text-7xl font-extrabold text-yellow-400 drop-shadow-lg">
            Ababas Fast Food Stall
          </h1>

          <p className="mt-6 text-xl md:text-2xl text-gray-200 max-w-2xl mx-auto">
            Taste The Real Street Food Magic 🍔🔥<br />
            Momos • Burger • Fries • Roll • Chilly Potato
          </p>

          <div className="mt-8 flex flex-wrap gap-4 justify-center">
            <a
              href="tel:9917838758"
              className="bg-red-600 hover:bg-red-700 transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Call Now
            </a>

            <button
              className="bg-yellow-500 hover:bg-yellow-600 text-black transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Order Now
            </button>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section className="py-20 px-6 bg-zinc-900 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-6">
          About Us
        </h2>

        <p className="max-w-3xl mx-auto text-lg text-gray-300 leading-8">
          Ababas Fast Food Stall brings delicious and hygienic fast food with
          amazing taste and affordable prices. Enjoy fresh Momos, Burgers,
          Crispy Fries, Rolls and spicy Chilly Potato with family and friends.
        </p>
      </section>

      {/* Menu Section */}
      <section className="py-20 px-6 bg-black">
        <h2 className="text-4xl font-bold text-center text-yellow-400 mb-14">
          Our Special Menu
        </h2>

        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 max-w-7xl mx-auto">
          {menuItems.map((item, index) => (
            <div
              key={index}
              className="bg-zinc-900 rounded-3xl overflow-hidden shadow-2xl hover:scale-105 transition-all duration-500"
            >
              <img
                src={item.image}
                alt={item.name}
                className="h-64 w-full object-cover"
              />

              <div className="p-6 text-center">
                <h3 className="text-3xl font-bold text-white">{item.name}</h3>

                <p className="text-yellow-400 text-2xl mt-2 font-semibold">
                  {item.price}
                </p>

                <div className="mt-5 space-y-3">
                  <button
                    onClick={() => alert(`Order placed for ${item.name}`)}
                    className="w-full bg-red-600 hover:bg-red-700 px-6 py-3 rounded-xl font-bold transition-all duration-300"
                  >
                    Order Now
                  </button>

                  <div className="flex justify-center gap-3 text-sm">
                    <span className="bg-green-600 px-3 py-2 rounded-lg font-semibold">
                      Prepaid Payment
                    </span>

                    <span className="bg-yellow-500 text-black px-3 py-2 rounded-lg font-semibold">
                      Cash on Delivery
                    </span>
                  </div>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Offer Section */}
      <section className="py-20 bg-gradient-to-r from-red-700 to-yellow-500 text-center px-6">
        <h2 className="text-5xl font-extrabold mb-4">
          Special Combo Offer 🎉
        </h2>

        <p className="text-2xl font-semibold">
          Buy 2 Burgers & Get Fries Free
        </p>
      </section>

      {/* Payment & Order Section */}
      <section className="py-20 px-6 bg-zinc-900">
        <div className="max-w-3xl mx-auto bg-black rounded-3xl p-8 shadow-2xl">
          <h2 className="text-4xl font-bold text-center text-yellow-400 mb-8">
            Place Your Order
          </h2>

          <div className="space-y-5">
            <input
              type="text"
              placeholder="Enter Your Name"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <input
              type="tel"
              placeholder="Enter Mobile Number"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <textarea
              placeholder="Enter Delivery Address"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700 h-32"
            ></textarea>

            <div>
              <h3 className="text-xl font-bold mb-4 text-white">
                Select Payment Method
              </h3>

              <div className="flex flex-wrap gap-4">
                <button
                  onClick={() => setSelectedPayment('prepaid')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'prepaid' ? 'bg-green-600' : 'bg-zinc-700'}`}
                >
                  Online Prepaid
                </button>

                <button
                  onClick={() => setSelectedPayment('cod')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'cod' ? 'bg-yellow-500 text-black' : 'bg-zinc-700'}`}
                >
                  Cash On Delivery
                </button>
              </div>
            </div>

            <button
              onClick={() => {
                if (selectedPayment === 'prepaid') {
                  alert('Razorpay Payment Gateway Will Open Here');
                } else {
                  alert('Order Confirmed With Cash On Delivery');
                }
              }}
              className="w-full bg-red-600 hover:bg-red-700 py-4 rounded-2xl text-xl font-bold transition-all duration-300"
            >
              Confirm Order
            </button>

            <p className="text-center text-gray-400 text-sm">
              Razorpay / UPI / Debit Card / COD Supported
            </p>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section className="py-20 px-6 bg-zinc-950 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-8">
          Contact Us
        </h2>

        <div className="space-y-4 text-xl text-gray-300">
          <p>
            📞 Phone: <span className="text-white">99178 38758</span>
          </p>

          <p>
            📍 Visit Ababas Fast Food Stall  shravan Nagar sewla jaat
          </p>
        </div>

        <div className="mt-8 flex flex-col items-center gap-4">
          <button className="bg-red-600 hover:bg-red-700 px-8 py-4 rounded-2xl text-xl font-bold transition-all duration-300 shadow-2xl">
            Place Your Order
          </button>

          <div className="flex gap-4 flex-wrap justify-center">
            <span className="bg-green-600 px-5 py-3 rounded-xl font-semibold">
              Online Prepaid Payment Available
            </span>

            <span className="bg-yellow-500 text-black px-5 py-3 rounded-xl font-semibold">
              Cash On Delivery Available
            </span>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black border-t border-zinc-800 py-6 text-center text-gray-400">
        © 2026 Ababas Fast Food Stall | All Rights Reserved
      </footer>
    </div>
  );
}

    },
    {
      name: 'Fries',
      price: '₹90',
      image: 'https://images.unsplash.com/photo-1573080496219-bb080dd4f877?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Roll',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1530469912745-a215c6b256ea?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Chilly Potato',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1518013431117-eb1465fa5752?q=80&w=1200&auto=format&fit=crop'
    }
  ];

  return (
    <div className="bg-black text-white min-h-screen font-sans">
      {/* Hero Section */}
      <section
        className="relative h-screen flex items-center justify-center text-center bg-cover bg-center"
        style={{
          backgroundImage:
            "url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1600&auto=format&fit=crop')"
        }}
      >
        <div className="absolute inset-0 bg-black/70"></div>

        <div className="relative z-10 px-6 animate-pulse">
          <h1 className="text-5xl md:text-7xl font-extrabold text-yellow-400 drop-shadow-lg">
            Ababas Fast Food Stall
          </h1>

          <p className="mt-6 text-xl md:text-2xl text-gray-200 max-w-2xl mx-auto">
            Taste The Real Street Food Magic 🍔🔥<br />
            Momos • Burger • Fries • Roll • Chilly Potato
          </p>

          <div className="mt-8 flex flex-wrap gap-4 justify-center">
            <a
              href="tel:9917838758"
              className="bg-red-600 hover:bg-red-700 transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Call Now
            </a>

            <button
              className="bg-yellow-500 hover:bg-yellow-600 text-black transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Order Now
            </button>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section className="py-20 px-6 bg-zinc-900 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-6">
          About Us
        </h2>

        <p className="max-w-3xl mx-auto text-lg text-gray-300 leading-8">
          Ababas Fast Food Stall brings delicious and hygienic fast food with
          amazing taste and affordable prices. Enjoy fresh Momos, Burgers,
          Crispy Fries, Rolls and spicy Chilly Potato with family and friends.
        </p>
      </section>

      {/* Menu Section */}
      <section className="py-20 px-6 bg-black">
        <h2 className="text-4xl font-bold text-center text-yellow-400 mb-14">
          Our Special Menu
        </h2>

        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 max-w-7xl mx-auto">
          {menuItems.map((item, index) => (
            <div
              key={index}
              className="bg-zinc-900 rounded-3xl overflow-hidden shadow-2xl hover:scale-105 transition-all duration-500"
            >
              <img
                src={item.image}
                alt={item.name}
                className="h-64 w-full object-cover"
              />

              <div className="p-6 text-center">
                <h3 className="text-3xl font-bold text-white">{item.name}</h3>

                <p className="text-yellow-400 text-2xl mt-2 font-semibold">
                  {item.price}
                </p>

                <div className="mt-5 space-y-3">
                  <button
                    onClick={() => alert(`Order placed for ${item.name}`)}
                    className="w-full bg-red-600 hover:bg-red-700 px-6 py-3 rounded-xl font-bold transition-all duration-300"
                  >
                    Order Now
                  </button>

                  <div className="flex justify-center gap-3 text-sm">
                    <span className="bg-green-600 px-3 py-2 rounded-lg font-semibold">
                      Prepaid Payment
                    </span>

                    <span className="bg-yellow-500 text-black px-3 py-2 rounded-lg font-semibold">
                      Cash on Delivery
                    </span>
                  </div>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Offer Section */}
      <section className="py-20 bg-gradient-to-r from-red-700 to-yellow-500 text-center px-6">
        <h2 className="text-5xl font-extrabold mb-4">
          Special Combo Offer 🎉
        </h2>

        <p className="text-2xl font-semibold">
          Buy 2 Burgers & Get Fries Free
        </p>
      </section>

      {/* Payment & Order Section */}
      <section className="py-20 px-6 bg-zinc-900">
        <div className="max-w-3xl mx-auto bg-black rounded-3xl p-8 shadow-2xl">
          <h2 className="text-4xl font-bold text-center text-yellow-400 mb-8">
            Place Your Order
          </h2>

          <div className="space-y-5">
            <input
              type="text"
              placeholder="Enter Your Name"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <input
              type="tel"
              placeholder="Enter Mobile Number"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <textarea
              placeholder="Enter Delivery Address"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700 h-32"
            ></textarea>

            <div>
              <h3 className="text-xl font-bold mb-4 text-white">
                Select Payment Method
              </h3>

              <div className="flex flex-wrap gap-4">
                <button
                  onClick={() => setSelectedPayment('prepaid')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'prepaid' ? 'bg-green-600' : 'bg-zinc-700'}`}
                >
                  Online Prepaid
                </button>

                <button
                  onClick={() => setSelectedPayment('cod')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'cod' ? 'bg-yellow-500 text-black' : 'bg-zinc-700'}`}
                >
                  Cash On Delivery
                </button>
              </div>
            </div>

            <button
              onClick={() => {
                if (selectedPayment === 'prepaid') {
                  alert('Razorpay Payment Gateway Will Open Here');
                } else {
                  alert('Order Confirmed With Cash On Delivery');
                }
              }}
              className="w-full bg-red-600 hover:bg-red-700 py-4 rounded-2xl text-xl font-bold transition-all duration-300"
            >
              Confirm Order
            </button>

            <p className="text-center text-gray-400 text-sm">
              Razorpay / UPI / Debit Card / COD Supported
            </p>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section className="py-20 px-6 bg-zinc-950 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-8">
          Contact Us
        </h2>

        <div className="space-y-4 text-xl text-gray-300">
          <p>
            📞 Phone: <span className="text-white">99178 38758</span>
          </p>

          <p>
            📍 Visit Ababas Fast Food Stall  shravan Nagar sewla jaat
          </p>
        </div>

        <div className="mt-8 flex flex-col items-center gap-4">
          <button className="bg-red-600 hover:bg-red-700 px-8 py-4 rounded-2xl text-xl font-bold transition-all duration-300 shadow-2xl">
            Place Your Order
          </button>

          <div className="flex gap-4 flex-wrap justify-center">
            <span className="bg-green-600 px-5 py-3 rounded-xl font-semibold">
              Online Prepaid Payment Available
            </span>

            <span className="bg-yellow-500 text-black px-5 py-3 rounded-xl font-semibold">
              Cash On Delivery Available
            </span>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black border-t border-zinc-800 py-6 text-center text-gray-400">
        © 2026 Ababas Fast Food Stall | All Rights Reserved
      </footer>
    </div>
  );
}

    },
    {
      name: 'Burger',
      price: '₹89',
      image: 'https://images.unsplash.com/photo-1568901346375-23c9450c58cd?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Fries',
      price: '₹90',
      image: 'https://images.unsplash.com/photo-1573080496219-bb080dd4f877?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Roll',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1530469912745-a215c6b256ea?q=80&w=1200&auto=format&fit=crop'
    },
    {
      name: 'Chilly Potato',
      price: '₹99',
      image: 'https://images.unsplash.com/photo-1518013431117-eb1465fa5752?q=80&w=1200&auto=format&fit=crop'
    }
  ];

  return (
    <div className="bg-black text-white min-h-screen font-sans">
      {/* Hero Section */}
      <section
        className="relative h-screen flex items-center justify-center text-center bg-cover bg-center"
        style={{
          backgroundImage:
            "url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?q=80&w=1600&auto=format&fit=crop')"
        }}
      >
        <div className="absolute inset-0 bg-black/70"></div>

        <div className="relative z-10 px-6 animate-pulse">
          <h1 className="text-5xl md:text-7xl font-extrabold text-yellow-400 drop-shadow-lg">
            Ababas Fast Food Stall
          </h1>

          <p className="mt-6 text-xl md:text-2xl text-gray-200 max-w-2xl mx-auto">
            Taste The Real Street Food Magic 🍔🔥<br />
            Momos • Burger • Fries • Roll • Chilly Potato
          </p>

          <div className="mt-8 flex flex-wrap gap-4 justify-center">
            <a
              href="tel:9917838758"
              className="bg-red-600 hover:bg-red-700 transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Call Now
            </a>

            <button
              className="bg-yellow-500 hover:bg-yellow-600 text-black transition-all duration-300 px-8 py-4 rounded-2xl text-lg font-bold shadow-2xl"
            >
              Order Now
            </button>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section className="py-20 px-6 bg-zinc-900 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-6">
          About Us
        </h2>

        <p className="max-w-3xl mx-auto text-lg text-gray-300 leading-8">
          Ababas Fast Food Stall brings delicious and hygienic fast food with
          amazing taste and affordable prices. Enjoy fresh Momos, Burgers,
          Crispy Fries, Rolls and spicy Chilly Potato with family and friends.
        </p>
      </section>

      {/* Menu Section */}
      <section className="py-20 px-6 bg-black">
        <h2 className="text-4xl font-bold text-center text-yellow-400 mb-14">
          Our Special Menu
        </h2>

        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 max-w-7xl mx-auto">
          {menuItems.map((item, index) => (
            <div
              key={index}
              className="bg-zinc-900 rounded-3xl overflow-hidden shadow-2xl hover:scale-105 transition-all duration-500"
            >
              <img
                src={item.image}
                alt={item.name}
                className="h-64 w-full object-cover"
              />

              <div className="p-6 text-center">
                <h3 className="text-3xl font-bold text-white">{item.name}</h3>

                <p className="text-yellow-400 text-2xl mt-2 font-semibold">
                  {item.price}
                </p>

                <div className="mt-5 space-y-3">
                  <button
                    onClick={() => alert(`Order placed for ${item.name}`)}
                    className="w-full bg-red-600 hover:bg-red-700 px-6 py-3 rounded-xl font-bold transition-all duration-300"
                  >
                    Order Now
                  </button>

                  <div className="flex justify-center gap-3 text-sm">
                    <span className="bg-green-600 px-3 py-2 rounded-lg font-semibold">
                      Prepaid Payment
                    </span>

                    <span className="bg-yellow-500 text-black px-3 py-2 rounded-lg font-semibold">
                      Cash on Delivery
                    </span>
                  </div>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Offer Section */}
      <section className="py-20 bg-gradient-to-r from-red-700 to-yellow-500 text-center px-6">
        <h2 className="text-5xl font-extrabold mb-4">
          Special Combo Offer 🎉
        </h2>

        <p className="text-2xl font-semibold">
          Buy 2 Burgers & Get Fries Free
        </p>
      </section>

      {/* Payment & Order Section */}
      <section className="py-20 px-6 bg-zinc-900">
        <div className="max-w-3xl mx-auto bg-black rounded-3xl p-8 shadow-2xl">
          <h2 className="text-4xl font-bold text-center text-yellow-400 mb-8">
            Place Your Order
          </h2>

          <div className="space-y-5">
            <input
              type="text"
              placeholder="Enter Your Name"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <input
              type="tel"
              placeholder="Enter Mobile Number"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700"
            />

            <textarea
              placeholder="Enter Delivery Address"
              className="w-full p-4 rounded-xl bg-zinc-800 border border-zinc-700 h-32"
            ></textarea>

            <div>
              <h3 className="text-xl font-bold mb-4 text-white">
                Select Payment Method
              </h3>

              <div className="flex flex-wrap gap-4">
                <button
                  onClick={() => setSelectedPayment('prepaid')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'prepaid' ? 'bg-green-600' : 'bg-zinc-700'}`}
                >
                  Online Prepaid
                </button>

                <button
                  onClick={() => setSelectedPayment('cod')}
                  className={`px-6 py-3 rounded-xl font-bold ${selectedPayment === 'cod' ? 'bg-yellow-500 text-black' : 'bg-zinc-700'}`}
                >
                  Cash On Delivery
                </button>
              </div>
            </div>

            <button
              onClick={() => {
                if (selectedPayment === 'prepaid') {
                  alert('Razorpay Payment Gateway Will Open Here');
                } else {
                  alert('Order Confirmed With Cash On Delivery');
                }
              }}
              className="w-full bg-red-600 hover:bg-red-700 py-4 rounded-2xl text-xl font-bold transition-all duration-300"
            >
              Confirm Order
            </button>

            <p className="text-center text-gray-400 text-sm">
              Razorpay / UPI / Debit Card / COD Supported
            </p>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section className="py-20 px-6 bg-zinc-950 text-center">
        <h2 className="text-4xl font-bold text-yellow-400 mb-8">
          Contact Us
        </h2>

        <div className="space-y-4 text-xl text-gray-300">
          <p>
            📞 Phone: <span className="text-white">99178 38758</span>
          </p>

          <p>
            📍 Visit Ababas Fast Food Stall  shravan Nagar sewla jaat
          </p>
        </div>

        <div className="mt-8 flex flex-col items-center gap-4">
          <button className="bg-red-600 hover:bg-red-700 px-8 py-4 rounded-2xl text-xl font-bold transition-all duration-300 shadow-2xl">
            Place Your Order
          </button>

          <div className="flex gap-4 flex-wrap justify-center">
            <span className="bg-green-600 px-5 py-3 rounded-xl font-semibold">
              Online Prepaid Payment Available
            </span>

            <span className="bg-yellow-500 text-black px-5 py-3 rounded-xl font-semibold">
              Cash On Delivery Available
            </span>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black border-t border-zinc-800 py-6 text-center text-gray-400">
        © 2026 Ababas Fast Food Stall | All Rights Reserved
      </footer>
    </div>
  );
}

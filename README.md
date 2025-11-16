# Satilla-Gun-Works
import React from "react";

// Updated Satilla Gun Works Website — Larger Logo, Dark Forest Theme, Service Images

const logoSrc = "/static/Satilla_Gun_Works_Logo.jpeg";

// Placeholder service images — replace with real URLs later
const serviceImages = {
  cleaning: "https://images.unsplash.com/photo-1608580904621-287a3e1bdc5e?auto=format&fit=crop&w=600&q=60",
  trigger: "https://images.unsplash.com/photo-1581090464777-44a6a7a0f1b7?auto=format&fit=crop&w=600&q=60",
  accurizing: "https://images.unsplash.com/photo-1613570521744-ec2f43f5201d?auto=format&fit=crop&w=600&q=60",
  restoration: "https://images.unsplash.com/photo-1519681393784-d120267933ba?auto=format&fit=crop&w=600&q=60"
};

export default function SatillaLanding() {
  return (
    <div className="min-h-screen bg-fixed bg-cover bg-center text-white" style={{ backgroundImage: "url('https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=1500&q=80')" }}>

      <header className="max-w-6xl mx-auto p-6 flex items-center justify-between bg-black/40 backdrop-blur-sm rounded-xl mt-4 shadow-lg">
        <div className="flex items-center gap-4">
          <img src={logoSrc} alt="Satilla Gun Works" className="w-28 h-28 object-contain rounded-md shadow-lg" />
          <div>
            <h1 className="text-3xl font-extrabold tracking-tight">Satilla Gun Works</h1>
            <p className="text-sm text-gray-200">Professional gunsmithing • Repairs • Custom builds • Finishing</p>
          </div>
        </div>
        <nav className="hidden md:flex gap-6 items-center text-sm">
          <a href="#services" className="hover:text-green-300">Services</a>
          <a href="#pricing" className="hover:text-green-300">Pricing</a>
          <a href="#book" className="hover:text-green-300">Book</a>
          <a href="#contact" className="px-3 py-2 bg-green-800 text-white rounded-md shadow">Contact</a>
        </nav>
      </header>

      <main className="max-w-6xl mx-auto p-6">
        <section className="grid grid-cols-1 md:grid-cols-2 gap-8 items-center py-12 bg-black/40 rounded-xl p-6 mt-6 shadow-xl">
          <div>
            <h2 className="text-4xl font-extrabold leading-tight">Local, expert gunsmithing — done right.</h2>
            <p className="mt-4 text-lg text-gray-200">From routine safety checks to precision accurizing and restoration, Satilla Gun Works brings professional, insured gunsmith services — now available at partner shops or by appointment.</p>

            <div className="mt-6 flex gap-4">
              <a href="#book" className="inline-block px-5 py-3 bg-green-800 text-white rounded-md font-medium shadow-md">Book an appointment</a>
              <a href="#services" className="inline-block px-5 py-3 border border-gray-200 rounded-md text-gray-100 bg-black/40">View services</a>
            </div>

            <ul className="mt-6 grid grid-cols-1 sm:grid-cols-2 gap-3 text-sm text-gray-200">
              <li>• Bench inspections & diagnostics</li>
              <li>• Basic cleaning & complete disassembly</li>
              <li>• Trigger jobs / tuning</li>
              <li>• Bedding, action truing & accurizing</li>
              <li>• Refinishing & Cerakote (partnered)</li>
            </ul>
          </div>

          <div className="bg-black/40 rounded-xl shadow-md p-6 backdrop-blur-md">
            <h3 className="font-semibold text-white">Quick quote</h3>
            <p className="text-sm text-gray-200 mt-2">Tell us the service you need and we'll provide a fast estimate.</p>
            <form className="mt-4 grid gap-3">
              <input className="border p-3 rounded-md bg-white/80 text-black" placeholder="Your name" />
              <input className="border p-3 rounded-md bg-white/80 text-black" placeholder="Email or Phone" />
              <select className="border p-3 rounded-md bg-white/80 text-black">
                <option>Diagnostic / Bench</option>
                <option>Trigger / Sights</option>
                <option>Action / Bedding</option>
                <option>Full restoration</option>
              </select>
              <textarea className="border p-3 rounded-md bg-white/80 text-black" rows={3} placeholder="Brief description"></textarea>
              <div className="flex gap-2">
                <button type="button" className="px-4 py-2 bg-green-800 text-white rounded-md">Request quote</button>
                <button type="button" className="px-4 py-2 border rounded-md bg-white/20 text-white">Call us</button>
              </div>
            </form>
          </div>
        </section>

        {/* Service Cards with Images */}
        <section id="services" className="py-12">
          <h3 className="text-3xl font-bold text-white mb-6">Services</h3>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">

            <div className="bg-black/40 rounded-xl shadow-md p-4">
              <img src={serviceImages.cleaning} className="w-full h-40 object-cover rounded-md" />
              <h4 className="mt-4 text-xl font-semibold">Routine & Safety</h4>
              <p className="text-gray-200 mt-2">Cleaning, inspections, function checks and minor repairs.</p>
            </div>

            <div className="bg-black/40 rounded-xl shadow-md p-4">
              <img src={serviceImages.trigger} className="w-full h-40 object-cover rounded-md" />
              <h4 className="mt-4 text-xl font-semibold">Trigger & Performance</h4>
              <p className="text-gray-200 mt-2">Trigger jobs, tuning, accurizing, and sight installation.</p>
            </div>

            <div className="bg-black/40 rounded-xl shadow-md p-4">
              <img src={serviceImages.restoration} className="w-full h-40 object-cover rounded-md" />
              <h4 className="mt-4 text-xl font-semibold">Restoration</h4>
              <p className="text-gray-200 mt-2">Restorations, refinishing, and full custom builds.</p>
            </div>

          </div>
        </section>

        {/* Pricing Section */}
        <section id="pricing" className="py-12">
          <h3 className="text-3xl font-bold text-white mb-6">Pricing examples</h3>
          <div className="grid grid-cols-1 md:grid-cols-4 gap-6 text-sm text-gray-100">
            <div className="bg-black/40 rounded-xl p-5 shadow-sm">
              <div className="font-medium">Bench / Diagnostic</div>
              <div className="mt-2">$50 (credited if repair accepted)</div>
            </div>
            <div className="bg-black/40 rounded-xl p-5 shadow-sm">
              <div className="font-medium">Trigger / Sight install</div>
              <div className="mt-2">$75–$150</div>
            </div>
            <div className="bg-black/40 rounded-xl p-5 shadow-sm">
              <div className="font-medium">Sight/Optic installation w/ bore sighting</div>
              <div className="mt-2">$60–$120</div>
            </div>
            <div className="bg-black/40 rounded-xl p-5 shadow-sm">
              <div className="font-medium">Bedding / Action work</div>
              <div className="mt-2">$200–$600+</div>
            </div>
          </div>
        </section>

        {/* Contact */}
        <section id="contact" className="py-12">
          <h3 className="text-3xl font-bold text-white mb-4">Contact & Location</h3>
          <p className="text-gray-100">Email: info@satillagunworks.com</p>
          <p className="text-gray-100">Phone: (555) 123-4567</p>
        </section>
      </main>
    </div>
  );
}

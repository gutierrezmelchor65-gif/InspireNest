import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function InspireNest() {
  return (
    <div className="min-h-screen bg-white text-gray-800 font-sans">
      {/* Header */}
      <header className="w-full py-6 shadow-md bg-white sticky top-0 z-50">
        <div className="max-w-6xl mx-auto flex justify-between items-center px-4">
          <h1 className="text-3xl font-bold tracking-tight">InspireNest</h1>
          <nav className="space-x-6 text-lg">
            <a href="#products" className="hover:text-gray-500">Products</a>
            <a href="#about" className="hover:text-gray-500">About</a>
            <a href="#contact" className="hover:text-gray-500">Contact</a>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section className="w-full bg-gradient-to-r from-gray-100 to-gray-200 py-20 px-4">
        <div className="max-w-5xl mx-auto text-center">
          <motion.h2
            initial={{ opacity: 0, y: -20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6 }}
            className="text-5xl font-extrabold mb-4"
          >
            Motivation That Speaks to Your Soul
          </motion.h2>

          <motion.p
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.8 }}
            className="text-xl max-w-2xl mx-auto mb-8"
          >
            Discover beautiful wall art and digital ebooks filled with inspiring quotes that keep you going every day.
          </motion.p>

          <motion.div initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 1 }}>
            <a href="#products">
              <Button className="text-lg px-6 py-3 rounded-2xl shadow-lg">Shop Now</Button>
            </a>
          </motion.div>
        </div>
      </section>

      {/* Products Section */}
      <section id="products" className="max-w-6xl mx-auto py-20 px-4">
        <h3 className="text-4xl font-bold text-center mb-10">Best Sellers</h3>
        <div className="grid md:grid-cols-3 gap-8">
          {[1,2,3].map((item) => (
            <Card key={item} className="rounded-2xl shadow-md hover:shadow-xl transition">
              <CardContent className="p-4">
                <div className="h-64 bg-gray-200 rounded-xl mb-4"></div>
                <h4 className="text-xl font-semibold">Motivational Quote #{item}</h4>
                <p className="text-gray-600 text-sm mt-2">High‑resolution printable wall art.</p>
                <Button className="mt-4 w-full">View Product</Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="bg-gray-100 py-20 px-4">
        <div className="max-w-4xl mx-auto text-center">
          <h3 className="text-4xl font-bold mb-6">About InspireNest</h3>
          <p className="text-lg text-gray-700 max-w-2xl mx-auto">
            InspireNest was built to bring daily positivity into your space. Whether it’s a motivational wall art or a digital ebook, everything is crafted to uplift your mood, spark your ambition, and help you grow.
          </p>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="max-w-4xl mx-auto py-20 px-4 text-center">
        <h3 className="text-4xl font-bold mb-6">Contact</h3>
        <p className="text-lg text-gray-700 mb-4">Have questions or custom requests?</p>
        <Button className="px-6 py-3 rounded-2xl text-lg">Email Us</Button>
      </section>

      {/* Footer */}
      <footer className="text-center py-6 bg-gray-900 text-white">
        <p>&copy; {new Date().getFullYear()} InspireNest. All rights reserved.</p>
      </footer>
    </div>
  );
}


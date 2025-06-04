# the-green-wolffia25
WOLFFIAom "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Facebook, Instagram, ShoppingCart } from "lucide-react";

export default function HomePage() {
  return (
    <main className="min-h-screen bg-green-50 text-gray-800 font-sans">
      <header className="bg-white shadow p-4 flex justify-between items-center">
        <h1 className="text-2xl font-bold text-green-800">THE GREEN WOLFFIA</h1>
        <nav className="space-x-4">
          <a href="#about" className="text-green-700 hover:underline">เกี่ยวกับเรา / About</a>
          <a href="#products" className="text-green-700 hover:underline">สินค้า / Products</a>
          <a href="#contact" className="text-green-700 hover:underline">ติดต่อ / Contact</a>
          <ShoppingCart className="inline-block text-green-700" />
        </nav>
      </header>

      <section id="about" className="p-8 text-center bg-white">
        <h2 className="text-xl font-semibold mb-4">ทำความรู้จัก THE GREEN WOLFFIA</h2>
        <p className="max-w-2xl mx-auto">
          THE GREEN WOLFFIA คือแบรนด์ผลิตภัณฑ์แปรรูปจากไข่ผำคุณภาพสูง ปลอดสาร เน้นความยั่งยืน เพื่อสุขภาพและสิ่งแวดล้อม
        </p>
      </section>

      <section id="products" className="p-8 bg-green-100">
        <h2 className="text-xl font-semibold mb-6 text-center">สินค้า / Products</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          {[1, 2, 3].map((i) => (
            <Card key={i} className="rounded-2xl shadow-sm">
              <CardContent className="p-4">
                <img
                  src={`/product-${i}.jpg`}
                  alt={`Product ${i}`}
                  className="w-full h-40 object-cover rounded-xl mb-4"
                />
                <h3 className="font-semibold text-lg">ผลิตภัณฑ์ {i}</h3>
                <p className="text-sm text-gray-600">รายละเอียดสินค้าแบบย่อ</p>
                <Button className="mt-4 w-full bg-green-700 hover:bg-green-800 text-white">
                  เพิ่มในตะกร้า
                </Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      <section id="contact" className="p-8 bg-white">
        <h2 className="text-xl font-semibold mb-4 text-center">ติดต่อเรา / Contact</h2>
        <form className="max-w-xl mx-auto space-y-4">
          <Input placeholder="ชื่อ / Name" />
          <Input placeholder="อีเมล / Email" type="email" />
          <Textarea placeholder="ข้อความ / Message" />
          <Button className="bg-green-700 hover:bg-green-800 text-white">ส่งข้อความ / Send</Button>
        </form>
      </section>

      <footer className="p-4 bg-green-800 text-white flex flex-col md:flex-row justify-between items-center text-sm">
        <p>&copy; 2025 THE GREEN WOLFFIA. All rights reserved.</p>
        <div className="flex gap-4 mt-2 md:mt-0">
          <a href="#" aria-label="Facebook">
            <Facebook />
          </a>
          <a href="#" aria-label="Instagram">
            <Instagram />
          </a>
        </div>
      </footer>
    </main>
  );
}

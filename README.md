# ClownCoin
ClownCoin is the first cryptocurrency powered entirely by pure clown energy. Every transaction comes with a random joke, and the more coins you hold, the bigger your red nose gets (figuratively, of course).
import { useState } from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { motion } from "framer-motion";
import { FaTwitter, FaDiscord } from "react-icons/fa";

export default function ClownCoinWebsite() {
  const [honk, setHonk] = useState(false);

  return (
    <div className="min-h-screen bg-yellow-200 flex flex-col items-center p-6 text-center">
      {/* Hero Section */}
      <motion.div animate={{ rotate: 360 }} transition={{ duration: 4, repeat: Infinity }}>
        <img src="/clowncoin-logo.png" alt="ClownCoin Logo" className="w-32 h-32 mb-4" />
      </motion.div>
      <h1 className="text-4xl font-bold text-red-600">Laughing all the way to the blockchain!</h1>
      <Button className="mt-4 bg-red-500 text-white px-6 py-3 rounded-xl" onClick={() => setHonk(!honk)}>
        Buy $CLOWN {honk && "📢 Honk!"}
      </Button>
      
      {/* Tokenomics Section */}
      <Card className="mt-10 w-full max-w-md bg-white p-6 shadow-lg">
        <CardContent>
          <h2 className="text-2xl font-bold text-blue-600">Tokenomics</h2>
          <p className="text-gray-700 mt-2">💰 1 Trillion Supply | 🔥 1% Burn | 🎭 2% Redistribution</p>
        </CardContent>
      </Card>

      {/* Roadmap Section */}
      <Card className="mt-6 w-full max-w-md bg-white p-6 shadow-lg">
        <CardContent>
          <h2 className="text-2xl font-bold text-green-600">Roadmap</h2>
          <ul className="list-disc text-gray-700 mt-2 text-left">
            <li>Phase 1: Make people laugh</li>
            <li>Phase 2: Get listed on an exchange (probably a sketchy one)</li>
            <li>Phase 3: Buy a circus</li>
          </ul>
        </CardContent>
      </Card>

      {/* Socials */}
      <div className="mt-10 flex space-x-4">
        <a href="#" className="text-blue-500 text-3xl">
          <FaTwitter />
        </a>
        <a href="#" className="text-purple-500 text-3xl">
          <FaDiscord />
        </a>
      </div>

      {/* Footer */}
      <p className="mt-6 text-sm text-gray-600">*We are not responsible if you lose your clown shoes investing in $CLOWN.*</p>
    </div>

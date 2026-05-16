import React from "react";
import { motion } from "framer-motion";
import { ArrowUpRight, Mountain, Compass, Timer, Route, CircleDot } from "lucide-react";

const navItems = ["DROP 001", "SYSTEM", "MANIFESTO"];

const pillars = [
  {
    title: "ENDURANCE",
    eyebrow: "PUSH THROUGH TIME",
    body:
      "Built around sustained effort. Long miles, repeated climbs, early starts, late finishes, and the quiet discipline of continuing when the route stops feeling easy.",
    icon: Timer,
  },
  {
    title: "EXPEDITION",
    eyebrow: "INTO DISTANCE",
    body:
      "A uniform for movement into the unknown. Road, trail, altitude, heat, wind, rain, airport, ridgeline, and every strange place between start and summit.",
    icon: Compass,
  },
  {
    title: "ASCENT",
    eyebrow: "ZERO TO SUMMIT",
    body:
      "The upward line. Physical elevation, mental elevation, and the belief that every serious pursuit begins at zero before it becomes something earned.",
    icon: Mountain,
  },
];

const specs = [
  "Matte technical knit",
  "Run-ready stretch",
  "Lightweight hand-feel",
  "Anti-cotton build philosophy",
  "Minimal reflective language",
  "Expedition-grade restraint",
];

const logoSystem = [
  {
    title: "PRIMARY WORDMARK",
    body: "Clean MILEZERO typography for product tags, website headers, invoices, packaging, and moments where readability matters most.",
  },
  {
    title: "TRACK-ZERO SYMBOL",
    body: "The hero mark. A long vertical route form inspired by track lanes, elevation lines, ascent, movement, and the climb from zero.",
  },
  {
    title: "SLASH MARK",
    body: "The secondary icon system for small scale applications: chest marks, zipper pulls, hardware, app icons, woven labels, and reflective details.",
  },
];

const dropSystem = ["MZ-001 / FOUNDATION", "MZ-002 / ASCENT", "MZ-003 / ALTITUDE", "MZ-004 / EXPEDITION"];

function TrackZeroLogo({ className = "" }) {
  return (
    <div className={`relative flex items-center justify-center ${className}`}>
      <div className="h-full w-full rounded-full border border-white/80" />
      <div className="absolute h-[58%] w-[58%] rounded-full border border-white/45" />
      <div className="absolute h-[1px] w-[72%] bg-white/65" />
      <div className="absolute h-[72%] w-[1px] bg-white/35" />
      <div className="absolute -right-[6%] top-1/2 h-[1px] w-[28%] -translate-y-1/2 bg-white/80" />
    </div>
  );
}

function SmallProductMock() {
  return (
    <div className="relative mx-auto aspect-[4/5] w-full max-w-[430px] overflow-hidden rounded-[2rem] border border-white/10 bg-[#070707] shadow-2xl shadow-black/60">
      <div className="absolute inset-0 bg-[radial-gradient(circle_at_50%_0%,rgba(255,255,255,0.13),transparent_38%),linear-gradient(180deg,rgba(255,255,255,0.04),rgba(255,255,255,0))]" />
      <div className="absolute left-1/2 top-10 -translate-x-1/2 text-[10px] font-medium tracking-[0.52em] text-white/70">
        MILEZERO
      </div>
      <div className="absolute left-8 top-[46%] flex items-center gap-3 text-[9px] tracking-[0.38em] text-white/35 [writing-mode:vertical-rl]">
        MZ-001
      </div>
      <TrackZeroLogo className="absolute left-1/2 top-[38%] h-40 w-72 -translate-x-1/2 opacity-90" />
      <div className="absolute left-1/2 top-[64%] -translate-x-1/2 text-center text-[10px] tracking-[0.42em] text-white/60">
        ENDURANCE / EXPEDITION / ASCENT
      </div>
      <div className="absolute bottom-9 left-9 flex items-center gap-3 text-[10px] tracking-[0.24em] text-white/45">
        <TrackZeroLogo className="h-7 w-7 opacity-60" />
        <span>0M → 8849M</span>
      </div>
      <div className="absolute inset-x-10 bottom-0 h-28 rounded-t-full bg-white/[0.025] blur-2xl" />
    </div>
  );
}

export default function MilezeroLandingPage() {
  return (
    <main className="min-h-screen bg-black text-white selection:bg-white selection:text-black">
      <section className="relative min-h-screen overflow-hidden border-b border-white/10">
        <div className="absolute inset-0 bg-[radial-gradient(circle_at_50%_10%,rgba(255,255,255,0.12),transparent_34%),radial-gradient(circle_at_20%_90%,rgba(255,255,255,0.07),transparent_28%),linear-gradient(180deg,#050505_0%,#000_70%)]" />
        <div className="absolute inset-0 opacity-[0.08] [background-image:linear-gradient(rgba(255,255,255,.6)_1px,transparent_1px),linear-gradient(90deg,rgba(255,255,255,.6)_1px,transparent_1px)] [background-size:72px_72px]" />
        <div className="absolute left-1/2 top-1/2 h-[720px] w-[720px] -translate-x-1/2 -translate-y-1/2 rounded-full border border-white/10" />
        <div className="absolute left-1/2 top-1/2 h-[520px] w-[520px] -translate-x-1/2 -translate-y-1/2 rounded-full border border-white/[0.06]" />

        <header className="relative z-10 flex items-center justify-between px-6 py-6 md:px-12">
          <div className="flex items-center gap-4">
            <TrackZeroLogo className="h-8 w-8" />
            <div className="text-sm font-semibold tracking-[0.42em]">MILEZERO</div>
          </div>
          <nav className="hidden items-center gap-8 text-[10px] tracking-[0.32em] text-white/50 md:flex">
            {navItems.map((item) => (
              <a key={item} href={`#${item.toLowerCase().replace(" ", "-")}`} className="transition hover:text-white">
                {item}
              </a>
            ))}
          </nav>
          <a
            href="#drop-001"
            className="rounded-full border border-white/15 px-4 py-2 text-[10px] tracking-[0.28em] text-white/70 transition hover:border-white/40 hover:text-white"
          >
            MZ-001
          </a>
        </header>

        <div className="relative z-10 mx-auto grid min-h-[calc(100vh-92px)] max-w-7xl grid-cols-1 items-center gap-12 px-6 pb-20 pt-8 md:grid-cols-[1.05fr_.95fr] md:px-12">
          <motion.div
            initial={{ opacity: 0, y: 24 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.9, ease: "easeOut" }}
          >
            <div className="mb-8 flex flex-wrap items-center gap-3 text-[10px] tracking-[0.35em] text-white/45">
              <span className="rounded-full border border-white/10 px-4 py-2">MZ-001</span>
              <span className="rounded-full border border-white/10 px-4 py-2">0M → 8849M</span>
              <span className="rounded-full border border-white/10 px-4 py-2">START FROM ZERO</span>
            </div>

            <h1 className="max-w-4xl text-6xl font-semibold uppercase leading-[0.86] tracking-[-0.08em] md:text-8xl lg:text-[9rem]">
              START
              <br />
              FROM
              <br />
              ZERO
            </h1>

            <p className="mt-8 max-w-xl text-base leading-7 text-white/58 md:text-lg">
              Premium technical running and adventure apparel built for the first meter, the long middle, and the climb toward something higher.
            </p>

            <div className="mt-10 flex flex-col gap-4 sm:flex-row">
              <a
                href="#drop-001"
                className="group flex items-center justify-center gap-3 rounded-full bg-white px-6 py-4 text-xs font-semibold tracking-[0.28em] text-black transition hover:bg-white/80"
              >
                ENTER DROP 001
                <ArrowUpRight className="h-4 w-4 transition group-hover:translate-x-0.5 group-hover:-translate-y-0.5" />
              </a>
              <a
                href="#manifesto"
                className="flex items-center justify-center rounded-full border border-white/15 px-6 py-4 text-xs tracking-[0.28em] text-white/65 transition hover:border-white/40 hover:text-white"
              >
                READ SYSTEM
              </a>
            </div>
          </motion.div>

          <motion.div
            initial={{ opacity: 0, scale: 0.96 }}
            animate={{ opacity: 1, scale: 1 }}
            transition={{ duration: 1.1, ease: "easeOut", delay: 0.15 }}
            className="relative"
          >
            <SmallProductMock />
          </motion.div>
        </div>
      </section>

      <section id="drop-001" className="border-b border-white/10 px-6 py-24 md:px-12">
        <div className="mx-auto grid max-w-7xl gap-12 md:grid-cols-[.8fr_1.2fr]">
          <div>
            <p className="text-[10px] tracking-[0.42em] text-white/40">DROP 001</p>
            <h2 className="mt-5 text-4xl font-semibold uppercase tracking-[-0.06em] md:text-6xl">
              The first uniform.
            </h2>
          </div>
          <div className="grid gap-4 md:grid-cols-2">
            {specs.map((spec, index) => (
              <div key={spec} className="rounded-3xl border border-white/10 bg-white/[0.025] p-6">
                <div className="mb-8 flex items-center justify-between text-[10px] tracking-[0.28em] text-white/35">
                  <span>{String(index + 1).padStart(2, "0")}</span>
                  <CircleDot className="h-4 w-4" />
                </div>
                <p className="text-sm uppercase tracking-[0.24em] text-white/75">{spec}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      <section id="system" className="border-b border-white/10 px-6 py-24 md:px-12">
        <div className="mx-auto max-w-7xl">
          <div className="mb-14 flex flex-col justify-between gap-6 md:flex-row md:items-end">
            <div>
              <p className="text-[10px] tracking-[0.42em] text-white/40">BRAND SYSTEM</p>
              <h2 className="mt-5 max-w-3xl text-4xl font-semibold uppercase tracking-[-0.06em] md:text-6xl">
                Endurance / Expedition / Ascent
              </h2>
            </div>
            <p className="max-w-md text-sm leading-6 text-white/45">
              Three words that define the product, the route, and the person wearing it.
            </p>
          </div>

          <div className="grid gap-5 md:grid-cols-3">
            {pillars.map((pillar) => {
              const Icon = pillar.icon;
              return (
                <div key={pillar.title} className="group rounded-[2rem] border border-white/10 bg-white/[0.025] p-7 transition hover:bg-white/[0.045]">
                  <div className="mb-12 flex items-center justify-between">
                    <Icon className="h-6 w-6 text-white/60" />
                    <span className="text-[10px] tracking-[0.3em] text-white/30">{pillar.eyebrow}</span>
                  </div>
                  <h3 className="text-2xl font-semibold tracking-[-0.04em]">{pillar.title}</h3>
                  <p className="mt-5 text-sm leading-7 text-white/48">{pillar.body}</p>
                </div>
              );
            })}
          </div>
        </div>
      </section>

      <section className="overflow-hidden border-b border-white/10 px-6 py-24 md:px-12">
        <div className="mx-auto grid max-w-7xl gap-10 md:grid-cols-[1.1fr_.9fr] md:items-center">
          <div className="relative rounded-[2rem] border border-white/10 bg-white/[0.025] p-8 md:p-12">
            <div className="absolute right-8 top-8 text-[10px] tracking-[0.35em] text-white/30">MZ-001</div>
            <TrackZeroLogo className="h-36 w-64 opacity-80 md:h-52 md:w-96" />
            <div className="mt-14 grid gap-5 text-[10px] tracking-[0.3em] text-white/45 md:grid-cols-3">
              <span>FRONT / CENTER WORDMARK</span>
              <span>LOWER LEFT TECH MARK</span>
              <span>BACK / HIGH SHOULDER LOGO</span>
            </div>
          </div>
          <div>
            <p className="text-[10px] tracking-[0.42em] text-white/40">VISUAL DIRECTION</p>
            <h2 className="mt-5 text-4xl font-semibold uppercase tracking-[-0.06em] md:text-6xl">
              Quiet from the front. Unmistakable from the back.
            </h2>
            <p className="mt-7 text-base leading-7 text-white/50">
              The front stays nearly silent: a small centered wordmark and a low circular mark. The back carries the identity: an elongated track-zero symbol with technical expedition language below it.
            </p>
          </div>
        </div>
      </section>

      <section id="manifesto" className="px-6 py-28 md:px-12">
        <div className="mx-auto max-w-5xl text-center">
          <Route className="mx-auto mb-8 h-8 w-8 text-white/35" />
          <p className="text-[10px] tracking-[0.42em] text-white/40">0M → 8849M</p>
          <h2 className="mt-8 text-5xl font-semibold uppercase leading-[0.92] tracking-[-0.08em] md:text-8xl">
            Every ascent starts at zero.
          </h2>
          <p className="mx-auto mt-8 max-w-2xl text-base leading-8 text-white/50">
            MILEZERO is for the beginning before the breakthrough. The first run back. The first meter of the climb. The first decision to move toward something that does not feel possible yet.
          </p>
          <div className="mt-14 flex justify-center">
            <a
              href="#drop-001"
              className="rounded-full border border-white/15 px-8 py-4 text-xs tracking-[0.3em] text-white/65 transition hover:border-white/45 hover:text-white"
            >
              START FROM ZERO
            </a>
          </div>
        </div>
      </section>
    </main>
  );
}

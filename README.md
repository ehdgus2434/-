import React, { useState } from "react";
import { motion } from "framer-motion";
import {
  ArrowRight,
  ShieldCheck,
  Home,
  PlusCircle,
  Phone,
  MessageCircle,
  Sparkles,
  Building2,
  Users,
  BriefcaseBusiness,
  CheckCircle2,
  LineChart,
  Handshake,
  HeartHandshake,
  UserRound,
  ClipboardCheck,
  Send,
} from "lucide-react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const businessCategories = [
  {
    title: "더 좋은 라이프 든든본부",
    subtitle: "생활형 라이프케어 · 상조 · 가족 미래 대비",
    description:
      "상조를 위한 상조가 아닌, 미래를 위한 상조. 최신가전, 건강관리, 가족 혜택, 만기환급 구조까지 함께 제안하는 생활형 라이프케어 브랜드입니다.",
    badge: "MAIN BUSINESS",
    icon: ShieldCheck,
    linkText: "라이프케어 상담 신청",
  },
  {
    title: "렌탈맛집",
    subtitle: "가전 · 전자제품 렌탈 비교 및 상담",
    description:
      "고객의 생활환경과 예산에 맞춰 필요한 가전·전자제품 렌탈을 비교하고 제안하는 실속형 생활 렌탈 상담 서비스입니다.",
    badge: "RENTAL SERVICE",
    icon: Home,
    linkText: "렌탈 상담 신청",
  },
];

const valueCards = [
  {
    icon: HeartHandshake,
    title: "Life Planner",
    text: "고객 한 분 한 분의 현재 생활과 미래 준비를 함께 설계합니다.",
  },
  {
    icon: Building2,
    title: "Multi Business Platform",
    text: "상조, 렌탈을 시작으로 삶에 필요한 다양한 영업영역을 확장합니다.",
  },
  {
    icon: Users,
    title: "Sales Partner Growth",
    text: "함께 성장할 영업 파트너가 안정적으로 활동할 수 있는 구조를 만듭니다.",
  },
  {
    icon: LineChart,
    title: "Long-term Value",
    text: "단기 판매가 아닌 신뢰, 소개, 재구매가 이어지는 장기 가치를 지향합니다.",
  },
];

const process = [
  "상담 문의 접수",
  "고객 상황 분석",
  "맞춤 솔루션 제안",
  "가입·계약 진행",
  "사후 관리 및 추가 혜택 안내",
];

const futureCategories = [
  "자동차 제휴 영업",
  "보험/재무 상담",
  "부동산/숙박 사업",
  "기업 제휴 상품",
  "헬스케어 서비스",
  "생활복지 멤버십",
];

export default function TheBetterSalesHomepage() {
  const [formType, setFormType] = useState("상담문의");

  return (
    <div className="min-h-screen bg-white text-slate-950">
      <header className="sticky top-0 z-50 border-b border-slate-200/80 bg-white/90 backdrop-blur-xl">
        <div className="mx-auto flex max-w-7xl items-center justify-between px-5 py-4">
          <div>
            <div className="text-xl font-black tracking-tight text-slate-950">THE BETTER SALES</div>
            <div className="text-xs font-medium text-slate-500">Better Life. Better Sales. Better Future.</div>
          </div>
          <nav className="hidden gap-7 text-sm font-semibold text-slate-600 md:flex">
            <a href="#about" className="hover:text-slate-950">회사소개</a>
            <a href="#business" className="hover:text-slate-950">사업영역</a>
            <a href="#recruit" className="hover:text-slate-950">영업파트너</a>
            <a href="#contact" className="hover:text-slate-950">상담·채용문의</a>
          </nav>
          <a href="#contact">
            <Button className="rounded-full bg-slate-950 px-5 hover:bg-slate-800">문의하기</Button>
          </a>
        </div>
      </header>

      <section className="relative overflow-hidden bg-slate-950 px-5 py-20 text-white md:py-28">
        <div className="absolute inset-0 bg-[radial-gradient(circle_at_top_right,rgba(245,158,11,0.22),transparent_34%),radial-gradient(circle_at_bottom_left,rgba(59,130,246,0.20),transparent_32%)]" />
        <div className="absolute inset-x-0 bottom-0 h-28 bg-gradient-to-t from-white to-transparent" />
        <div className="relative mx-auto grid max-w-7xl gap-12 md:grid-cols-[1.1fr_0.9fr] md:items-center">
          <motion.div initial={{ opacity: 0, y: 18 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.7 }}>
            <div className="mb-6 inline-flex items-center gap-2 rounded-full border border-amber-300/30 bg-amber-300/10 px-4 py-2 text-sm font-semibold text-amber-200">
              <Sparkles size={16} /> 공식 라이프 세일즈 플랫폼
            </div>
            <h1 className="text-4xl font-black leading-tight tracking-tight md:text-6xl">
              지금까지의 영업과 다른<br />
              <span className="text-amber-300">라이프 플래너 그룹</span>
            </h1>
            <p className="mt-6 max-w-2xl text-lg leading-8 text-slate-300">
              THE BETTER SALES는 고객의 삶에 필요한 영업영역을 연결하고, 한 분 한 분의 현재와 미래를 함께 설계하는 생활형 세일즈 플랫폼입니다.
            </p>
            <div className="mt-8 flex flex-col gap-3 sm:flex-row">
              <a href="#contact">
                <Button size="lg" className="rounded-full bg-amber-300 px-7 font-bold text-slate-950 hover:bg-amber-200">
                  상담 문의 남기기 <ArrowRight className="ml-2" size={18} />
                </Button>
              </a>
              <a href="#recruit">
                <Button size="lg" variant="outline" className="rounded-full border-white/25 bg-white/5 px-7 text-white hover:bg-white/10">
                  영업사원 신청하기
                </Button>
              </a>
            </div>
            <div className="mt-10 grid max-w-2xl grid-cols-3 gap-3 text-center">
              <div className="rounded-3xl border border-white/10 bg-white/10 p-4">
                <div className="text-2xl font-black">01</div>
                <div className="mt-1 text-xs text-slate-300">라이프케어</div>
              </div>
              <div className="rounded-3xl border border-white/10 bg-white/10 p-4">
                <div className="text-2xl font-black">02</div>
                <div className="mt-1 text-xs text-slate-300">렌탈 솔루션</div>
              </div>
              <div className="rounded-3xl border border-white/10 bg-white/10 p-4">
                <div className="text-2xl font-black">∞</div>
                <div className="mt-1 text-xs text-slate-300">영역 확장</div>
              </div>
            </div>
          </motion.div>

          <motion.div initial={{ opacity: 0, scale: 0.96 }} animate={{ opacity: 1, scale: 1 }} transition={{ duration: 0.7, delay: 0.15 }}>
            <Card className="rounded-[2.2rem] border-white/10 bg-white/10 shadow-2xl backdrop-blur-xl">
              <CardContent className="p-7 md:p-9">
                <div className="mx-auto flex h-32 w-32 items-center justify-center rounded-full border-4 border-amber-300/30 bg-slate-900 text-center text-xs font-semibold text-slate-400">
                  대표 프로필<br />사진 영역
                </div>
                <div className="mt-6 text-center text-sm font-bold text-amber-200">CEO MESSAGE</div>
                <div className="mt-3 text-center text-2xl font-black leading-snug text-white">
                  한 분 한 분의 삶에<br />든든한 플래너가 되겠습니다.
                </div>
                <p className="mt-5 leading-8 text-slate-300">
                  저희는 단순히 상품을 판매하지 않습니다. 고객에게 필요한 생활, 가족, 미래 대비 영역을 함께 고민하고 가장 현실적인 선택을 제안합니다. THE BETTER SALES는 신뢰를 기반으로 오래 함께하는 라이프 파트너가 되겠습니다.
                </p>
                <div className="mt-6 rounded-3xl bg-white/10 p-5 text-sm leading-7 text-slate-300">
                  “상조를 위한 상조가 아닌, 미래를 위한 상조. 더 좋은 라이프 든든본부에서 든든한 라이프 플래너가 되어 드리겠습니다.”
                </div>
              </CardContent>
            </Card>
          </motion.div>
        </div>
      </section>

      <section id="about" className="px-5 py-20">
        <div className="mx-auto max-w-7xl">
          <div className="grid gap-10 md:grid-cols-[0.9fr_1.1fr] md:items-end">
            <div>
              <div className="text-sm font-black tracking-widest text-amber-600">ABOUT THE BETTER SALES</div>
              <h2 className="mt-3 text-3xl font-black leading-tight md:text-5xl">
                고객의 인생에 필요한<br />영업을 설계합니다.
              </h2>
            </div>
            <p className="text-lg leading-9 text-slate-600">
              THE BETTER SALES는 상조, 렌탈, 생활복지, 미래 대비 등 삶에 필요한 영역을 하나의 플랫폼으로 연결합니다. 우리는 고객에게는 더 나은 선택을, 영업 파트너에게는 더 나은 성장의 기회를 제공합니다.
            </p>
          </div>

          <div className="mt-12 grid gap-5 md:grid-cols-4">
            {valueCards.map((item) => {
              const Icon = item.icon;
              return (
                <Card key={item.title} className="rounded-[2rem] border-slate-200 shadow-sm transition hover:-translate-y-1 hover:shadow-xl">
                  <CardContent className="p-7">
                    <div className="mb-6 flex h-12 w-12 items-center justify-center rounded-2xl bg-slate-950 text-amber-300">
                      <Icon size={24} />
                    </div>
                    <h3 className="text-lg font-black">{item.title}</h3>
                    <p className="mt-3 leading-7 text-slate-600">{item.text}</p>
                  </CardContent>
                </Card>
              );
            })}
          </div>
        </div>
      </section>

      <section id="business" className="bg-slate-50 px-5 py-20">
        <div className="mx-auto max-w-7xl">
          <div className="mb-12 flex flex-col justify-between gap-4 md:flex-row md:items-end">
            <div>
              <div className="text-sm font-black tracking-widest text-amber-600">BUSINESS AREA</div>
              <h2 className="mt-3 text-3xl font-black md:text-5xl">메인 사업영역</h2>
              <p className="mt-4 max-w-2xl leading-8 text-slate-600">
                현재는 더 좋은 라이프 든든본부와 렌탈맛집을 중심으로 운영하며, 향후 새로운 영업 카테고리를 지속적으로 추가할 수 있는 확장형 구조입니다.
              </p>
            </div>
          </div>

          <div className="grid gap-6 md:grid-cols-2">
            {businessCategories.map((item) => {
              const Icon = item.icon;
              return (
                <Card key={item.title} className="group rounded-[2rem] border-slate-200 bg-white shadow-sm transition hover:-translate-y-1 hover:shadow-2xl">
                  <CardContent className="p-8">
                    <div className="flex items-start justify-between gap-4">
                      <div className="rounded-2xl bg-slate-950 p-4 text-amber-300">
                        <Icon size={30} />
                      </div>
                      <span className="rounded-full border border-slate-200 px-3 py-1 text-xs font-bold text-slate-500">{item.badge}</span>
                    </div>
                    <h3 className="mt-8 text-2xl font-black">{item.title}</h3>
                    <p className="mt-2 text-sm font-bold text-amber-700">{item.subtitle}</p>
                    <p className="mt-5 min-h-28 leading-8 text-slate-600">{item.description}</p>
                    <a href="#contact">
                      <Button className="mt-6 rounded-full bg-slate-950 px-6 hover:bg-slate-800">
                        {item.linkText} <ArrowRight className="ml-2" size={17} />
                      </Button>
                    </a>
                  </CardContent>
                </Card>
              );
            })}
          </div>
        </div>
      </section>

      <section className="px-5 py-20">
        <div className="mx-auto max-w-7xl rounded-[2.5rem] bg-slate-950 p-8 text-white md:p-14">
          <div className="grid gap-10 md:grid-cols-[0.9fr_1.1fr] md:items-center">
            <div>
              <div className="text-sm font-black tracking-widest text-amber-300">CUSTOMER PROCESS</div>
              <h2 className="mt-3 text-3xl font-black leading-tight md:text-5xl">
                상담부터 사후관리까지<br />체계적으로 진행합니다.
              </h2>
              <p className="mt-5 leading-8 text-slate-300">
                고객이 불안하지 않도록 처음 문의부터 가입, 계약, 사후 안내까지 명확한 프로세스로 관리합니다.
              </p>
            </div>
            <div className="grid gap-3">
              {process.map((step, index) => (
                <div key={step} className="flex items-center gap-4 rounded-3xl bg-white/10 p-5">
                  <div className="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-amber-300 font-black text-slate-950">{index + 1}</div>
                  <div className="font-bold">{step}</div>
                </div>
              ))}
            </div>
          </div>
        </div>
      </section>

      <section id="recruit" className="bg-slate-50 px-5 py-20">
        <div className="mx-auto max-w-7xl">
          <div className="grid gap-10 md:grid-cols-[1fr_1fr] md:items-center">
            <div>
              <div className="text-sm font-black tracking-widest text-amber-600">SALES PARTNER</div>
              <h2 className="mt-3 text-3xl font-black leading-tight md:text-5xl">
                함께 성장할<br />영업 파트너를 기다립니다.
              </h2>
              <p className="mt-5 leading-8 text-slate-600">
                THE BETTER SALES는 영업을 단순한 판매가 아닌, 고객의 삶을 설계하는 전문 영역으로 봅니다. 고객에게 필요한 솔루션을 제안하고, 함께 성장할 분을 찾습니다.
              </p>
              <div className="mt-7 grid gap-3">
                {[
                  "초보자도 이해할 수 있는 사업 구조 안내",
                  "상담·가입·계약 프로세스 교육",
                  "더 좋은 라이프 든든본부 중심의 생활형 라이프케어 영업",
                  "향후 다양한 영업 카테고리 확장 기회",
                ].map((item) => (
                  <div key={item} className="flex items-center gap-3 text-slate-700">
                    <CheckCircle2 className="text-amber-600" size={20} />
                    <span>{item}</span>
                  </div>
                ))}
              </div>
              <a href="#contact">
                <Button size="lg" className="mt-8 rounded-full bg-slate-950 px-7 hover:bg-slate-800">
                  영업사원 신청하기 <ArrowRight className="ml-2" size={18} />
                </Button>
              </a>
            </div>

            <Card className="rounded-[2.2rem] border-slate-200 bg-white shadow-xl">
              <CardContent className="p-8">
                <div className="mb-6 flex h-14 w-14 items-center justify-center rounded-2xl bg-slate-950 text-amber-300">
                  <BriefcaseBusiness size={28} />
                </div>
                <h3 className="text-2xl font-black">앞으로 추가될 영업영역</h3>
                <p className="mt-3 leading-7 text-slate-600">
                  하나의 회사 안에서 다양한 영업 카테고리를 확장할 수 있도록 설계된 구조입니다.
                </p>
                <div className="mt-6 grid gap-3 sm:grid-cols-2">
                  {futureCategories.map((category) => (
                    <div key={category} className="flex items-center gap-3 rounded-2xl bg-slate-50 p-4 text-sm font-semibold text-slate-700">
                      <PlusCircle className="text-amber-600" size={19} />
                      {category}
                    </div>
                  ))}
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      <section id="contact" className="px-5 py-20">
        <div className="mx-auto max-w-7xl">
          <div className="grid gap-10 md:grid-cols-[0.9fr_1.1fr] md:items-start">
            <div>
              <div className="text-sm font-black tracking-widest text-amber-600">CONTACT & DB FORM</div>
              <h2 className="mt-3 text-3xl font-black leading-tight md:text-5xl">
                상담문의와 채용문의를<br />한 곳에서 접수합니다.
              </h2>
              <p className="mt-5 leading-8 text-slate-600">
                더 좋은 라이프 든든본부 가입 상담, 렌탈 상담, 영업사원 신청, 제휴 문의까지 목적에 맞게 정보를 남길 수 있습니다.
              </p>
              <div className="mt-8 grid gap-4 sm:grid-cols-2">
                <div className="rounded-3xl border border-slate-200 p-5">
                  <Phone className="text-amber-600" />
                  <div className="mt-3 font-black">전화 상담</div>
                  <div className="mt-1 text-sm text-slate-500">빠른 상담 연결 영역</div>
                </div>
                <div className="rounded-3xl border border-slate-200 p-5">
                  <MessageCircle className="text-amber-600" />
                  <div className="mt-3 font-black">카카오 상담</div>
                  <div className="mt-1 text-sm text-slate-500">카카오 채널 연결 영역</div>
                </div>
              </div>
            </div>

            <Card className="rounded-[2.2rem] border-slate-200 shadow-2xl">
              <CardContent className="p-7 md:p-8">
                <div className="mb-6 flex items-center gap-3">
                  <div className="flex h-12 w-12 items-center justify-center rounded-2xl bg-slate-950 text-amber-300">
                    <ClipboardCheck size={24} />
                  </div>
                  <div>
                    <h3 className="text-2xl font-black">문의 정보 남기기</h3>
                    <p className="text-sm text-slate-500">아래 양식은 실제 홈페이지에서 DB 수집 폼으로 연결됩니다.</p>
                  </div>
                </div>

                <div className="mb-5 grid grid-cols-2 gap-2 md:grid-cols-4">
                  {["상담문의", "채용문의", "영업사원 신청", "제휴문의"].map((type) => (
                    <button
                      key={type}
                      onClick={() => setFormType(type)}
                      className={`rounded-2xl px-3 py-3 text-sm font-bold transition ${formType === type ? "bg-slate-950 text-white" : "bg-slate-100 text-slate-600 hover:bg-slate-200"}`}
                    >
                      {type}
                    </button>
                  ))}
                </div>

                <div className="grid gap-4">
                  <div className="grid gap-4 md:grid-cols-2">
                    <input className="rounded-2xl border border-slate-200 px-4 py-4 outline-none focus:border-slate-950" placeholder="성함" />
                    <input className="rounded-2xl border border-slate-200 px-4 py-4 outline-none focus:border-slate-950" placeholder="연락처" />
                  </div>
                  <div className="grid gap-4 md:grid-cols-2">
                    <input className="rounded-2xl border border-slate-200 px-4 py-4 outline-none focus:border-slate-950" placeholder="거주지역" />
                    <select className="rounded-2xl border border-slate-200 px-4 py-4 outline-none focus:border-slate-950" value={formType} onChange={(e) => setFormType(e.target.value)}>
                      <option>상담문의</option>
                      <option>채용문의</option>
                      <option>영업사원 신청</option>
                      <option>제휴문의</option>
                    </select>
                  </div>
                  <textarea className="min-h-32 rounded-2xl border border-slate-200 px-4 py-4 outline-none focus:border-slate-950" placeholder="문의 내용을 남겨주세요." />
                  <label className="flex items-start gap-3 text-sm text-slate-500">
                    <input type="checkbox" className="mt-1" />
                    개인정보 수집 및 상담 연락에 동의합니다.
                  </label>
                  <Button size="lg" className="rounded-full bg-slate-950 py-6 text-base font-bold hover:bg-slate-800">
                    DB 문의 접수하기 <Send className="ml-2" size={18} />
                  </Button>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      <footer className="border-t border-slate-200 bg-slate-950 px-5 py-10 text-white">
        <div className="mx-auto flex max-w-7xl flex-col justify-between gap-5 md:flex-row md:items-center">
          <div>
            <div className="text-xl font-black">THE BETTER SALES</div>
            <div className="mt-2 text-sm text-slate-400">Better Life. Better Sales. Better Future.</div>
          </div>
          <div className="text-sm leading-7 text-slate-400 md:text-right">
            더 좋은 라이프 든든본부 · 렌탈맛집 · 영업 파트너 플랫폼<br />
            © THE BETTER SALES. All rights reserved.
          </div>
        </div>
      </footer>
    </div>
  );
}

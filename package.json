"use client";

import { useState } from "react";

export default function LoginPage() {
  const [role, setRole] = useState("");
  const [branch, setBranch] = useState("");

  const handleLogin = () => {
    console.log("Logging in...", { role, branch });
    // In a real app, this would use Supabase Auth and redirect to the appropriate portal
    alert(`Logged in as ${role} ${branch}`);
  };

  return (
    <div className="flex h-screen w-screen flex-col items-center justify-center bg-[var(--bg)] p-4">
      <div className="w-full max-w-[420px] rounded-[var(--r-xl)] border border-[var(--border)] bg-[var(--bg2)] p-9 shadow-2xl">
        <div className="mb-7 flex items-center justify-center gap-3">
          <div className="flex h-10 w-10 items-center justify-center rounded-[10px] bg-[var(--accent)] text-lg">
            🍽
          </div>
          <div className="text-[22px] font-semibold tracking-tight">
            Rest<span className="text-[var(--accent)]">OS</span>
          </div>
        </div>

        <h2 className="mb-1 text-center text-lg font-semibold">Sign in to your portal</h2>
        <p className="mb-6 text-center text-[13px] text-[var(--text2)]">
          Select your role and enter your password
        </p>

        <div className="mb-3">
          <label className="mb-1.5 block text-[10px] font-bold uppercase tracking-wider text-[var(--text2)]">
            Role
          </label>
          <select
            className="w-full rounded-[var(--r)] border border-[var(--border2)] bg-[var(--bg)] px-3 py-2 text-[13px] text-[var(--text)] outline-none transition-colors focus:border-[var(--accent)]"
            value={role}
            onChange={(e) => setRole(e.target.value)}
          >
            <option value="">— Select your role —</option>
            <option value="admin">🏢 Admin</option>
            <option value="ops">⚙️ Operations</option>
            <option value="foh">🪑 Front of House (FOH)</option>
            <option value="boh">🔥 Back of House (BOH)</option>
            <option value="warehouse">🏭 Warehouse</option>
            <option value="procurement">🛒 Procurement</option>
          </select>
        </div>

        {(role === "foh" || role === "boh") && (
          <div className="mb-3">
            <label className="mb-1.5 block text-[10px] font-bold uppercase tracking-wider text-[var(--text2)]">
              Branch
            </label>
            <select
              className="w-full rounded-[var(--r)] border border-[var(--border2)] bg-[var(--bg)] px-3 py-2 text-[13px] text-[var(--text)] outline-none transition-colors focus:border-[var(--accent)]"
              value={branch}
              onChange={(e) => setBranch(e.target.value)}
            >
              <option value="Karachi E Street">📍 Karachi — E Street</option>
              <option value="Lahore">📍 Lahore</option>
              <option value="Islamabad F6">📍 Islamabad — F6</option>
            </select>
          </div>
        )}

        <div className="mb-4">
          <label className="mb-1.5 block text-[10px] font-bold uppercase tracking-wider text-[var(--text2)]">
            Password
          </label>
          <input
            type="password"
            className="w-full rounded-[var(--r)] border border-[var(--border2)] bg-[var(--bg)] px-3 py-2 text-[13px] text-[var(--text)] outline-none transition-colors focus:border-[var(--accent)]"
            placeholder="Enter password"
          />
        </div>

        <button
          onClick={handleLogin}
          className="mt-1 w-full rounded-[var(--r)] bg-[var(--accent)] p-[11px] text-sm font-semibold text-white transition-colors hover:bg-[var(--accent-l)]"
        >
          Sign In →
        </button>

        <div className="mt-5 border-t border-[var(--border)] pt-4">
          <h3 className="mb-2.5 text-center text-[11px] font-bold uppercase tracking-wider text-[var(--text3)]">
            Quick Demo Access
          </h3>
          <div className="grid grid-cols-2 gap-1.5">
            {[
              { id: "admin", label: "Admin", sub: "admin / admin123" },
              { id: "ops", label: "Operations", sub: "ops / ops123" },
              { id: "wh", label: "Warehouse", sub: "wh / wh123" },
              { id: "proc", label: "Procurement", sub: "proc / proc123" },
              { id: "foh-khi", label: "FOH Karachi", sub: "foh123" },
              { id: "boh-lhe", label: "BOH Lahore", sub: "boh123" },
            ].map((demo) => (
              <div
                key={demo.id}
                className="cursor-pointer rounded-[var(--r)] border border-[var(--border)] bg-[var(--bg3)] px-2.5 py-[7px] text-center transition-colors hover:border-[var(--border2)] hover:bg-[var(--bg4)]"
              >
                <span className="block text-[11px] font-medium">{demo.label}</span>
                <span className="block text-[10px] text-[var(--text3)]">{demo.sub}</span>
              </div>
            ))}
          </div>
        </div>
      </div>
    </div>
  );
}

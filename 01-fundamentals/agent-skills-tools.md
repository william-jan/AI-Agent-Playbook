# Agent, Skill, Tool, dan MCP

**Agent** = model AI ditambah loop kerja dan akses tools. **LLM** merencanakan dan menafsirkan, tetapi tetap bisa salah.

**Tool** = fungsi eksekusi yang benar-benar tersedia (terminal, browser, generator gambar, GitHub API). **Agent Skill** = folder berisi instruksi kerja, biasanya `SKILL.md`, resources, dan scripts. **MCP** = protokol untuk menyambungkan tools/data ke agent, bukan sinonim skill.

## Skill AI vs skill manusia

Skill manusia dipelajari lewat latihan. Agent Skill mengemas prosedur yang dapat dibaca dan digunakan ulang. Menulis skill "professional artist" tidak melatih model menjadi pelukis atau otomatis menyediakan model gambar.

## Contoh: repair sprite

1. User meminta perbaikan tangan, sambil mengunci warna/kostum.
2. Agent membaca skill dan menentukan alur edit.
3. Jika tersedia, tool `image_gen` melakukan editing.
4. Agent memeriksa hasil visual, dimensi dan alpha.

Tanpa tool gambar, file `SKILL.md` sendiri tidak mampu menghasilkan ilustrasi AI.

## Anti-halusinasi

Skill membantu standardisasi dan checklist, **bukan jaminan tidak halusinasi**. Pakai pemeriksaan deterministik seperti lint, test, validasi file, dan screenshot saat memungkinkan.

Referensi: https://agentskills.io/ · https://github.com/openai/skills

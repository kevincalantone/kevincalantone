import { Github } from "lucide-react";

/**
 * GitHub Stats Section - Minimalismo Técnico Moderno
 * Exibe estatísticas do GitHub
 */
export default function GitHubStatsSection() {
  return (
    <section id="github" className="py-20 relative">
      <div className="container">
        <div className="mb-12">
          <div className="tech-accent-line mb-4" />
          <h2 className="tech-section-title">
            <Github className="text-accent" size={32} />
            <span>Atividade no GitHub</span>
          </h2>
          <p className="text-muted-foreground text-lg">
            Acompanhe meus projetos e contribuições
          </p>
        </div>

        {/* Stats Grid */}
        <div className="grid md:grid-cols-3 gap-6 mb-12">
          <div className="tech-card">
            <div className="text-center">
              <div className="text-5xl font-bold text-accent mb-2">50+</div>
              <p className="text-muted-foreground font-medium">Repositórios</p>
            </div>
          </div>

          <div className="tech-card">
            <div className="text-center">
              <div className="text-5xl font-bold text-accent mb-2">200+</div>
              <p className="text-muted-foreground font-medium">Commits</p>
            </div>
          </div>

          <div className="tech-card">
            <div className="text-center">
              <div className="text-5xl font-bold text-accent mb-2">15+</div>
              <p className="text-muted-foreground font-medium">Projetos Públicos</p>
            </div>
          </div>
        </div>

        {/* GitHub Link */}
        <div className="tech-card text-center">
          <p className="text-muted-foreground mb-4">
            Confira meus projetos e contribuições no GitHub
          </p>
          <a
            href="https://github.com/kevincalantone"
            target="_blank"
            rel="noopener noreferrer"
            className="tech-button bg-accent text-accent-foreground hover:bg-blue-700 inline-flex items-center justify-center gap-2"
          >
            <Github size={20} />
            Visitar GitHub
          </a>
        </div>

        {/* Estatísticas Visuais */}
        <div className="mt-12 grid md:grid-cols-2 gap-6">
          <div className="tech-card">
            <h3 className="text-lg font-semibold mb-4 text-foreground">
              Linguagens Mais Usadas
            </h3>
            <div className="space-y-3">
              {[
                { name: "Python", percentage: 35 },
                { name: "JavaScript", percentage: 25 },
                { name: "Java", percentage: 20 },
                { name: "SQL", percentage: 15 },
                { name: "Outros", percentage: 5 },
              ].map((lang, index) => (
                <div key={index}>
                  <div className="flex justify-between mb-1">
                    <span className="text-sm font-medium text-foreground">
                      {lang.name}
                    </span>
                    <span className="text-sm text-accent">{lang.percentage}%</span>
                  </div>
                  <div className="w-full bg-background rounded-full h-2 border border-border overflow-hidden">
                    <div
                      className="bg-accent rounded-full h-full"
                      style={{ width: `${lang.percentage}%` }}
                    />
                  </div>
                </div>
              ))}
            </div>
          </div>

          <div className="tech-card">
            <h3 className="text-lg font-semibold mb-4 text-foreground">
              Contribuições
            </h3>
            <div className="space-y-3">
              {[
                { label: "Commits este mês", value: "24" },
                { label: "Pull Requests", value: "8" },
                { label: "Issues Resolvidas", value: "12" },
                { label: "Dias Consecutivos", value: "15" },
              ].map((item, index) => (
                <div key={index} className="flex justify-between items-center">
                  <span className="text-foreground">{item.label}</span>
                  <span className="text-accent font-bold text-lg">{item.value}</span>
                </div>
              ))}
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}

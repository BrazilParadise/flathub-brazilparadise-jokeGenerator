Checklist de validação antes do merge

1) App ID
- Certifique-se que todos os arquivos apontam para com.diboua.jokeGenerator (ou outro app-id consistente).

2) Ícones
- Confirme que icon.png está presente no caminho referenciado nos manifests.
- Verifique as cópias icon-128.png, icon-256.png, icon-512.png e icon-transparent.png.

3) Build local
- Execute flatpak-builder localmente para validar o manifesto.

Comandos úteis
- flatpak-builder --force-clean --install-deps-from=flathub build-dir com.diboua.jokeGenerator.yaml
- flatpak-builder --run build-dir com.diboua.jokeGenerator.yaml /app/bin/run.sh

Notas
- Se houver erros de metainfo (appstream), use appstream-util validate (ou ferramentas equivalentes).

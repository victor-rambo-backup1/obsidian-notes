1. Corrigir o setId()

Bug confirmado

BoxBuilder · 2 min

Você recebe idName, mas sempre executa box.setId("main"). Esse é um bug confirmado.

2. Sincronizar seleção de música e player

ALTA

PlayerScreen · 20–40 min

Não avançar ou retroceder a seleção se player.load() falhar ou o caminho for null. Verificar também se selectNext() dispara outro carregamento.

3. Garantir salvamento atômico dos mapeamentos

ALTA

MapperScreen / MappingWidget · 40–90 min

Se saveChange() aplica alterações imediatamente, uma exceção pode deixar algumas regras novas e outras antigas. Coletar, validar tudo e só então aplicar.

4. Remover dependência de contador global de vozes

ALTA

CompositionScreen / VoiceWidget · 30–60 min

Se o contador é estático, a numeração e a escolha dos presets ficam dependentes da ordem de construção e remoção dos widgets. Preferir índices gerenciados pela tela.

5. Verificar os dois onClick() do botão de remover

ALTA

ButtonBuilder / CompositionScreen · 10–20 min

Confirmar se o segundo callback substitui o primeiro. Garantir que o contador só seja atualizado quando uma voz for realmente removida.

6. Tratar a ausência de arquivos MIDI na inicialização

ALTA

PlayerScreen · 20–40 min

getFirst() falha em uma lista vazia. Definir o que a interface apresenta quando não há músicas disponíveis e tratar arquivos inválidos.

7. Centralizar o encerramento dos recursos

MÉDIA

ScreenManager / PlayerScreen · 20–40 min

Usar Application.stop() para encerrar o player e liberar timers e animações. Evitar que a tela seja responsável por fechar a aplicação.

8. Sincronizar o botão de reprodução

MÉDIA

PlayerScreen / MusicPlayButtonWidget · 20–45 min

Quando a música terminar ou a reprodução mudar externamente, o ícone deve refletir o estado real do player.

9. Definir a semântica de Restaurar ao Padrão

MÉDIA

MapperScreen · 15–30 min

Decidir se restaura imediatamente as regras ou apenas os campos até clicar em Salvar. Deixar esse comportamento consistente.

10. Centralizar a adição e remoção de vozes

MÉDIA

CompositionScreen · 20–40 min

Usar os mesmos métodos para ações dos botões e operações de importação, incluindo limites de 1 e 15 vozes.

11. Validar a normalização da entrada musical

MÉDIA

CompositionScreen · 20–40 min

replace("\n", "") pode juntar tokens. Confirmar o comportamento esperado na gramática e testar entradas multilinha, vazias e inválidas.

12. Unificar a inicialização dos controles

MÉDIA

PlayerScreen · 15–30 min

Usar a música carregada no Player como fonte de verdade para título, seleção, duração e partitura, inclusive no construtor.

13. Evitar identificadores frágeis em strings

MÉDIA

MapperScreen / TextToMusicRules · 20–40 min

Considerar enum ou constantes para note, pause, octaveUp etc. quando os mesmos identificadores aparecerem em várias classes.

14. Aplicar CSS antes de mostrar a janela

ScreenManager · 5 min

Fazer createScene() apenas construir a Scene. Adicionar os estilos e então chamar stage.show().

15. Separar a criação dos containers do reset das regras

MapperScreen · 15–30 min

Evitar que restoreMappingContainers() faça três coisas: redefinir regras, reconstruir widgets e mudar a categoria visível.

16. Tornar as referências dos botões final

MusicPlayButtonWidget · 5 min

São inicializadas uma única vez. Avaliar se há vantagem real em manter dois botões; não é obrigatório mudar para um.

17. Corrigir nomes e pequenos detalhes

MapperScreen · 10 min

Trocar assingMappingWidgetToContainer por assignMappingWidgetToContainer, renomear variáveis confusas e corrigir comentários.
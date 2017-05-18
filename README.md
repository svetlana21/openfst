# openfst
Эксперименты с openfst

openfst/from openfst.org/ - quick tour с сайта openfst:

text.fst - первый пробный текстовый FST, isyms.txt и osyms.txt - файлы, задающие интерпретацию входных и выходных символов в виде натуральных чисел (во внутреннем представлении openfst все символы заменяются целыми числами; чтобы после операций с автоматом на выходе был автомат с понятными нам символами, эту замену следует задать эксплицитно).

binary.fst - скомпилированный text.fst (бинарный файл).

binary.dot - отрисованный binary.fst в формате Graphviz dot, binary.ps - рисунок binary.fst, который можно открыть и посмотреть.

Эксперименты с объединением автоматов:

input.fst, isyms_inp.txt, osyms_inp.txt - первый автомат, model.fst, isyms_mod.txt, osyms_mod.txt - второй.

Для объединения хотя бы один автомат должен быть отсортирован. 

model_sorted.fst - отсортированный model.fst.

comp.fst - объединённый автомат, comp.ps - его рисунок.

result.fst - тот же автомат comp.fst, но сохранены только выходные символы. result.png - рисунок.

openfst/from OpenFST_Tutorial.pdf/ :

lower.txtfst - текстовый FST. abc.syms описывает интерпретацию и входных, и выходных символов.

lower.fst - скомпилированный lower.txtfst.
 
lower.dot, lower.png - рисунок lower.fst.

lower.info - файл с информацией о lower.fst.

lower.info.txtfst - напечатанный в текстовом виде lower.fst.

Слово, подаваемое автомату на вход, должно быть представлено в виде простого "автомата-цепочки". Затем его нужно объединить с автоматом (compose).

input.txtfst - слово-инпут (автомат в текстовом виде). input.fst - он же скомпилированный, input.png - рисунок.

lower.output.fst - результат после того, как автомату было скормлено слово input.fst. Результат с ошибкой! В lower.txtfst не хватает строк 

0 0 <space> <space>

0 0 <newline> <newline>

lower2.txtfst - строки добавлены. lower2.fst - скомпилированный.

lower2.output.fst - верный результат. lower2.output.txtfst - получившийся автомат в текстовом виде,	lower2.output.png - рисунок.

osyms.txt - по-видимому создан для тренировки, в тьюториале нигде не используется.

openfst/from_my_notebook/ - эксперименты с минимизацией и детерминизацией по задачам с курса "Матмодели языка":

Задача: детерминировать следующий НКА: my.png.

my.fst - FST, скомпилированный из my.txt и mysyms.txt. my.png - рисунок.

my_det.fst - результат детерминизации. my_det.png - рисунок.

Задача: минимизировать следующий НКА:  	my_min.png.

my_min.fst - FST, скомпилированный из my_min.txt и mysyms.txt. my_min.png - рисунок.

my_min_det.fst - детерминированный my_min.fst. my_min.png - рисунок.

minimized.fst - решение, минимизированнй my_min.fst. minimized.png - рисунок.

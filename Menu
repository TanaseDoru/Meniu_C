#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

int main()
{
	FILE* pFile;

	pFile = fopen("Menu.cpp", "w");
	if (pFile == NULL)
	{
		printf("Eroare: deschide fisier");
		return 1;
	}
	
	fprintf(pFile, "#define _CRT_SECURE_NO_WARNINGS\n#include <stdio.h>\n\n");
	printf("n = ");
	int n;
	scanf("%d", &n);
	for (int i = 0; i < n; i++)
	{
		fprintf(pFile, "void Ex%d();\n", i + 1);
	}
	fprintf(pFile, "\n");
	fprintf(pFile, "int main()\n{\n");
	fprintf(pFile, "int opt;\n");
	fprintf(pFile, "do {\nprintf(\"Optiune: \");\nscanf(\"%%\d\", &opt);\nswitch (opt){\n");
	for (int i = 0; i < n; i++)
	{
		fprintf(pFile, "case %d: Ex%d(); break;\n", i + 1, i + 1);
	}
	fprintf(pFile, "}\nprintf(\"\\n********************************************\\n\\n\\n\");");
	fprintf(pFile, "\n}while(opt != 0);\nreturn 0;\n}\n\n");
	for (int i = 0; i < n; i++)
	{
		fprintf(pFile, "void Ex%d()\n", i + 1);
		fprintf(pFile, "{\n\n}\n\n");
	}
	return 0;
}

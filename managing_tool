#include<stdio.h>
#include<stdlib.h>
#include<string.h>

struct students{
    char name[20];
    int phy_marks;
    int chem_marks;
    int maths_marks;
    int bio_marks;
};

void clearInputBuffer() {
    int c;
    while ((c = getchar()) != '\n' && c != EOF) { }
}

void stripNewline(char *str) {
    size_t len = strlen(str);
    if (len > 0 && str[len-1] == '\n') {
        str[len-1] = '\0';
    }
}

void gradesys(float avg){
    if(avg>90 && avg<=100){
        printf("Student got grade 'O'\n");
    }
    else if(avg>80 && avg<=90){
        printf("Student got grade 'A'\n");
    }
    else if(avg>70 && avg<=80){
        printf("Student got grade 'B'\n");
    }
    else if(avg>60 && avg<=70){
        printf("Student got grade 'C'\n");
    }
    else if(avg>50 && avg<=60){
        printf("Student got grade 'D'\n");
    }
    else if(avg>40 && avg<=50){
        printf("Student got grade 'E'\n");
    }
    else{
        printf("Student failed in the exam\n");
    }
}


int main(){
    printf("Welcome to the STUDENT GRADE MANAGEMENT system\n\n"); 
    int num;
    printf("Enter the number of students:");
    scanf("%d",&num);
    clearInputBuffer();
    struct students array[num];
    for(int i=0;i<num;i++){
        printf("Enter the name of student %d:",i+1);
        fgets(array[i].name,sizeof(array[i].name),stdin);
        stripNewline(array[i].name);
        printf("Enter the Physics marks:");
        scanf("%d",&array[i].phy_marks);
        printf("Enter the Chemistry marks:");
        scanf("%d",&array[i].chem_marks);
        printf("Enter the Math marks:");
        scanf("%d",&array[i].maths_marks);
        printf("Enter the Biology marks:");
        scanf("%d",&array[i].bio_marks);
        printf("\n");
        printf("'%s':\n",array[i].name);
        float avg = (array[i].phy_marks+array[i].maths_marks+array[i].bio_marks+array[i].chem_marks)/4.0;
        printf("The average marks of the student: %.2f\n",avg);
        
        int max = array[i].phy_marks;
        if(max < array[i].chem_marks){
            max = array[i].chem_marks;
        }
        if(max < array[i].bio_marks){
            max = array[i].bio_marks;
        }
        if(max < array[i].maths_marks){
            max = array[i].maths_marks;
        }

        int min = array[i].phy_marks;
        if(min > array[i].chem_marks){
            min = array[i].chem_marks;
        }
        if(min > array[i].bio_marks){
            min = array[i].bio_marks;
        }
        if(min > array[i].maths_marks){
            min = array[i].maths_marks;
        }

        printf("Maximum marks: %d\nMinimum marks: %d\n", max, min);
        gradesys(avg);
        printf("\n\n");
        clearInputBuffer();
    }

    int max, count;

    printf("In Physics:\n");
    max = array[0].phy_marks;
    count = 0;
    for(int i = 1; i < num; i++){
        if(max < array[i].phy_marks){
            max = array[i].phy_marks;
            count = i;
        }
    }
    printf("%s got maximum %d marks in Physics\n", array[count].name, array[count].phy_marks);

    printf("In Chemistry:\n");
    max = array[0].chem_marks;
    count = 0;
    for(int i = 1; i < num; i++){
        if(max < array[i].chem_marks){
            max = array[i].chem_marks;
            count = i;
        }
    }
    printf("%s got maximum %d marks in Chemistry\n", array[count].name, array[count].chem_marks);

    printf("In Maths:\n");
    max = array[0].maths_marks;
    count = 0;
    for(int i = 1; i < num; i++){
        if(max < array[i].maths_marks){
            max = array[i].maths_marks;
            count = i;
        }
    }
    printf("%s got maximum %d marks in Mathematics\n", array[count].name, array[count].maths_marks);

    printf("In Biology:\n");
    max = array[0].bio_marks;
    count = 0;
    for(int i = 1; i < num; i++){
        if(max < array[i].bio_marks){
            max = array[i].bio_marks;
            count = i;
        }
    }
    printf("%s got maximum %d marks in Biology\n", array[count].name, array[count].bio_marks);

    printf("\n\n");
    printf("Thank You for using my STUDENT GRADE MANAGEMENT system......I hope it performed well without any bugs in your work\n\n");

    return 0;
}

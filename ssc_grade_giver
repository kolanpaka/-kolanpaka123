




class Check_result:
    '''THIS CLASS NAME  IS Check_result():
    which help full for estimating grades,GPA,avg_marks for ssc students
     atrributes={self.data={}}
     ___________________________disclamier :_______________________________________________
     DONOT USE INVALID INPUT WHILE USING SELF.INPUT_FROM_USER() function'''
    def __init__(self):
        self.data={}
    def total_marks(self):
        return sum(i for i in self.list_1)

    def estimate_grade(self,marks,subject,ranges, grade, points_dic):
        for i in ranges:
            if marks in list(range(i[0], i[1] + 1)):
                d = ranges.index([i[0], i[1]])
                self.data_set = [subject, [i[0], i[1]], grade[d], points_dic[grade[d]]]
                return self.data_set
    def grades(self,marks,subject):
        grade = ["A1", "A2", "B1", "B2", "C1", "c2", "D1", "D2", "E"]
        points = list(range(10, 2, -1))
        points.append("Fail")
        points_dic = dict(zip(grade, points))
        self.data=points_dic

        if subject.lower()!="hindi":
            ranges = [[92, 100], [83, 91], [0, 34]]
            k = 35
            for i in range(k, 75, 7):
                ranges.insert(2, [k, k + 7])
                k = k + 8
            dic = dict(zip(grade, ranges))
            s00w=self.estimate_grade(marks,subject,ranges, grade, points_dic)
            return s00w
        else:
            ranges_1=[[90,100]]+list([i,i+9] for i in range(80,10,-10))+[[0,19]]
            ranges_1_dic=dict(zip(grade,ranges_1))
            s00w=self.estimate_grade(marks,subject,ranges_1, grade, points_dic)
            return s00w
    def input_from_user(self):
        subjects=["Telugu","Hindi","English","Maths","Science","Social"]
        marks_list=[]
        for i in subjects:
            s_l=int(input("hey user input your marks of {} subject: ".format(i)))
            marks_list.append(s_l)
        marks_dict=dict(zip(subjects,marks_list))
        print("\t\n")
        print("SUBJECT          RANGE          GRADE          POINTS          ")
        print("\t\n")
        total=0
        failed_sub=[]
        statment=False
        for sub,marks in marks_dict.items():
            y=self.grades(marks,sub)
            if y[3]=="Fail":
                total+=0
                statment=True
                failed_sub.append(sub)
            else:
                total+=y[3]

            print("-------------------------------------------------------------------------------------------------------------------------------------------------")
            print("\t\n")
            print(f'{y[0]}          {y[1][0]}-{y[1][1]}           {y[2]}           {y[3]}')


        print('-----------------------------------------------------------------------------------------------------------------------------------------------------------')

        print("\t\n")
        print(" NOTE: ")
        if statment==True:
            print(f'sorry ! to say user you are Failed in {len(failed_sub)} subjects : ')
            for i in failed_sub:
                print(i.title())
            print(" TRY NEXT TIME! ")
        else:
            print(f"you secured {sum(marks_list)}/600 marks")
            print(f'total gpa (all subjects) : {round(total / 6,1)}')
            for i, j in self.data.items():
                if j == int(total / 6):
                    print(f'GRADE: {i}')
        print("*************************************************************\\END//***********************************************************************************************")








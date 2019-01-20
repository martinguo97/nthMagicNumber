from math import gcd
class nthMagicNumber:
    def nthMagicalNumber(self, N, A, B):
        period=A*B
        overlap_list=[]
        number_of_element=A+B-1
        overlap=gcd(A,B)-1
        group=N/number_of_element
        total_overlap=int(group)*overlap
        if group==int(group):
            group=int(group)
            group-=1

        # group=int(group)
        # total_overlap=group*overlap
        remain=total_overlap%number_of_element
        remain_group=int(total_overlap/number_of_element)
        group+=int(remain_group)
        print("group begain is ",group)
        if N%number_of_element==0:
            count=number_of_element
        else:
            count=N%number_of_element    
        count+=remain
        print("count1",count)
        if count>number_of_element:
            more_group=count/number_of_element
            print("more_group is",more_group)
            group+=int(more_group)
            # count=count%number_of_element
            print("count 2 ",count)
            
        # if group!=int(group):
        print("group is",group)
        group=int(group)
        start=period*group
        end=period*(group+1)
        # else:
        #     group=int(group)
        #     start=period*(group-1)
        #     end=period*group
        print(group)
        position=N%(number_of_element-overlap)
        number_list=set()
        copy=start
        if A==B:
            result=(N*A)%(10**9+7)
            print(result)
            return result
        else:
            while start+A<=end:
                start+=A
                number_list.add(start)
            while copy+B<end:
                copy+=B

                if copy in number_list:
                    overlap_list.append(copy)
                number_list.add(copy)
            # overlap_counter=0
            # for element in overlap_list
        print("overlap is",overlap)
        number_list=list(number_list)
        number_list.sort()
        print(number_list)
        print(number_list[position-1]%(10**9+7))
            



        
        return number_list[position-1]%(10**9+7)

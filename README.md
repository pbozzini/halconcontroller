# halconcontroller
This package allows to control MvTec HALCON Programs into Python. 

PROGRAMMING EXAMPLE:
###################################################################################
import os 
# Import Class from the Package
from halconcontroller import HalconProgram

# main programm
def main():

    # the class need two arguments: the program path and the program Name
    path='PATH PF THE PROGRAM'
    ProgName='PROGRAM NAME.hdev'

    # Generate class object with arguments
    Prog = HalconProgram(ProgName,path)

    # function 1 --> load a HALCON program and generate all his variables
    prova=Prog.loadProgram()

    # function 2 --> load and execute a HALCON programm
    prova2=Prog.executeProgram()

    # function 1 --> load, execute and generate a JSON structured data that holds the iconic and the control variables
    prova3=Prog.getResults()


###################################################################################
    



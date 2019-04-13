import random
def printboard(board):
    print("----------------------------------------------------------------")
    print("current situation")
    print(str(board[0][0])+"    "+str(board[0][1])+"    "+str(board[0][2]))
    print(str(board[1][0])+"    "+str(board[1][1])+"    "+str(board[1][2]))
    print(str(board[2][0])+"    "+str(board[2][1])+"    "+str(board[2][2]))
    
def updateboard(board,choice,turn):
    if choice<3:
        if turn==0:
            board[0][choice]='O'
        else:
             board[0][choice]='X'
    elif choice<6:
        if turn==0:
            board[1][choice-3]='O'
        else:
            board[1][choice-3]='X'
    else:
        if turn==0:
            board[2][choice-6]='O'
        else:
            board[2][choice-6]='X'
def threeinarow(board):
    check=board[0][0]
    if(board[1][1]==check and board[2][2]==check and check!='-'):
        return 1
    check=board[0][2]
    if(board[1][1]==check and board[2][0]==check and check!='-'):
        return 1
    for i in range(3):
       if(end==0):
            check=board[i][0]
            if(board[i][1]==check and board[i][2]==check and check!='-'):
                return 1
            check=board[0][i]
            if(board[1][i]==check and board[2][i]==check and check!='-'):
                return 1
    return 0
turn = 0 #a variable to see whose turn it is
print("1 player or  2 players: ")
board=[[],[],[]]
players=int(input()) 
for i in range(3):
    board[i]=['-' for x in range(3)]
b=[x for x in range(9)] #choices available
end=0 #variable to see of game ended or not

if players==1:
    while(end==0):
        if(turn==0):
            print("computers turn: ")
            choice=random.choice(b)
            print("entering my move")
            updateboard(board,choice,turn)
            b.remove(choice)
            printboard(board)
            end=threeinarow(board)
            turn=1
        else:
            print("your turn. Enter the position: ")
            choice=int(input())-1
            print("entering your move")
            updateboard(board,choice,turn)
            b.remove(choice)
            printboard(board)
            end=threeinarow(board)
            turn=0
        if len(b)==0:
            print("game draw")
            end=1
        if(end==1):
            if turn==0:
                print("you won")
            else:
                print("computer won")
            

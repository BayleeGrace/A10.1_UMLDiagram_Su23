```mermaid
classDiagram


%%AI for characters in the Land of Smell in a video game

    SmellAI<--smellNight
    SmellAI<--smellDay

class SmellAI{
    String location cityOfSmell
    String buildingType slums
    String buildingType treeHouse

    detTime()
}

    class smellNight{
        String characterType childN
        String characterType adultN
        String location landOfSmell
        int amountInLocation 20

        determineTimeCycle()
        findPath()
    }

    class smellDay{
        class characterType childD
        String characterType adultD
        String location landOfSmell
        int amountInLocation 20

        determineTimeCycle()
        findPath()
    }


%%AI for characters in the Land of Touch in a video game

    TouchAI<--touchNight
    TouchAI<--touchDay

    touchNight<--childN
    touchNight<--mentorN
    touchNight<--scientistN

class TouchAI{
    String location cityOfTouch
    String buildingType electric

    detTime()

}

    class touchNight{
        class characterType childN
        class characterType mentorN
        class characterType scientistN
        String location landOfTouch
        int amountInLocation 20
        bool isNight true

        determineTimeCycle()
        findPath()
    }

        class childN{
            String mentorN
            String playItem
            String mentorTask1
            bool canSleep true
            
            findPlayItem()
            play()
            followMentor()
            chasePlayer()
        }

        class mentorN{
            String childN
            String teachItem
            String mentorTask1
            bool canSleep false
            
            findTeachItem()
            teach()
            findTeachPath()
            findRunPath()
        }

        class scientistN{
            String testTubes
            String scientistTask1
            int numberOfTasks 5
            bool gogglesOn true
            bool canSleep false
            
            removeGoggles()
            replaceGoggles
            findTask()
            stressAnimation()
        }

    touchDay<--childD
    touchDay<--mentorD
    touchDay<--scientistD

    class touchDay{
        class characterType childD
        class characterType mentorD
        class characterType scientistD
        String location landOfTouch
        int amountInLocation 20
        bool isNight false

        determineTimeCycle()
        findPath()
    }

        class childD{
            String projectItem
            String childChair
            int timeForPresentation 10

            presentProjectTurn()
            findSeatPath()
        }

        class mentorD{
            String childD
            Sting mentorChair
            bool canSleep true
            
            findPresentor()
        }

        class scientistD{
            String testTubes
            String scientistHome
            int numberOfTasks 0
            bool gogglesOn true
            bool canSleep true
            
            removeGoggles()
            replaceGoggles
            sleepAnimation()
        }

    
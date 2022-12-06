import kotlin.Array as KotlinArray

fun main(args: KotlinArray<String>) {
    open class Animal(name: String, food: String, hunt: String) {
        init {
            println("Name is $name")
            println("Basic food is $food")
            println("This animal is a $hunt")
        }

    }

    class herbiroves(name: String, food: String, hunt: String) : Animal(name, food, hunt) {
        fun doProgram() {
            println("The class of this animal is herbivorous")
        }

        inner class carnivores(name: String, food: String, hunt: String) : Animal(name, food, hunt) {
            fun fieldWork() {
                println("The class of this animal is carnivores")
            }

        }

        fun main(args:KotlinArray<String>) {
            val obj1 = herbiroves("cow", "grass", "not hunter")
            obj1.doProgram()
            val obj2 = herbiroves("goat", "grass", "not hunter")
            obj2.doProgram()
            val obj3 = herbiroves("lion", "meat", "hunter")
            obj3.doProgram()
            val obj4 = herbiroves("wolf", "meat", "hunter")
            obj4.doProgram()
        }
    }
}

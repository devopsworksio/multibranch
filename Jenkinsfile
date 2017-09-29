node() {

    checkout scm

    def somename
    def message = "Hello Word!"
    somename = load 'loaded.groovy'

    try {
        somename.hello()
    } catch (error) {
        println error
    }

}

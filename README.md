# progKievUa
progKievUa

package progUa.annatationLesson.homework.task3_1;

public class MyMaintask3_1 {
    public static void main(String[] args) throws IllegalAccessException, NoSuchFieldException, InstantiationException {
        MyClassForSerialisation mcfs = new MyClassForSerialisation();
        mcfs.setName("Pavel");
        mcfs.setAge(28);
        mcfs.setYear("2017");

        String res = MySerialisation.serialize(mcfs);
        System.out.println("serialized " + res);

        MyClassForSerialisation newMsfc = new MyClassForSerialisation();
        newMsfc = MySerialisation.deserialize(res, MyClassForSerialisation.class);
        System.out.println("deserialized " + newMsfc.getName() + newMsfc.getAge() + newMsfc.getYear());
    }
}

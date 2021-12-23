import java.awt.*; 
 import java.awt.event.*; 
 import java.applet.*; 
 /* <APPLET CODE ="TextareaJavaApplet.class" WIDTH=300 HEIGHT=200> </APPLET> */ 
 public class TextareaJavaApplet extends Applet implements ActionListener 
   { 
       TextArea txt; 
       Button b1,b2; 
       String s1,s2; 
       Label l1,l2,l3; 
       TextField t1,t2,t3; 
         public void init() 
             { 
                 txt = new TextArea(5,30); 
                 add(txt); 
                 s1="This is the text which is already present in textarea\nMerry"+ "Christmas to     
                 you\nToday it may rain"; 
                 txt.append(s1); 
                 s2="In the middle this text will be inserted"; 
                 b1=new Button("insert Text"); 
                 add(b1); 
                 b1.addActionListener(this); 
                 l1=new Label("Replacing a range of above text with new text.Enter starting location"); 
                 add(l1); 
                 t1=new TextField(10); 
                 add(t1); 
                 l2=new Label("Ending range"); 
                 add(l2); 
                 t2=new TextField(10); 
                 add(t2); 
                 l3=new Label("Replacing with"); 
                 add(l3); 
                 t3=new TextField(10); 
                 add(t3); 
                 b2=new Button("Replace"); 
                 add(b2); 
                 b2.addActionListener(this); 
              }      
                 public void actionPerformed(ActionEvent e) 
                    { 
                      int start,end; 
                      if(e.getSource()==b1) 
                         { 
                           txt.insert(s2,12); 
                        } 
                           if(e.getSource()==b2) 
                             { 
                                start=Integer.parseInt(t1.getText()); 
                                end=Integer.parseInt(t2.getText()); 
                                txt.replaceRange(t3.getText(),start,end); 
                             } 
                     } 
    }

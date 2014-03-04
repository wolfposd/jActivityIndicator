jActivityIndicator
==================

A Java Swing Activity Indicator

Simple to use, comes with 2 styles, easily use your own


SampleCode:

    public static void main(String[] args)
    {
        final JActivityIndicator act = new JActivityIndicator(1);
        final JActivityIndicator act2 = new JActivityIndicator(0);

        JFrame frame = new JFrame();
        frame.setLayout(new FlowLayout());
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300, 300);

        frame.add(act);
        frame.add(act2);

        JButton button = new JButton("Start/Stop");
        frame.add(button);

        button.addActionListener(new ActionListener()
        {
            public void actionPerformed(ActionEvent e)
            {
                act.toggleRotating();
                act2.toggleRotating();
            }
        });

        frame.setVisible(true);
    }

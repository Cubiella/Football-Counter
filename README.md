package com.example.android.footballcounter;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;

import com.example.android.footballcounter.R;

public class MainActivity extends AppCompatActivity {
    int scoreRMadrid = 0;
    int scoreBarça = 0;
    int redCardRMadrid = 0;
    int redCardBarça = 0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    /**
     * Increase the score for RMadrid by 1 goal.
     */

    public void addAGoalForRMadrid(View v) {
        scoreRMadrid = scoreRMadrid + 1;
        displayForRMadrid(scoreRMadrid);
    }

    /**
     * Increase the score for Barça by 1 goal.
     */
    public void addAGoalForBarça(View v) {
        scoreBarça = scoreBarça + 1;
        displayForBarça(scoreBarça);
    }
        /**
     * Increase the number of Red Cards for RMadrid by one.
     */
    public void addARedCardForRMadrid(View v) {
        redCardRMadrid = redCardRMadrid + 1;
        displayRCardForRMadrid(redCardRMadrid);;
    }
    /**
     * Increase the number of Red Cards for RMadrid by one.
     */
    public void addARedCardForBarça(View v) {
        redCardBarça = redCardBarça + 1;
        displayRCardForBarça(redCardBarça);;
    }
    /**
     * This method resets the counter to 0
     */
    public void reset(View v) {
        scoreRMadrid = 0;
        scoreBarça = 0;
        redCardRMadrid = 0;
        redCardBarça = 0;
        displayForRMadrid(scoreRMadrid);
        displayForBarça(scoreBarça);
        displayRCardForRMadrid(redCardRMadrid);
        displayRCardForBarça(redCardBarça);
    }
    /**
     * Displays the given score for RMadrid.
     */
    public void displayForRMadrid(int score) {
        TextView scoreView = (TextView) findViewById(R.id.GoalsForRMadrid);
        scoreView.setText(String.valueOf(score));
    }
    /**
     * Displays the given score for Barça.
     */
    public void displayForBarça(int score) {
        TextView scoreView = (TextView) findViewById(R.id.GoalsForBarça);
        scoreView.setText(String.valueOf(score));
    }
    /**
     * Displays the Red Cards for RMadrid.
     */
    public void displayRCardForRMadrid(int score) {
        TextView scoreView = (TextView) findViewById(R.id.RedCardsForRMadrid);
        scoreView.setText(String.valueOf(score));
    }
    /**
     * Displays the Red Cards for Barça.
     */
    public void displayRCardForBarça(int score) {
        TextView scoreView = (TextView) findViewById(R.id.RedCardsForBarça);
        scoreView.setText(String.valueOf(score));
    }
}

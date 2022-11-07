import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void printMatrix(int SIZE, int colors[][]) {
        for (int i = 0; i < SIZE; i++) {
            for (int j = 0; j < SIZE; j++) {
                System.out.format("%4d", colors[i][j]);
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {

        int SIZE = 8;
        int[][] colors = new int[SIZE][SIZE];
        Random random = new Random();
        for (int i = 0; i < SIZE; i++) {
            for (int j = 0; j < SIZE; j++) {
                colors[i][j] = random.nextInt(256);
            }
        }

        printMatrix(SIZE, colors);
        System.out.println();
        int[][] rotatedColors = new int[SIZE][SIZE];
        System.out.print("Введите угол поворота матрицы в градусах(90/180/270):");
        Scanner scanner = new Scanner(System.in);
        int input = scanner.nextInt();
        switch (input) {
            case 90:
                rotateMatrix(SIZE, colors, rotatedColors);
                break;
            case 180:
                rotateMatrix(SIZE, colors, rotatedColors);
                copyMatrix(SIZE, colors, rotatedColors);
                rotateMatrix(SIZE, colors, rotatedColors);
                break;
            case 270:
                rotateMatrix(SIZE, colors, rotatedColors);
                copyMatrix(SIZE, colors, rotatedColors);
                rotateMatrix(SIZE, colors, rotatedColors);
                copyMatrix(SIZE, colors, rotatedColors);
                rotateMatrix(SIZE, colors, rotatedColors);
                break;
            default:
                System.out.println("Недопустимый ввод!");
        }
        printMatrix(SIZE, rotatedColors);
    }

    public static int rotateMatrix(int SIZE, int colors[][], int rotatedColors[][]) {
        for (int i = 0; i < SIZE; i++) {
            for (int j = 0; j < SIZE; j++) {
                rotatedColors[i][j] = colors[SIZE - j - 1][i];
            }
        }
        return rotatedColors[SIZE - 1][SIZE - 1];
    }

    public static int copyMatrix(int SIZE, int colors[][], int rotatedColors[][]) {
        for (int i = 0; i < SIZE; i++) {
            for (int j = 0; j < SIZE; j++) {
                colors[i][j] = rotatedColors[i][j];
            }
        }
        return colors[SIZE - 1][SIZE - 1];
    }
}
#include <stdio.h>
double calculate_execution_time(double cpi, double clock_rate, int instructions) 
{
    return (cpi * instructions) / clock_rate;
}
int main() {
    int num_processors, instructions;
    double cpi, clock_rate;
    printf("Enter the number of processors: ");
    scanf("%d", &num_processors);
    double execution_times[num_processors];
    double response_times[num_processors];
    double throughputs[num_processors];
    for (int i = 0; i < num_processors; i++) {
        printf("Enter the Cycles per Instruction (CPI) of processor %d: ", i + 1);
        scanf("%lf", &cpi);
        printf("Enter the clock rate in GHz of processor %d: ", i + 1);
        scanf("%lf", &clock_rate);
        clock_rate *= 1e9;
        printf("Enter the number of instructions for processor %d: ", i + 1);
        scanf("%d", &instructions);
        double execution_time = calculate_execution_time(cpi, clock_rate, instructions);
        double response_time = execution_time; 
        double throughput = instructions / execution_time;
        execution_times[i] = execution_time;
        response_times[i] = response_time;
        throughputs[i] = throughput;
    printf("Processor %d - Execution Time: %f seconds, Response Time: %f seconds, Throughput: %f instructions/second\n",
               i + 1, execution_time, response_time, throughput);
    }
    double min_execution_time = execution_times[0];
    int best_processor_index = 0;
    for (int i = 1; i < num_processors; i++) {
        if (execution_times[i] < min_execution_time) {
            min_execution_time = execution_times[i];
            best_processor_index = i;
        }
    }
    printf("\nProcessor with the lowest execution time is Processor %d with %f seconds.\n",
           best_processor_index + 1, min_execution_time);
    return 0;
}

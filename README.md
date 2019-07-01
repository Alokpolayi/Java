/**
	 * @param args using Normal for to remove duplicate in a array
	 */
	public static void removeDuplicateElement(int[] arr) {
		System.out.println("Before Removing duplicate : ");
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + "\t");
		}
		int noOfElement = arr.length;
		for (int i = 0; i < noOfElement; i++) {
			for (int j = i + 1; j < noOfElement; j++) {
				if (arr[i] == arr[j]) {
					arr[j] = arr[noOfElement - 1];
					noOfElement--;
					j--;
				}
			}
		}
		int withOutDuplicate[] = Arrays.copyOf(arr, noOfElement);
		System.out.println();
		System.out.println("After removing duplicate elements : ");
		for (int i = 0; i < withOutDuplicate.length; i++) {
			System.out.print(withOutDuplicate[i] + "\t");
		}
	}


---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a5087c3c2d2354eb33ab9777687d43f56f3eb42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532292"
---
# <span data-ttu-id="37d60-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="37d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d60-102">SYNOPSIS</span></span>
<span data-ttu-id="37d60-103">Data Lake Store에서 파일 또는 폴더가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37d60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37d60-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37d60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="37d60-105">DESCRIPTION</span></span>
<span data-ttu-id="37d60-106">**AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에 파일 또는 폴더가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="37d60-107">예제의</span><span class="sxs-lookup"><span data-stu-id="37d60-107">EXAMPLES</span></span>

### <span data-ttu-id="37d60-108">예제 1: 파일 테스트</span><span class="sxs-lookup"><span data-stu-id="37d60-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="37d60-109">이 명령은 ContosoADL 계정에 파일 Test.csv 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="37d60-110">변수</span><span class="sxs-lookup"><span data-stu-id="37d60-110">PARAMETERS</span></span>

### <span data-ttu-id="37d60-111">-계정</span><span class="sxs-lookup"><span data-stu-id="37d60-111">-Account</span></span>
<span data-ttu-id="37d60-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d60-113">-Path</span><span class="sxs-lookup"><span data-stu-id="37d60-113">-Path</span></span>
<span data-ttu-id="37d60-114">루트 디렉터리 (/)로 시작 하 여 테스트할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-114">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d60-115">-PathType</span><span class="sxs-lookup"><span data-stu-id="37d60-115">-PathType</span></span>
<span data-ttu-id="37d60-116">테스트할 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-116">Specifies the type of item to test.</span></span>
<span data-ttu-id="37d60-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37d60-118">이상</span><span class="sxs-lookup"><span data-stu-id="37d60-118">Any</span></span> 
- <span data-ttu-id="37d60-119">파일</span><span class="sxs-lookup"><span data-stu-id="37d60-119">File</span></span> 
- <span data-ttu-id="37d60-120">폴더</span><span class="sxs-lookup"><span data-stu-id="37d60-120">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37d60-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d60-121">-DefaultProfile</span></span>
<span data-ttu-id="37d60-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d60-123">CommonParameters</span></span>
<span data-ttu-id="37d60-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d60-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d60-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d60-126">입력</span><span class="sxs-lookup"><span data-stu-id="37d60-126">INPUTS</span></span>

## <span data-ttu-id="37d60-127">출력</span><span class="sxs-lookup"><span data-stu-id="37d60-127">OUTPUTS</span></span>

### <span data-ttu-id="37d60-128">부울</span><span class="sxs-lookup"><span data-stu-id="37d60-128">bool</span></span>
<span data-ttu-id="37d60-129">지정 된 파일 또는 폴더가 있음을 나타내는 True 또는 false입니다.</span><span class="sxs-lookup"><span data-stu-id="37d60-129">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="37d60-130">상속자</span><span class="sxs-lookup"><span data-stu-id="37d60-130">NOTES</span></span>

## <span data-ttu-id="37d60-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37d60-131">RELATED LINKS</span></span>

[<span data-ttu-id="37d60-132">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-132">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="37d60-133">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-133">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="37d60-134">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-134">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="37d60-135">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-135">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="37d60-136">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-136">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="37d60-137">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37d60-137">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)



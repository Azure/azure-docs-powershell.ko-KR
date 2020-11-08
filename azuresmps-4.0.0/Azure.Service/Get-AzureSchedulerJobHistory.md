---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046310"
---
# <span data-ttu-id="6e45d-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="6e45d-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="6e45d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e45d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e45d-103">스케줄러 작업에 대 한 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="6e45d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e45d-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e45d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e45d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e45d-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6e45d-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6e45d-108">**AzureSchedulerJobHistory** cmdlet은 스케줄러 작업에 대 한 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="6e45d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e45d-109">EXAMPLES</span></span>

### <span data-ttu-id="6e45d-110">예제 1: 이름을 사용 하 여 작업에 대 한 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e45d-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="6e45d-111">이 명령은 Job01 이라는 작업 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="6e45d-112">해당 작업은 지정 된 위치에서 JobCollection01 이라는 작업 컬렉션에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="6e45d-113">예제 2: 이름을 사용 하 여 실패 한 작업에 대 한 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e45d-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="6e45d-114">이 명령은 상태가 실패 한 Job12 이라는 작업 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="6e45d-115">해당 작업은 지정 된 위치에서 JobCollection01 이라는 작업 컬렉션에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="6e45d-116">변수</span><span class="sxs-lookup"><span data-stu-id="6e45d-116">PARAMETERS</span></span>

### <span data-ttu-id="6e45d-117">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="6e45d-117">-First</span></span>
<span data-ttu-id="6e45d-118">지정 된 수의 개체만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="6e45d-119">가져올 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="6e45d-120">-IncludeTotalCount</span></span>
<span data-ttu-id="6e45d-121">데이터 집합 (정수)에 있는 개체의 총 수와 선택한 개체를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="6e45d-122">Cmdlet에서 총 개수를 확인할 수 없는 경우 "알 수 없는 총 개수"가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="6e45d-123">Integer에는 총 count 값의 안정성을 나타내는 정확도 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="6e45d-124">정확도 값의 범위는 0.0에서 0.0 1.0는 cmdlet이 개체 수를 계산할 수 없음을 의미 하 고, 1.0에서는 카운트가 정확한 지를 의미 하며, 0.0 및 1.0 간의 값이 점차 안정적인 추정치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6e45d-125">-JobCollectionName</span></span>
<span data-ttu-id="6e45d-126">스케줄러 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="6e45d-127">이 cmdlet은이 매개 변수에서 지정 하는 컬렉션에 속한 작업의 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="6e45d-128">-JobName</span></span>
<span data-ttu-id="6e45d-129">기록을 가져올 스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-129">Specifies the name of a scheduler job for which to get the history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="6e45d-130">-JobStatus</span></span>
<span data-ttu-id="6e45d-131">기록을 가져올 스케줄러 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="6e45d-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e45d-133">완료</span><span class="sxs-lookup"><span data-stu-id="6e45d-133">Completed</span></span>
- <span data-ttu-id="6e45d-134">못함</span><span class="sxs-lookup"><span data-stu-id="6e45d-134">Failed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-135">-위치</span><span class="sxs-lookup"><span data-stu-id="6e45d-135">-Location</span></span>
<span data-ttu-id="6e45d-136">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="6e45d-137">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-137">Valid values are:</span></span> 

- <span data-ttu-id="6e45d-138">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="6e45d-138">Anywhere Asia</span></span>
- <span data-ttu-id="6e45d-139">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="6e45d-139">Anywhere Europe</span></span>
- <span data-ttu-id="6e45d-140">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="6e45d-140">Anywhere US</span></span>
- <span data-ttu-id="6e45d-141">동아시아</span><span class="sxs-lookup"><span data-stu-id="6e45d-141">East Asia</span></span>
- <span data-ttu-id="6e45d-142">미국 동부</span><span class="sxs-lookup"><span data-stu-id="6e45d-142">East US</span></span>
- <span data-ttu-id="6e45d-143">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="6e45d-143">North Central US</span></span>
- <span data-ttu-id="6e45d-144">동유럽</span><span class="sxs-lookup"><span data-stu-id="6e45d-144">North Europe</span></span>
- <span data-ttu-id="6e45d-145">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="6e45d-145">South Central US</span></span>
- <span data-ttu-id="6e45d-146">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="6e45d-146">Southeast Asia</span></span>
- <span data-ttu-id="6e45d-147">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="6e45d-147">West Europe</span></span>
- <span data-ttu-id="6e45d-148">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="6e45d-148">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-149">-프로필</span><span class="sxs-lookup"><span data-stu-id="6e45d-149">-Profile</span></span>
<span data-ttu-id="6e45d-150">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e45d-151">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-152">-생략</span><span class="sxs-lookup"><span data-stu-id="6e45d-152">-Skip</span></span>
<span data-ttu-id="6e45d-153">지정 된 수의 개체를 무시 한 다음 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="6e45d-154">건너뛸 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e45d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e45d-155">CommonParameters</span></span>
<span data-ttu-id="6e45d-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e45d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e45d-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e45d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e45d-158">입력</span><span class="sxs-lookup"><span data-stu-id="6e45d-158">INPUTS</span></span>

## <span data-ttu-id="6e45d-159">출력</span><span class="sxs-lookup"><span data-stu-id="6e45d-159">OUTPUTS</span></span>

## <span data-ttu-id="6e45d-160">상속자</span><span class="sxs-lookup"><span data-stu-id="6e45d-160">NOTES</span></span>

## <span data-ttu-id="6e45d-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e45d-161">RELATED LINKS</span></span>

[<span data-ttu-id="6e45d-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="6e45d-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="6e45d-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6e45d-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)



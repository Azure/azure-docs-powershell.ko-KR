---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046311"
---
# <span data-ttu-id="95d3d-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="95d3d-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="95d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="95d3d-103">스케줄러 작업 또는 특정 스케줄러 작업의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="95d3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95d3d-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95d3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="95d3d-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95d3d-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95d3d-108">**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 또는 특정 스케줄러 작업의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="95d3d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="95d3d-109">EXAMPLES</span></span>

### <span data-ttu-id="95d3d-110">예제 1: 컬렉션의 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="95d3d-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="95d3d-111">이 명령은 JobCollection01 이라는 작업 컬렉션의 일부인 스케줄러 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="95d3d-112">예제 2: 명명 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="95d3d-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="95d3d-113">이 명령은 지정 된 위치에 JobCollection01 이라는 컬렉션에서 Job01 라는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="95d3d-114">예제 3: 컬렉션에서 사용 하지 않도록 설정 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="95d3d-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="95d3d-115">이 명령은 지정 된 위치에서 JobCollection01의 일부인 비활성화 된 모든 스케줄러 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="95d3d-116">변수</span><span class="sxs-lookup"><span data-stu-id="95d3d-116">PARAMETERS</span></span>

### <span data-ttu-id="95d3d-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="95d3d-117">-JobCollectionName</span></span>
<span data-ttu-id="95d3d-118">가져올 스케줄러 작업을 포함 하는 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="95d3d-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="95d3d-119">-JobName</span></span>
<span data-ttu-id="95d3d-120">가져올 스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="95d3d-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="95d3d-121">-JobState</span></span>
<span data-ttu-id="95d3d-122">가져올 스케줄러 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="95d3d-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95d3d-124">수</span><span class="sxs-lookup"><span data-stu-id="95d3d-124">Enabled</span></span>
- <span data-ttu-id="95d3d-125">비활성화</span><span class="sxs-lookup"><span data-stu-id="95d3d-125">Disabled</span></span>
- <span data-ttu-id="95d3d-126">오류</span><span class="sxs-lookup"><span data-stu-id="95d3d-126">Faulted</span></span>
- <span data-ttu-id="95d3d-127">완료</span><span class="sxs-lookup"><span data-stu-id="95d3d-127">Completed</span></span>

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

### <span data-ttu-id="95d3d-128">-위치</span><span class="sxs-lookup"><span data-stu-id="95d3d-128">-Location</span></span>
<span data-ttu-id="95d3d-129">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="95d3d-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95d3d-131">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="95d3d-131">Anywhere Asia</span></span>
- <span data-ttu-id="95d3d-132">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="95d3d-132">Anywhere Europe</span></span>
- <span data-ttu-id="95d3d-133">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="95d3d-133">Anywhere US</span></span>
- <span data-ttu-id="95d3d-134">동아시아</span><span class="sxs-lookup"><span data-stu-id="95d3d-134">East Asia</span></span>
- <span data-ttu-id="95d3d-135">미국 동부</span><span class="sxs-lookup"><span data-stu-id="95d3d-135">East US</span></span>
- <span data-ttu-id="95d3d-136">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="95d3d-136">North Central US</span></span>
- <span data-ttu-id="95d3d-137">동유럽</span><span class="sxs-lookup"><span data-stu-id="95d3d-137">North Europe</span></span>
- <span data-ttu-id="95d3d-138">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="95d3d-138">South Central US</span></span>
- <span data-ttu-id="95d3d-139">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="95d3d-139">Southeast Asia</span></span>
- <span data-ttu-id="95d3d-140">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="95d3d-140">West Europe</span></span>
- <span data-ttu-id="95d3d-141">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="95d3d-141">West US</span></span>

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

### <span data-ttu-id="95d3d-142">-프로필</span><span class="sxs-lookup"><span data-stu-id="95d3d-142">-Profile</span></span>
<span data-ttu-id="95d3d-143">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95d3d-144">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95d3d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d3d-145">CommonParameters</span></span>
<span data-ttu-id="95d3d-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d3d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d3d-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d3d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d3d-148">입력</span><span class="sxs-lookup"><span data-stu-id="95d3d-148">INPUTS</span></span>

## <span data-ttu-id="95d3d-149">출력</span><span class="sxs-lookup"><span data-stu-id="95d3d-149">OUTPUTS</span></span>

## <span data-ttu-id="95d3d-150">상속자</span><span class="sxs-lookup"><span data-stu-id="95d3d-150">NOTES</span></span>

## <span data-ttu-id="95d3d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d3d-151">RELATED LINKS</span></span>

[<span data-ttu-id="95d3d-152">제거-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="95d3d-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045980"
---
# <span data-ttu-id="e5859-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e5859-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="e5859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5859-102">SYNOPSIS</span></span>
<span data-ttu-id="e5859-103">스케줄러 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="e5859-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5859-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5859-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5859-105">DESCRIPTION</span></span>
<span data-ttu-id="e5859-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e5859-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e5859-108">**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="e5859-109">*Plan* 매개 변수에 대 한 값을 지정 하지 않으면 cmdlet이 표준 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="e5859-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e5859-110">EXAMPLES</span></span>

### <span data-ttu-id="e5859-111">예제 1: 기본 값이 포함 된 스케줄러 작업 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="e5859-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="e5859-112">이 명령은 JobCollection01 이라는 표준 스케줄러 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="e5859-113">새 컬렉션에는 표준 스케줄러 작업 모음에 대 한 기본 작업 수 및 최대 되풀이 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="e5859-114">예제 2: 지정 된 값을 사용 하 여 스케줄러 작업 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="e5859-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="e5859-115">이 명령은 JobCollection02 이라는 표준 스케줄러 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="e5859-116">새 컬렉션의 최대 작업 수는 30이 고 최대 되풀이 시간은 시간 당 12입니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="e5859-117">변수</span><span class="sxs-lookup"><span data-stu-id="e5859-117">PARAMETERS</span></span>

### <span data-ttu-id="e5859-118">-빈도</span><span class="sxs-lookup"><span data-stu-id="e5859-118">-Frequency</span></span>
<span data-ttu-id="e5859-119">이 스케줄러 작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5859-120">-Interval</span><span class="sxs-lookup"><span data-stu-id="e5859-120">-Interval</span></span>
<span data-ttu-id="e5859-121">*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5859-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e5859-122">-JobCollectionName</span></span>
<span data-ttu-id="e5859-123">새 스케줄러 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="e5859-124">-위치</span><span class="sxs-lookup"><span data-stu-id="e5859-124">-Location</span></span>
<span data-ttu-id="e5859-125">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="e5859-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-126">Valid values are:</span></span> 

- <span data-ttu-id="e5859-127">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="e5859-127">Anywhere Asia</span></span>
- <span data-ttu-id="e5859-128">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="e5859-128">Anywhere Europe</span></span>
- <span data-ttu-id="e5859-129">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="e5859-129">Anywhere US</span></span>
- <span data-ttu-id="e5859-130">동아시아</span><span class="sxs-lookup"><span data-stu-id="e5859-130">East Asia</span></span>
- <span data-ttu-id="e5859-131">미국 동부</span><span class="sxs-lookup"><span data-stu-id="e5859-131">East US</span></span>
- <span data-ttu-id="e5859-132">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="e5859-132">North Central US</span></span>
- <span data-ttu-id="e5859-133">동유럽</span><span class="sxs-lookup"><span data-stu-id="e5859-133">North Europe</span></span>
- <span data-ttu-id="e5859-134">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="e5859-134">South Central US</span></span>
- <span data-ttu-id="e5859-135">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="e5859-135">Southeast Asia</span></span>
- <span data-ttu-id="e5859-136">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="e5859-136">West Europe</span></span>
- <span data-ttu-id="e5859-137">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="e5859-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5859-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="e5859-138">-MaxJobCount</span></span>
<span data-ttu-id="e5859-139">스케줄러 작업 컬렉션에서 만들 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5859-140">-계획</span><span class="sxs-lookup"><span data-stu-id="e5859-140">-Plan</span></span>
<span data-ttu-id="e5859-141">스케줄러 작업 컬렉션 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="e5859-142">-프로필</span><span class="sxs-lookup"><span data-stu-id="e5859-142">-Profile</span></span>
<span data-ttu-id="e5859-143">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5859-144">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5859-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5859-145">CommonParameters</span></span>
<span data-ttu-id="e5859-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5859-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5859-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5859-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5859-148">입력</span><span class="sxs-lookup"><span data-stu-id="e5859-148">INPUTS</span></span>

## <span data-ttu-id="e5859-149">출력</span><span class="sxs-lookup"><span data-stu-id="e5859-149">OUTPUTS</span></span>

## <span data-ttu-id="e5859-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e5859-150">NOTES</span></span>

## <span data-ttu-id="e5859-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5859-151">RELATED LINKS</span></span>

[<span data-ttu-id="e5859-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e5859-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="e5859-153">제거-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e5859-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="e5859-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e5859-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)



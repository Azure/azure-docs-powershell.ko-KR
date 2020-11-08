---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045443"
---
# <span data-ttu-id="0c931-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0c931-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="0c931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c931-102">SYNOPSIS</span></span>
<span data-ttu-id="0c931-103">스케줄러 작업 컬렉션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="0c931-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c931-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c931-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c931-105">DESCRIPTION</span></span>
<span data-ttu-id="0c931-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0c931-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0c931-108">**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 컬렉션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="0c931-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c931-109">EXAMPLES</span></span>

### <span data-ttu-id="0c931-110">예제 1: 컬렉션의 최대 작업 수 변경</span><span class="sxs-lookup"><span data-stu-id="0c931-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="0c931-111">이 명령은 JobCollection01 이라는 기존 스케줄러 작업 컬렉션에서 최대 작업 수를 30으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="0c931-112">변수</span><span class="sxs-lookup"><span data-stu-id="0c931-112">PARAMETERS</span></span>

### <span data-ttu-id="0c931-113">-빈도</span><span class="sxs-lookup"><span data-stu-id="0c931-113">-Frequency</span></span>
<span data-ttu-id="0c931-114">이 스케줄러 작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="0c931-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c931-116">길이의</span><span class="sxs-lookup"><span data-stu-id="0c931-116">Minute</span></span>
- <span data-ttu-id="0c931-117">시간씩</span><span class="sxs-lookup"><span data-stu-id="0c931-117">Hour</span></span>
- <span data-ttu-id="0c931-118">부활절</span><span class="sxs-lookup"><span data-stu-id="0c931-118">Day</span></span>
- <span data-ttu-id="0c931-119">이번</span><span class="sxs-lookup"><span data-stu-id="0c931-119">Week</span></span>
- <span data-ttu-id="0c931-120">달은</span><span class="sxs-lookup"><span data-stu-id="0c931-120">Month</span></span>
- <span data-ttu-id="0c931-121">반기</span><span class="sxs-lookup"><span data-stu-id="0c931-121">Year</span></span>

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

### <span data-ttu-id="0c931-122">-Interval</span><span class="sxs-lookup"><span data-stu-id="0c931-122">-Interval</span></span>
<span data-ttu-id="0c931-123">*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="0c931-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0c931-124">-JobCollectionName</span></span>
<span data-ttu-id="0c931-125">업데이트할 스케줄러 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="0c931-126">-위치</span><span class="sxs-lookup"><span data-stu-id="0c931-126">-Location</span></span>
<span data-ttu-id="0c931-127">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="0c931-128">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-128">Valid values are:</span></span> 

- <span data-ttu-id="0c931-129">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="0c931-129">Anywhere Asia</span></span>
- <span data-ttu-id="0c931-130">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="0c931-130">Anywhere Europe</span></span>
- <span data-ttu-id="0c931-131">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="0c931-131">Anywhere US</span></span>
- <span data-ttu-id="0c931-132">동아시아</span><span class="sxs-lookup"><span data-stu-id="0c931-132">East Asia</span></span>
- <span data-ttu-id="0c931-133">미국 동부</span><span class="sxs-lookup"><span data-stu-id="0c931-133">East US</span></span>
- <span data-ttu-id="0c931-134">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="0c931-134">North Central US</span></span>
- <span data-ttu-id="0c931-135">동유럽</span><span class="sxs-lookup"><span data-stu-id="0c931-135">North Europe</span></span>
- <span data-ttu-id="0c931-136">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="0c931-136">South Central US</span></span>
- <span data-ttu-id="0c931-137">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="0c931-137">Southeast Asia</span></span>
- <span data-ttu-id="0c931-138">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="0c931-138">West Europe</span></span>
- <span data-ttu-id="0c931-139">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="0c931-139">West US</span></span>

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

### <span data-ttu-id="0c931-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="0c931-140">-MaxJobCount</span></span>
<span data-ttu-id="0c931-141">스케줄러 작업 컬렉션에서 만들 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="0c931-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c931-142">-PassThru</span></span>
<span data-ttu-id="0c931-143">이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="0c931-144">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c931-145">-계획</span><span class="sxs-lookup"><span data-stu-id="0c931-145">-Plan</span></span>
<span data-ttu-id="0c931-146">스케줄러 작업 컬렉션 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="0c931-147">-프로필</span><span class="sxs-lookup"><span data-stu-id="0c931-147">-Profile</span></span>
<span data-ttu-id="0c931-148">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c931-149">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c931-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c931-150">CommonParameters</span></span>
<span data-ttu-id="0c931-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c931-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c931-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c931-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c931-153">입력</span><span class="sxs-lookup"><span data-stu-id="0c931-153">INPUTS</span></span>

## <span data-ttu-id="0c931-154">출력</span><span class="sxs-lookup"><span data-stu-id="0c931-154">OUTPUTS</span></span>

## <span data-ttu-id="0c931-155">상속자</span><span class="sxs-lookup"><span data-stu-id="0c931-155">NOTES</span></span>

## <span data-ttu-id="0c931-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c931-156">RELATED LINKS</span></span>

[<span data-ttu-id="0c931-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0c931-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0c931-158">새로운 AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0c931-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0c931-159">제거-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0c931-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)



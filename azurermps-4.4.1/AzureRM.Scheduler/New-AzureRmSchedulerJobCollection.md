---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533856"
---
# <span data-ttu-id="d469d-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d469d-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d469d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d469d-102">SYNOPSIS</span></span>
<span data-ttu-id="d469d-103">작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d469d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d469d-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d469d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d469d-105">DESCRIPTION</span></span>
<span data-ttu-id="d469d-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler에서 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d469d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d469d-107">EXAMPLES</span></span>

## <span data-ttu-id="d469d-108">변수</span><span class="sxs-lookup"><span data-stu-id="d469d-108">PARAMETERS</span></span>

### <span data-ttu-id="d469d-109">-빈도</span><span class="sxs-lookup"><span data-stu-id="d469d-109">-Frequency</span></span>
<span data-ttu-id="d469d-110">작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="d469d-111">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d469d-112">길이의</span><span class="sxs-lookup"><span data-stu-id="d469d-112">Minute</span></span> 
- <span data-ttu-id="d469d-113">시간씩</span><span class="sxs-lookup"><span data-stu-id="d469d-113">Hour</span></span> 
- <span data-ttu-id="d469d-114">부활절</span><span class="sxs-lookup"><span data-stu-id="d469d-114">Day</span></span> 
- <span data-ttu-id="d469d-115">이번</span><span class="sxs-lookup"><span data-stu-id="d469d-115">Week</span></span> 
- <span data-ttu-id="d469d-116">달은</span><span class="sxs-lookup"><span data-stu-id="d469d-116">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-117">-Interval</span><span class="sxs-lookup"><span data-stu-id="d469d-117">-Interval</span></span>
<span data-ttu-id="d469d-118">되풀이의 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-118">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d469d-119">-JobCollectionName</span></span>
<span data-ttu-id="d469d-120">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-120">Specifies a name for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-121">-위치</span><span class="sxs-lookup"><span data-stu-id="d469d-121">-Location</span></span>
<span data-ttu-id="d469d-122">이 cmdlet이 작업 컬렉션을 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d469d-123">-MaxJobCount</span></span>
<span data-ttu-id="d469d-124">작업 컬렉션에서 만들 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="d469d-125">Maximum은 *계획* 매개 변수에서 지정 하는 계획에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-126">-계획</span><span class="sxs-lookup"><span data-stu-id="d469d-126">-Plan</span></span>
<span data-ttu-id="d469d-127">작업 컬렉션 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="d469d-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d469d-129">비우거나</span><span class="sxs-lookup"><span data-stu-id="d469d-129">Free</span></span> 
- <span data-ttu-id="d469d-130">표준이</span><span class="sxs-lookup"><span data-stu-id="d469d-130">Standard</span></span> 
- <span data-ttu-id="d469d-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="d469d-131">P10Premium</span></span> 
- <span data-ttu-id="d469d-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="d469d-132">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d469d-133">-ResourceGroupName</span></span>
<span data-ttu-id="d469d-134">작업 컬렉션에 대 한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-134">Specifies the resource group for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="d469d-135">-Confirm</span></span>
<span data-ttu-id="d469d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d469d-137">-WhatIf</span></span>
<span data-ttu-id="d469d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d469d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d469d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d469d-140">-DefaultProfile</span></span>
<span data-ttu-id="d469d-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d469d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d469d-142">CommonParameters</span></span>
<span data-ttu-id="d469d-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d469d-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d469d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d469d-145">입력</span><span class="sxs-lookup"><span data-stu-id="d469d-145">INPUTS</span></span>

## <span data-ttu-id="d469d-146">출력</span><span class="sxs-lookup"><span data-stu-id="d469d-146">OUTPUTS</span></span>

### <span data-ttu-id="d469d-147">PSJobCollectionDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="d469d-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="d469d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="d469d-148">NOTES</span></span>

## <span data-ttu-id="d469d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d469d-149">RELATED LINKS</span></span>

[<span data-ttu-id="d469d-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d469d-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d469d-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d469d-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d469d-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d469d-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d469d-153">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d469d-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d469d-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d469d-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)



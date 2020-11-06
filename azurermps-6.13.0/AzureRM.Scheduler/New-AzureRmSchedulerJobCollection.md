---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 479b91f222852ebfc356d320cf880eb2ae99db6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528402"
---
# <span data-ttu-id="9696c-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9696c-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="9696c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9696c-102">SYNOPSIS</span></span>
<span data-ttu-id="9696c-103">작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9696c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9696c-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9696c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9696c-105">DESCRIPTION</span></span>
<span data-ttu-id="9696c-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler에서 작업 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="9696c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9696c-107">EXAMPLES</span></span>

## <span data-ttu-id="9696c-108">변수</span><span class="sxs-lookup"><span data-stu-id="9696c-108">PARAMETERS</span></span>

### <span data-ttu-id="9696c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9696c-109">-DefaultProfile</span></span>
<span data-ttu-id="9696c-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9696c-111">-빈도</span><span class="sxs-lookup"><span data-stu-id="9696c-111">-Frequency</span></span>
<span data-ttu-id="9696c-112">작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="9696c-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9696c-114">길이의</span><span class="sxs-lookup"><span data-stu-id="9696c-114">Minute</span></span> 
- <span data-ttu-id="9696c-115">시간씩</span><span class="sxs-lookup"><span data-stu-id="9696c-115">Hour</span></span> 
- <span data-ttu-id="9696c-116">부활절</span><span class="sxs-lookup"><span data-stu-id="9696c-116">Day</span></span> 
- <span data-ttu-id="9696c-117">이번</span><span class="sxs-lookup"><span data-stu-id="9696c-117">Week</span></span> 
- <span data-ttu-id="9696c-118">달은</span><span class="sxs-lookup"><span data-stu-id="9696c-118">Month</span></span>

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

### <span data-ttu-id="9696c-119">-Interval</span><span class="sxs-lookup"><span data-stu-id="9696c-119">-Interval</span></span>
<span data-ttu-id="9696c-120">되풀이의 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="9696c-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9696c-121">-JobCollectionName</span></span>
<span data-ttu-id="9696c-122">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-122">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="9696c-123">-위치</span><span class="sxs-lookup"><span data-stu-id="9696c-123">-Location</span></span>
<span data-ttu-id="9696c-124">이 cmdlet이 작업 컬렉션을 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="9696c-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="9696c-125">-MaxJobCount</span></span>
<span data-ttu-id="9696c-126">작업 컬렉션에서 만들 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="9696c-127">Maximum은 *계획* 매개 변수에서 지정 하는 계획에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="9696c-128">-계획</span><span class="sxs-lookup"><span data-stu-id="9696c-128">-Plan</span></span>
<span data-ttu-id="9696c-129">작업 컬렉션 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="9696c-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9696c-131">비우거나</span><span class="sxs-lookup"><span data-stu-id="9696c-131">Free</span></span> 
- <span data-ttu-id="9696c-132">표준이</span><span class="sxs-lookup"><span data-stu-id="9696c-132">Standard</span></span> 
- <span data-ttu-id="9696c-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="9696c-133">P10Premium</span></span> 
- <span data-ttu-id="9696c-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="9696c-134">P20Premium</span></span>

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

### <span data-ttu-id="9696c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9696c-135">-ResourceGroupName</span></span>
<span data-ttu-id="9696c-136">작업 컬렉션에 대 한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-136">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="9696c-137">-확인</span><span class="sxs-lookup"><span data-stu-id="9696c-137">-Confirm</span></span>
<span data-ttu-id="9696c-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9696c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9696c-139">-WhatIf</span></span>
<span data-ttu-id="9696c-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9696c-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9696c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9696c-142">CommonParameters</span></span>
<span data-ttu-id="9696c-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9696c-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9696c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9696c-145">입력</span><span class="sxs-lookup"><span data-stu-id="9696c-145">INPUTS</span></span>

### <span data-ttu-id="9696c-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9696c-146">System.String</span></span>

## <span data-ttu-id="9696c-147">출력</span><span class="sxs-lookup"><span data-stu-id="9696c-147">OUTPUTS</span></span>

### <span data-ttu-id="9696c-148">PSJobCollectionDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="9696c-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="9696c-149">상속자</span><span class="sxs-lookup"><span data-stu-id="9696c-149">NOTES</span></span>

## <span data-ttu-id="9696c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9696c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9696c-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9696c-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9696c-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9696c-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9696c-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9696c-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9696c-154">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9696c-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9696c-155">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9696c-155">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)



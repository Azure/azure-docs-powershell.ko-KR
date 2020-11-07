---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 141a91272e805cc30f290d544a9a33c7c81484e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703619"
---
# <span data-ttu-id="bba0e-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bba0e-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="bba0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba0e-102">SYNOPSIS</span></span>
<span data-ttu-id="bba0e-103">작업 컬렉션을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bba0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bba0e-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bba0e-105">DESCRIPTION</span></span>
<span data-ttu-id="bba0e-106">**Set-AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler의 작업 컬렉션을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="bba0e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bba0e-107">EXAMPLES</span></span>

## <span data-ttu-id="bba0e-108">변수</span><span class="sxs-lookup"><span data-stu-id="bba0e-108">PARAMETERS</span></span>

### <span data-ttu-id="bba0e-109">-빈도</span><span class="sxs-lookup"><span data-stu-id="bba0e-109">-Frequency</span></span>
<span data-ttu-id="bba0e-110">작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="bba0e-111">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bba0e-112">길이의</span><span class="sxs-lookup"><span data-stu-id="bba0e-112">Minute</span></span> 
- <span data-ttu-id="bba0e-113">시간씩</span><span class="sxs-lookup"><span data-stu-id="bba0e-113">Hour</span></span> 
- <span data-ttu-id="bba0e-114">부활절</span><span class="sxs-lookup"><span data-stu-id="bba0e-114">Day</span></span> 
- <span data-ttu-id="bba0e-115">이번</span><span class="sxs-lookup"><span data-stu-id="bba0e-115">Week</span></span> 
- <span data-ttu-id="bba0e-116">달은</span><span class="sxs-lookup"><span data-stu-id="bba0e-116">Month</span></span>

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

### <span data-ttu-id="bba0e-117">-Interval</span><span class="sxs-lookup"><span data-stu-id="bba0e-117">-Interval</span></span>
<span data-ttu-id="bba0e-118">되풀이의 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="bba0e-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bba0e-119">-JobCollectionName</span></span>
<span data-ttu-id="bba0e-120">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-120">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="bba0e-121">-위치</span><span class="sxs-lookup"><span data-stu-id="bba0e-121">-Location</span></span>
<span data-ttu-id="bba0e-122">작업 컬렉션이 있는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-122">Specifies the Azure region in which the job collection exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba0e-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="bba0e-123">-MaxJobCount</span></span>
<span data-ttu-id="bba0e-124">작업 컬렉션에서 만들 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="bba0e-125">Maximum은 *계획* 매개 변수에서 지정 하는 계획에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="bba0e-126">-계획</span><span class="sxs-lookup"><span data-stu-id="bba0e-126">-Plan</span></span>
<span data-ttu-id="bba0e-127">작업 컬렉션 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="bba0e-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bba0e-129">비우거나</span><span class="sxs-lookup"><span data-stu-id="bba0e-129">Free</span></span> 
- <span data-ttu-id="bba0e-130">표준이</span><span class="sxs-lookup"><span data-stu-id="bba0e-130">Standard</span></span> 
- <span data-ttu-id="bba0e-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="bba0e-131">P10Premium</span></span> 
- <span data-ttu-id="bba0e-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="bba0e-132">P20Premium</span></span>

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

### <span data-ttu-id="bba0e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba0e-133">-ResourceGroupName</span></span>
<span data-ttu-id="bba0e-134">작업 컬렉션의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-134">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="bba0e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="bba0e-135">-Confirm</span></span>
<span data-ttu-id="bba0e-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba0e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba0e-137">-WhatIf</span></span>
<span data-ttu-id="bba0e-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba0e-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba0e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba0e-140">-DefaultProfile</span></span>
<span data-ttu-id="bba0e-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bba0e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba0e-142">CommonParameters</span></span>
<span data-ttu-id="bba0e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba0e-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba0e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba0e-145">입력</span><span class="sxs-lookup"><span data-stu-id="bba0e-145">INPUTS</span></span>

## <span data-ttu-id="bba0e-146">출력</span><span class="sxs-lookup"><span data-stu-id="bba0e-146">OUTPUTS</span></span>

### <span data-ttu-id="bba0e-147">PSJobCollectionDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="bba0e-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="bba0e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="bba0e-148">NOTES</span></span>

## <span data-ttu-id="bba0e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bba0e-149">RELATED LINKS</span></span>

[<span data-ttu-id="bba0e-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bba0e-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bba0e-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bba0e-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bba0e-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bba0e-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bba0e-153">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bba0e-153">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bba0e-154">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bba0e-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)



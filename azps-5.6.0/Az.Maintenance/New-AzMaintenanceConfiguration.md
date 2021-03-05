---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: ac264e048ea428ba68caa683eb6076074c9894b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985992"
---
# <span data-ttu-id="b22d8-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b22d8-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="b22d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b22d8-103">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="b22d8-103">Create or Update configuration record</span></span>

## <span data-ttu-id="b22d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="b22d8-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b22d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="b22d8-105">DESCRIPTION</span></span>
<span data-ttu-id="b22d8-106">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="b22d8-106">Create or Update configuration record</span></span>

## <span data-ttu-id="b22d8-107">예제</span><span class="sxs-lookup"><span data-stu-id="b22d8-107">EXAMPLES</span></span>

### <span data-ttu-id="b22d8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b22d8-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="b22d8-109">범위 호스트를 사용하여 유지 관리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="b22d8-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="b22d8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b22d8-110">PARAMETERS</span></span>

### <span data-ttu-id="b22d8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b22d8-111">-AsJob</span></span>
<span data-ttu-id="b22d8-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b22d8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22d8-113">-DefaultProfile</span></span>
<span data-ttu-id="b22d8-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-115">-기간</span><span class="sxs-lookup"><span data-stu-id="b22d8-115">-Duration</span></span>
<span data-ttu-id="b22d8-116">기간</span><span class="sxs-lookup"><span data-stu-id="b22d8-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="b22d8-117">-ExpirationDateTime</span></span>
<span data-ttu-id="b22d8-118">YYYY-MM-DD 형식의 일정의 expirationDateTime hh:mm</span><span class="sxs-lookup"><span data-stu-id="b22d8-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="b22d8-119">-ExtensionProperty</span></span>
<span data-ttu-id="b22d8-120">리소스당 확장 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-120">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b22d8-121">-Location</span></span>
<span data-ttu-id="b22d8-122">유지 관리 구성 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-122">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="b22d8-123">-MaintenanceScope</span></span>
<span data-ttu-id="b22d8-124">유지 관리 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-124">The Maintenance Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b22d8-125">-Name</span></span>
<span data-ttu-id="b22d8-126">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-126">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="b22d8-127">-RecurEvery</span></span>
<span data-ttu-id="b22d8-128">일정 재발</span><span class="sxs-lookup"><span data-stu-id="b22d8-128">The schedule recurrence</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="b22d8-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-130">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b22d8-131">-StartDateTime</span></span>
<span data-ttu-id="b22d8-132">YYYY-MM-DD 형식의 일정의 StartDateTime hh:mm</span><span class="sxs-lookup"><span data-stu-id="b22d8-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b22d8-133">-Tag</span></span>
<span data-ttu-id="b22d8-134">ARM 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-134">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="b22d8-135">-Timezone</span></span>
<span data-ttu-id="b22d8-136">타임존</span><span class="sxs-lookup"><span data-stu-id="b22d8-136">The timezone</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-137">-가시성</span><span class="sxs-lookup"><span data-stu-id="b22d8-137">-Visibility</span></span>
<span data-ttu-id="b22d8-138">범위의 가시성</span><span class="sxs-lookup"><span data-stu-id="b22d8-138">The visibility of the scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-139">-확인</span><span class="sxs-lookup"><span data-stu-id="b22d8-139">-Confirm</span></span>
<span data-ttu-id="b22d8-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22d8-141">-WhatIf</span></span>
<span data-ttu-id="b22d8-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22d8-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22d8-144">CommonParameters</span></span>
<span data-ttu-id="b22d8-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b22d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22d8-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b22d8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22d8-147">입력</span><span class="sxs-lookup"><span data-stu-id="b22d8-147">INPUTS</span></span>

### <span data-ttu-id="b22d8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b22d8-148">System.String</span></span>

## <span data-ttu-id="b22d8-149">출력</span><span class="sxs-lookup"><span data-stu-id="b22d8-149">OUTPUTS</span></span>

### <span data-ttu-id="b22d8-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b22d8-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="b22d8-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b22d8-151">NOTES</span></span>

## <span data-ttu-id="b22d8-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b22d8-152">RELATED LINKS</span></span>

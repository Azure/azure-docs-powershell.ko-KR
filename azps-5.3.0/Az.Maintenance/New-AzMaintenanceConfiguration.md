---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493410"
---
# <span data-ttu-id="d8674-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8674-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="d8674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8674-102">SYNOPSIS</span></span>
<span data-ttu-id="d8674-103">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d8674-103">Create or Update configuration record</span></span>

## <span data-ttu-id="d8674-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8674-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8674-105">설명</span><span class="sxs-lookup"><span data-stu-id="d8674-105">DESCRIPTION</span></span>
<span data-ttu-id="d8674-106">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d8674-106">Create or Update configuration record</span></span>

## <span data-ttu-id="d8674-107">예제</span><span class="sxs-lookup"><span data-stu-id="d8674-107">EXAMPLES</span></span>

### <span data-ttu-id="d8674-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8674-108">Example 1</span></span>
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

<span data-ttu-id="d8674-109">범위 호스트를 사용하여 유지 관리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="d8674-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="d8674-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8674-110">PARAMETERS</span></span>

### <span data-ttu-id="d8674-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8674-111">-AsJob</span></span>
<span data-ttu-id="d8674-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8674-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8674-113">-DefaultProfile</span></span>
<span data-ttu-id="d8674-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8674-115">-Duration</span><span class="sxs-lookup"><span data-stu-id="d8674-115">-Duration</span></span>
<span data-ttu-id="d8674-116">기간</span><span class="sxs-lookup"><span data-stu-id="d8674-116">The duration</span></span>


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

### <span data-ttu-id="d8674-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d8674-117">-ExpirationDateTime</span></span>
<span data-ttu-id="d8674-118">YYYY-MM-DD hh:mm 형식의 schedule의 expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d8674-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="d8674-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="d8674-119">-ExtensionProperty</span></span>
<span data-ttu-id="d8674-120">리소스당 확장 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="d8674-121">-Location</span><span class="sxs-lookup"><span data-stu-id="d8674-121">-Location</span></span>
<span data-ttu-id="d8674-122">유지 관리 구성 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="d8674-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="d8674-123">-MaintenanceScope</span></span>
<span data-ttu-id="d8674-124">유지 관리 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="d8674-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d8674-125">-Name</span></span>
<span data-ttu-id="d8674-126">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="d8674-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="d8674-127">-RecurEvery</span></span>
<span data-ttu-id="d8674-128">일정 재발</span><span class="sxs-lookup"><span data-stu-id="d8674-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="d8674-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8674-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8674-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="d8674-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d8674-131">-StartDateTime</span></span>
<span data-ttu-id="d8674-132">YYYY-MM-DD hh:mm 형식의 일정의 StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d8674-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="d8674-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8674-133">-Tag</span></span>
<span data-ttu-id="d8674-134">ARM 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="d8674-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="d8674-135">-Timezone</span></span>
<span data-ttu-id="d8674-136">Timezone</span><span class="sxs-lookup"><span data-stu-id="d8674-136">The timezone</span></span>

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

### <span data-ttu-id="d8674-137">-Visibility</span><span class="sxs-lookup"><span data-stu-id="d8674-137">-Visibility</span></span>
<span data-ttu-id="d8674-138">범위의 표시 여부</span><span class="sxs-lookup"><span data-stu-id="d8674-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="d8674-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8674-139">-Confirm</span></span>
<span data-ttu-id="d8674-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8674-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8674-141">-WhatIf</span></span>
<span data-ttu-id="d8674-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d8674-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8674-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8674-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8674-144">CommonParameters</span></span>
<span data-ttu-id="d8674-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8674-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8674-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8674-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8674-147">입력</span><span class="sxs-lookup"><span data-stu-id="d8674-147">INPUTS</span></span>

### <span data-ttu-id="d8674-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d8674-148">System.String</span></span>

## <span data-ttu-id="d8674-149">출력</span><span class="sxs-lookup"><span data-stu-id="d8674-149">OUTPUTS</span></span>

### <span data-ttu-id="d8674-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8674-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="d8674-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8674-151">NOTES</span></span>

## <span data-ttu-id="d8674-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8674-152">RELATED LINKS</span></span>

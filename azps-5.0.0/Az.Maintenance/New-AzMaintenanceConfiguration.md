---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217698"
---
# <span data-ttu-id="7b6fc-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b6fc-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="7b6fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6fc-103">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="7b6fc-103">Create or Update configuration record</span></span>

## <span data-ttu-id="7b6fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b6fc-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b6fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6fc-106">구성 레코드 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="7b6fc-106">Create or Update configuration record</span></span>

## <span data-ttu-id="7b6fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7b6fc-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6fc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b6fc-108">Example 1</span></span>
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

<span data-ttu-id="7b6fc-109">범위 호스트를 사용 하 여 유지 관리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="7b6fc-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="7b6fc-110">변수</span><span class="sxs-lookup"><span data-stu-id="7b6fc-110">PARAMETERS</span></span>

### <span data-ttu-id="7b6fc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b6fc-111">-AsJob</span></span>
<span data-ttu-id="7b6fc-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7b6fc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b6fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6fc-113">-DefaultProfile</span></span>
<span data-ttu-id="7b6fc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b6fc-115">-기간</span><span class="sxs-lookup"><span data-stu-id="7b6fc-115">-Duration</span></span>
<span data-ttu-id="7b6fc-116">기간</span><span class="sxs-lookup"><span data-stu-id="7b6fc-116">The duration</span></span>


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

### <span data-ttu-id="7b6fc-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="7b6fc-117">-ExpirationDateTime</span></span>
<span data-ttu-id="7b6fc-118">YYYY-MM-DD hh: MM 형식으로 된 일정의 expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="7b6fc-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="7b6fc-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="7b6fc-119">-ExtensionProperty</span></span>
<span data-ttu-id="7b6fc-120">Resource 당 확장 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="7b6fc-121">-위치</span><span class="sxs-lookup"><span data-stu-id="7b6fc-121">-Location</span></span>
<span data-ttu-id="7b6fc-122">유지 관리 구성 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="7b6fc-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="7b6fc-123">-MaintenanceScope</span></span>
<span data-ttu-id="7b6fc-124">유지 관리 범위</span><span class="sxs-lookup"><span data-stu-id="7b6fc-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="7b6fc-125">-이름</span><span class="sxs-lookup"><span data-stu-id="7b6fc-125">-Name</span></span>
<span data-ttu-id="7b6fc-126">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="7b6fc-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="7b6fc-127">-RecurEvery</span></span>
<span data-ttu-id="7b6fc-128">일정 되풀이</span><span class="sxs-lookup"><span data-stu-id="7b6fc-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="7b6fc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6fc-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b6fc-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="7b6fc-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="7b6fc-131">-StartDateTime</span></span>
<span data-ttu-id="7b6fc-132">YYYY-MM-DD hh: MM 형식으로 된 일정의 StartDateTime</span><span class="sxs-lookup"><span data-stu-id="7b6fc-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="7b6fc-133">태그</span><span class="sxs-lookup"><span data-stu-id="7b6fc-133">-Tag</span></span>
<span data-ttu-id="7b6fc-134">ARM 태그.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="7b6fc-135">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="7b6fc-135">-Timezone</span></span>
<span data-ttu-id="7b6fc-136">표준 시간대</span><span class="sxs-lookup"><span data-stu-id="7b6fc-136">The timezone</span></span>

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

### <span data-ttu-id="7b6fc-137">-표시 유형</span><span class="sxs-lookup"><span data-stu-id="7b6fc-137">-Visibility</span></span>
<span data-ttu-id="7b6fc-138">범위의 표시 여부</span><span class="sxs-lookup"><span data-stu-id="7b6fc-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="7b6fc-139">-확인</span><span class="sxs-lookup"><span data-stu-id="7b6fc-139">-Confirm</span></span>
<span data-ttu-id="7b6fc-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b6fc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6fc-141">-WhatIf</span></span>
<span data-ttu-id="7b6fc-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b6fc-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b6fc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6fc-144">CommonParameters</span></span>
<span data-ttu-id="7b6fc-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6fc-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b6fc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6fc-147">입력</span><span class="sxs-lookup"><span data-stu-id="7b6fc-147">INPUTS</span></span>

### <span data-ttu-id="7b6fc-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b6fc-148">System.String</span></span>

## <span data-ttu-id="7b6fc-149">출력</span><span class="sxs-lookup"><span data-stu-id="7b6fc-149">OUTPUTS</span></span>

### <span data-ttu-id="7b6fc-150">PSMaintenanceConfiguration/. m m</span><span class="sxs-lookup"><span data-stu-id="7b6fc-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="7b6fc-151">상속자</span><span class="sxs-lookup"><span data-stu-id="7b6fc-151">NOTES</span></span>

## <span data-ttu-id="7b6fc-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b6fc-152">RELATED LINKS</span></span>

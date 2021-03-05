---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 38292351f091528ef4e153f9374dff75ccbfe941
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966155"
---
# <span data-ttu-id="7d728-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="7d728-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="7d728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d728-102">SYNOPSIS</span></span>
<span data-ttu-id="7d728-103">applicationGroup을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="7d728-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d728-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7d728-105">설명</span><span class="sxs-lookup"><span data-stu-id="7d728-105">DESCRIPTION</span></span>
<span data-ttu-id="7d728-106">applicationGroup을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="7d728-107">예제</span><span class="sxs-lookup"><span data-stu-id="7d728-107">EXAMPLES</span></span>

### <span data-ttu-id="7d728-108">예제 1: 이름에 따라 Windows Virtual Desktop ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="7d728-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="7d728-109">이 명령은 리소스 그룹에 Windows Virtual Desktop ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="7d728-110">예제 2: 이름에 따라 Windows Virtual Desktop ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="7d728-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="7d728-111">이 명령은 리소스 그룹에 Windows Virtual Desktop ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="7d728-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d728-112">PARAMETERS</span></span>

### <span data-ttu-id="7d728-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="7d728-113">-ApplicationGroupType</span></span>
<span data-ttu-id="7d728-114">ApplicationGroup의 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d728-115">-DefaultProfile</span></span>
<span data-ttu-id="7d728-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-117">-Description</span><span class="sxs-lookup"><span data-stu-id="7d728-117">-Description</span></span>
<span data-ttu-id="7d728-118">ApplicationGroup에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="7d728-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d728-119">-FriendlyName</span></span>
<span data-ttu-id="7d728-120">ApplicationGroup의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="7d728-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="7d728-121">-HostPoolArmPath</span></span>
<span data-ttu-id="7d728-122">ApplicationGroup의 HostPool 암 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-122">HostPool arm path of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-123">-Location</span><span class="sxs-lookup"><span data-stu-id="7d728-123">-Location</span></span>
<span data-ttu-id="7d728-124">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="7d728-124">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7d728-125">-Name</span></span>
<span data-ttu-id="7d728-126">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="7d728-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d728-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d728-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-128">The name of the resource group.</span></span>
<span data-ttu-id="7d728-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d728-130">-SubscriptionId</span></span>
<span data-ttu-id="7d728-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d728-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d728-132">-Tag</span></span>
<span data-ttu-id="7d728-133">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-133">Resource tags.</span></span>

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

### <span data-ttu-id="7d728-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7d728-134">-Confirm</span></span>
<span data-ttu-id="7d728-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d728-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d728-136">-WhatIf</span></span>
<span data-ttu-id="7d728-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d728-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d728-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d728-139">CommonParameters</span></span>
<span data-ttu-id="7d728-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d728-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d728-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d728-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d728-142">입력</span><span class="sxs-lookup"><span data-stu-id="7d728-142">INPUTS</span></span>

## <span data-ttu-id="7d728-143">출력</span><span class="sxs-lookup"><span data-stu-id="7d728-143">OUTPUTS</span></span>

### <span data-ttu-id="7d728-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="7d728-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="7d728-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d728-145">NOTES</span></span>

<span data-ttu-id="7d728-146">별칭</span><span class="sxs-lookup"><span data-stu-id="7d728-146">ALIASES</span></span>

## <span data-ttu-id="7d728-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d728-147">RELATED LINKS</span></span>


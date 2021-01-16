---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 6cfee237c1104a77f0e1790c4980e8eb793a771c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341409"
---
# <span data-ttu-id="bd79b-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bd79b-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="bd79b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd79b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd79b-103">applicationGroup을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="bd79b-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd79b-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd79b-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd79b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd79b-106">applicationGroup을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="bd79b-107">예제</span><span class="sxs-lookup"><span data-stu-id="bd79b-107">EXAMPLES</span></span>

### <span data-ttu-id="bd79b-108">예제 1: 이름으로 Windows Virtual Desktop ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="bd79b-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="bd79b-109">이 명령은 리소스 그룹에 Windows Virtual Desktop ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="bd79b-110">예제 2: 이름으로 Windows Virtual Desktop ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="bd79b-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="bd79b-111">이 명령은 리소스 그룹에 Windows Virtual Desktop ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="bd79b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd79b-112">PARAMETERS</span></span>

### <span data-ttu-id="bd79b-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="bd79b-113">-ApplicationGroupType</span></span>
<span data-ttu-id="bd79b-114">ApplicationGroup의 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bd79b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd79b-115">-DefaultProfile</span></span>
<span data-ttu-id="bd79b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd79b-117">-Description</span><span class="sxs-lookup"><span data-stu-id="bd79b-117">-Description</span></span>
<span data-ttu-id="bd79b-118">ApplicationGroup에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bd79b-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bd79b-119">-FriendlyName</span></span>
<span data-ttu-id="bd79b-120">ApplicationGroup의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bd79b-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="bd79b-121">-HostPoolArmPath</span></span>
<span data-ttu-id="bd79b-122">ApplicationGroup의 HostPool arm 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bd79b-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bd79b-123">-Location</span></span>
<span data-ttu-id="bd79b-124">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="bd79b-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="bd79b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bd79b-125">-Name</span></span>
<span data-ttu-id="bd79b-126">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="bd79b-126">The name of the application group</span></span>

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

### <span data-ttu-id="bd79b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd79b-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd79b-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-128">The name of the resource group.</span></span>
<span data-ttu-id="bd79b-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd79b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd79b-130">-SubscriptionId</span></span>
<span data-ttu-id="bd79b-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd79b-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd79b-132">-Tag</span></span>
<span data-ttu-id="bd79b-133">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="bd79b-133">Resource tags.</span></span>

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

### <span data-ttu-id="bd79b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd79b-134">-Confirm</span></span>
<span data-ttu-id="bd79b-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd79b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd79b-136">-WhatIf</span></span>
<span data-ttu-id="bd79b-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd79b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd79b-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd79b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd79b-139">CommonParameters</span></span>
<span data-ttu-id="bd79b-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd79b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd79b-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd79b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd79b-142">입력</span><span class="sxs-lookup"><span data-stu-id="bd79b-142">INPUTS</span></span>

## <span data-ttu-id="bd79b-143">출력</span><span class="sxs-lookup"><span data-stu-id="bd79b-143">OUTPUTS</span></span>

### <span data-ttu-id="bd79b-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bd79b-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="bd79b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd79b-145">NOTES</span></span>

<span data-ttu-id="bd79b-146">별칭</span><span class="sxs-lookup"><span data-stu-id="bd79b-146">ALIASES</span></span>

## <span data-ttu-id="bd79b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd79b-147">RELATED LINKS</span></span>


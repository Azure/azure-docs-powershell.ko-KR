---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304796"
---
# <span data-ttu-id="4117d-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4117d-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4117d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4117d-102">SYNOPSIS</span></span>
<span data-ttu-id="4117d-103">ApplicationGroup을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="4117d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4117d-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4117d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4117d-105">DESCRIPTION</span></span>
<span data-ttu-id="4117d-106">ApplicationGroup을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="4117d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4117d-107">EXAMPLES</span></span>

### <span data-ttu-id="4117d-108">예제 1: 이름별로 Windows 가상 데스크톱 ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="4117d-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="4117d-109">이 명령은 리소스 그룹에 Windows 가상 데스크톱 ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="4117d-110">예제 2: 이름별로 Windows 가상 데스크톱 ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="4117d-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="4117d-111">이 명령은 리소스 그룹에 Windows 가상 데스크톱 ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="4117d-112">변수</span><span class="sxs-lookup"><span data-stu-id="4117d-112">PARAMETERS</span></span>

### <span data-ttu-id="4117d-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="4117d-113">-ApplicationGroupType</span></span>
<span data-ttu-id="4117d-114">ApplicationGroup의 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4117d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4117d-115">-DefaultProfile</span></span>
<span data-ttu-id="4117d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4117d-117">-설명</span><span class="sxs-lookup"><span data-stu-id="4117d-117">-Description</span></span>
<span data-ttu-id="4117d-118">ApplicationGroup에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4117d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4117d-119">-FriendlyName</span></span>
<span data-ttu-id="4117d-120">ApplicationGroup의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4117d-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="4117d-121">-HostPoolArmPath</span></span>
<span data-ttu-id="4117d-122">ApplicationGroup의 HostPool 팔 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4117d-123">-위치</span><span class="sxs-lookup"><span data-stu-id="4117d-123">-Location</span></span>
<span data-ttu-id="4117d-124">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="4117d-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="4117d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4117d-125">-Name</span></span>
<span data-ttu-id="4117d-126">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-126">The name of the application group</span></span>

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

### <span data-ttu-id="4117d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4117d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4117d-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-128">The name of the resource group.</span></span>
<span data-ttu-id="4117d-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4117d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4117d-130">-SubscriptionId</span></span>
<span data-ttu-id="4117d-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4117d-132">태그</span><span class="sxs-lookup"><span data-stu-id="4117d-132">-Tag</span></span>
<span data-ttu-id="4117d-133">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="4117d-133">Resource tags.</span></span>

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

### <span data-ttu-id="4117d-134">-확인</span><span class="sxs-lookup"><span data-stu-id="4117d-134">-Confirm</span></span>
<span data-ttu-id="4117d-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4117d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4117d-136">-WhatIf</span></span>
<span data-ttu-id="4117d-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4117d-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4117d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4117d-139">CommonParameters</span></span>
<span data-ttu-id="4117d-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4117d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4117d-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4117d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4117d-142">입력</span><span class="sxs-lookup"><span data-stu-id="4117d-142">INPUTS</span></span>

## <span data-ttu-id="4117d-143">출력</span><span class="sxs-lookup"><span data-stu-id="4117d-143">OUTPUTS</span></span>

### <span data-ttu-id="4117d-144">Api20191210Preview. i i PowerShell. i i m. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4117d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="4117d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="4117d-145">NOTES</span></span>

<span data-ttu-id="4117d-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="4117d-146">ALIASES</span></span>

## <span data-ttu-id="4117d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4117d-147">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384721"
---
# <span data-ttu-id="70d11-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="70d11-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="70d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d11-102">SYNOPSIS</span></span>
<span data-ttu-id="70d11-103">새 피어링 서비스 prefix를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="70d11-104">구문</span><span class="sxs-lookup"><span data-stu-id="70d11-104">SYNTAX</span></span>

### <span data-ttu-id="70d11-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="70d11-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70d11-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d11-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70d11-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70d11-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d11-108">설명</span><span class="sxs-lookup"><span data-stu-id="70d11-108">DESCRIPTION</span></span>
<span data-ttu-id="70d11-109">피어링 서비스 개체와 연결된 피어링 서비스 prefix를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="70d11-110">예제</span><span class="sxs-lookup"><span data-stu-id="70d11-110">EXAMPLES</span></span>

### <span data-ttu-id="70d11-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="70d11-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="70d11-112">피어링 서비스 개체에서 prefix를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="70d11-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="70d11-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="70d11-114">피어링 서비스 리소스 ID에서 prefix를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="70d11-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="70d11-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="70d11-116">피어링 서비스 리소스 그룹 이름 및 이름에서 prefix를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="70d11-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70d11-117">PARAMETERS</span></span>

### <span data-ttu-id="70d11-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70d11-118">-AsJob</span></span>
<span data-ttu-id="70d11-119">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-119">Run in the background.</span></span>

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

### <span data-ttu-id="70d11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d11-120">-DefaultProfile</span></span>
<span data-ttu-id="70d11-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d11-122">-Name</span><span class="sxs-lookup"><span data-stu-id="70d11-122">-Name</span></span>
<span data-ttu-id="70d11-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d11-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="70d11-124">-PeeringServiceId</span></span>
<span data-ttu-id="70d11-125">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d11-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="70d11-126">-PeeringServiceName</span></span>
<span data-ttu-id="70d11-127">피어링 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-127">The peering service name.</span></span>
<span data-ttu-id="70d11-128">새 New-AzPeeringService 서비스에 대해 Get-AzPeeringService cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="70d11-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d11-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="70d11-129">-PeeringServiceObject</span></span>
<span data-ttu-id="70d11-130">다음 Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="70d11-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70d11-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="70d11-131">-Prefix</span></span>
<span data-ttu-id="70d11-132">세션 IPv4 prefix</span><span class="sxs-lookup"><span data-stu-id="70d11-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="70d11-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d11-133">-ResourceGroupName</span></span>
<span data-ttu-id="70d11-134">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d11-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="70d11-135">-ServiceKey</span></span>
<span data-ttu-id="70d11-136">서비스 공급자가 제공하는 고유한 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="70d11-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70d11-137">-Confirm</span></span>
<span data-ttu-id="70d11-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d11-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d11-139">-WhatIf</span></span>
<span data-ttu-id="70d11-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="70d11-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d11-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d11-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d11-142">CommonParameters</span></span>
<span data-ttu-id="70d11-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70d11-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d11-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70d11-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d11-145">입력</span><span class="sxs-lookup"><span data-stu-id="70d11-145">INPUTS</span></span>

### <span data-ttu-id="70d11-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="70d11-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="70d11-147">출력</span><span class="sxs-lookup"><span data-stu-id="70d11-147">OUTPUTS</span></span>

### <span data-ttu-id="70d11-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="70d11-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="70d11-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70d11-149">NOTES</span></span>

## <span data-ttu-id="70d11-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70d11-150">RELATED LINKS</span></span>

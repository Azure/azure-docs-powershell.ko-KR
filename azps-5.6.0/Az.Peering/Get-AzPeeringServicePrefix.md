---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 8b62189848583d11738a39555bc80ed0a52776fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989473"
---
# <span data-ttu-id="0e647-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="0e647-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="0e647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e647-102">SYNOPSIS</span></span>
<span data-ttu-id="0e647-103">구독에 대한 피어링 서비스 사전 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="0e647-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e647-104">SYNTAX</span></span>

### <span data-ttu-id="0e647-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e647-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e647-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e647-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e647-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e647-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e647-108">설명</span><span class="sxs-lookup"><span data-stu-id="0e647-108">DESCRIPTION</span></span>
<span data-ttu-id="0e647-109">피어링 서비스 개체에 대한 피어링 서비스 프리픽스 나열</span><span class="sxs-lookup"><span data-stu-id="0e647-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="0e647-110">예제</span><span class="sxs-lookup"><span data-stu-id="0e647-110">EXAMPLES</span></span>

### <span data-ttu-id="0e647-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e647-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="0e647-112">파이핑 명령을 기반으로 피어링 서비스에 대한 도두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="0e647-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0e647-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="0e647-114">리소스 ID를 통해 피어링 서비스에 대한 특정 도두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="0e647-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="0e647-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="0e647-116">리소스 ID를 통해 피어링 서비스에 대한 특정 도두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="0e647-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="0e647-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="0e647-118">확장된 특성이 있는 피어링 서비스에 대한 특정 도두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="0e647-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0e647-119">PARAMETERS</span></span>

### <span data-ttu-id="0e647-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e647-120">-DefaultProfile</span></span>
<span data-ttu-id="0e647-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e647-122">-확장</span><span class="sxs-lookup"><span data-stu-id="0e647-122">-Expand</span></span>
<span data-ttu-id="0e647-123">피어링 서비스 연결에 대한 이벤트 보기</span><span class="sxs-lookup"><span data-stu-id="0e647-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="0e647-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0e647-124">-Name</span></span>
<span data-ttu-id="0e647-125">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e647-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="0e647-126">-PeeringServiceName</span></span>
<span data-ttu-id="0e647-127">피어링 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-127">The peering service name.</span></span> <span data-ttu-id="0e647-128">새 피어링 서비스에 New-AzPeeringService cmdlet을 사용하거나 목록에 Get-AzPeeringService 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e647-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="0e647-129">-PeeringServiceObject</span></span>
<span data-ttu-id="0e647-130">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="0e647-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e647-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e647-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e647-132">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e647-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e647-133">-ResourceId</span></span>
<span data-ttu-id="0e647-134">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e647-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e647-135">CommonParameters</span></span>
<span data-ttu-id="0e647-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e647-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e647-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e647-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e647-138">입력</span><span class="sxs-lookup"><span data-stu-id="0e647-138">INPUTS</span></span>

### <span data-ttu-id="0e647-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="0e647-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="0e647-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0e647-140">System.String</span></span>

## <span data-ttu-id="0e647-141">출력</span><span class="sxs-lookup"><span data-stu-id="0e647-141">OUTPUTS</span></span>

### <span data-ttu-id="0e647-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="0e647-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="0e647-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e647-143">NOTES</span></span>

## <span data-ttu-id="0e647-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e647-144">RELATED LINKS</span></span>

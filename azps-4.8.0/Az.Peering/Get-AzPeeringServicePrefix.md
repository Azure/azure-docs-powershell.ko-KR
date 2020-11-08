---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: fef6f1615bb2e3dd9d3bb19738ea6cef393235aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214028"
---
# <span data-ttu-id="e863f-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e863f-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="e863f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e863f-102">SYNOPSIS</span></span>
<span data-ttu-id="e863f-103">구독에 대 한 피어 링 서비스 접두사의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="e863f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e863f-104">SYNTAX</span></span>

### <span data-ttu-id="e863f-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e863f-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e863f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e863f-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e863f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e863f-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e863f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e863f-108">DESCRIPTION</span></span>
<span data-ttu-id="e863f-109">피어 링 서비스 개체에 대 한 피어 링 서비스 접두사 나열</span><span class="sxs-lookup"><span data-stu-id="e863f-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="e863f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e863f-110">EXAMPLES</span></span>

### <span data-ttu-id="e863f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e863f-111">Example 1</span></span>
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

<span data-ttu-id="e863f-112">파이핑 명령을 기반으로 피어 링 서비스에 대 한 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="e863f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e863f-113">Example 2</span></span>
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

<span data-ttu-id="e863f-114">리소스 id를 기준으로 피어 링 서비스에 대 한 특정 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="e863f-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e863f-115">Example 3</span></span>
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

<span data-ttu-id="e863f-116">리소스 id를 기준으로 피어 링 서비스에 대 한 특정 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="e863f-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="e863f-117">Example 4</span></span>
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

<span data-ttu-id="e863f-118">확장 특성을 사용 하 여 피어 링 서비스에 대 한 특정 접두사를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="e863f-119">변수</span><span class="sxs-lookup"><span data-stu-id="e863f-119">PARAMETERS</span></span>

### <span data-ttu-id="e863f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e863f-120">-DefaultProfile</span></span>
<span data-ttu-id="e863f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e863f-122">-확장</span><span class="sxs-lookup"><span data-stu-id="e863f-122">-Expand</span></span>
<span data-ttu-id="e863f-123">피어 링 서비스 접두사에 대 한 이벤트 보기</span><span class="sxs-lookup"><span data-stu-id="e863f-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="e863f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="e863f-124">-Name</span></span>
<span data-ttu-id="e863f-125">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e863f-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="e863f-126">-PeeringServiceName</span></span>
<span data-ttu-id="e863f-127">피어 링 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-127">The peering service name.</span></span> <span data-ttu-id="e863f-128">새 피어 링 서비스 또는 목록 Get-AzPeeringService에 대해 New-AzPeeringService cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="e863f-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="e863f-129">-PeeringServiceObject</span></span>
<span data-ttu-id="e863f-130">Get-AzPeeringService 사용</span><span class="sxs-lookup"><span data-stu-id="e863f-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="e863f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e863f-131">-ResourceGroupName</span></span>
<span data-ttu-id="e863f-132">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e863f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e863f-133">-ResourceId</span></span>
<span data-ttu-id="e863f-134">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-134">The resource id string name.</span></span>

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

### <span data-ttu-id="e863f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e863f-135">CommonParameters</span></span>
<span data-ttu-id="e863f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e863f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e863f-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e863f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e863f-138">입력</span><span class="sxs-lookup"><span data-stu-id="e863f-138">INPUTS</span></span>

### <span data-ttu-id="e863f-139">PSPeeringService (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e863f-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="e863f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e863f-140">System.String</span></span>

## <span data-ttu-id="e863f-141">출력</span><span class="sxs-lookup"><span data-stu-id="e863f-141">OUTPUTS</span></span>

### <span data-ttu-id="e863f-142">PSPeeringServicePrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e863f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="e863f-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e863f-143">NOTES</span></span>

## <span data-ttu-id="e863f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e863f-144">RELATED LINKS</span></span>

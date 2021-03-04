---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 2990b28e811b21940d51ce8d0fd9c7540feccfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989193"
---
# <span data-ttu-id="8258c-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="8258c-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="8258c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8258c-102">SYNOPSIS</span></span>
<span data-ttu-id="8258c-103">부모 피어링 리소스에서 등록된 도두를 설정하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="8258c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8258c-104">SYNTAX</span></span>

### <span data-ttu-id="8258c-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8258c-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8258c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8258c-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8258c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8258c-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8258c-108">설명</span><span class="sxs-lookup"><span data-stu-id="8258c-108">DESCRIPTION</span></span>
<span data-ttu-id="8258c-109">부모 피어링 리소스에서 등록된 도두를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="8258c-110">예제</span><span class="sxs-lookup"><span data-stu-id="8258c-110">EXAMPLES</span></span>

### <span data-ttu-id="8258c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8258c-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="8258c-112">리소스 ID에 따라 강두두를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="8258c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8258c-113">PARAMETERS</span></span>

### <span data-ttu-id="8258c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8258c-114">-AsJob</span></span>
<span data-ttu-id="8258c-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-115">Run in the background.</span></span>

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

### <span data-ttu-id="8258c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8258c-116">-DefaultProfile</span></span>
<span data-ttu-id="8258c-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8258c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8258c-118">-InputObject</span></span>
<span data-ttu-id="8258c-119">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="8258c-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8258c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8258c-120">-Name</span></span>
<span data-ttu-id="8258c-121">도두사 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8258c-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="8258c-122">-PeeringName</span></span>
<span data-ttu-id="8258c-123">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="8258c-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="8258c-124">-Prefix</span></span>
<span data-ttu-id="8258c-125">세션 IPv4 연결선</span><span class="sxs-lookup"><span data-stu-id="8258c-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="8258c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8258c-126">-ResourceGroupName</span></span>
<span data-ttu-id="8258c-127">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="8258c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8258c-128">-ResourceId</span></span>
<span data-ttu-id="8258c-129">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-129">The resource id string name.</span></span>

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

### <span data-ttu-id="8258c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8258c-130">-Confirm</span></span>
<span data-ttu-id="8258c-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8258c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8258c-132">-WhatIf</span></span>
<span data-ttu-id="8258c-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8258c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8258c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8258c-135">CommonParameters</span></span>
<span data-ttu-id="8258c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8258c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8258c-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8258c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8258c-138">입력</span><span class="sxs-lookup"><span data-stu-id="8258c-138">INPUTS</span></span>

### <span data-ttu-id="8258c-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="8258c-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="8258c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8258c-140">System.String</span></span>

## <span data-ttu-id="8258c-141">출력</span><span class="sxs-lookup"><span data-stu-id="8258c-141">OUTPUTS</span></span>

### <span data-ttu-id="8258c-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="8258c-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="8258c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8258c-143">NOTES</span></span>

## <span data-ttu-id="8258c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8258c-144">RELATED LINKS</span></span>

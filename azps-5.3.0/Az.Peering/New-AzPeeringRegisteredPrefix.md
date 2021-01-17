---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384749"
---
# <span data-ttu-id="a2393-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a2393-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a2393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2393-102">SYNOPSIS</span></span>
<span data-ttu-id="a2393-103">피어링 개체에 대해 등록된 Prefix를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="a2393-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2393-104">SYNTAX</span></span>

### <span data-ttu-id="a2393-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a2393-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2393-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2393-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2393-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2393-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2393-108">설명</span><span class="sxs-lookup"><span data-stu-id="a2393-108">DESCRIPTION</span></span>
<span data-ttu-id="a2393-109">피어링 개체에 대해 등록된 Prefix를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="a2393-110">예제</span><span class="sxs-lookup"><span data-stu-id="a2393-110">EXAMPLES</span></span>

### <span data-ttu-id="a2393-111">피어링을 만들고 등록된 Prefix 만들기</span><span class="sxs-lookup"><span data-stu-id="a2393-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="a2393-112">등록된 prefix를 추가하려는 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="a2393-113">그런 다음 commandlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="a2393-114">피어링 resourceId를 사용하여 등록된 asn 만들기</span><span class="sxs-lookup"><span data-stu-id="a2393-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="a2393-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2393-115">PARAMETERS</span></span>

### <span data-ttu-id="a2393-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2393-116">-AsJob</span></span>
<span data-ttu-id="a2393-117">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-117">Run in the background.</span></span>

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

### <span data-ttu-id="a2393-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2393-118">-DefaultProfile</span></span>
<span data-ttu-id="a2393-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2393-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2393-120">-InputObject</span></span>
<span data-ttu-id="a2393-121">다음 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a2393-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2393-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2393-122">-Name</span></span>
<span data-ttu-id="a2393-123">prefix의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2393-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a2393-124">-PeeringName</span></span>
<span data-ttu-id="a2393-125">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a2393-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a2393-126">-Prefix</span></span>
<span data-ttu-id="a2393-127">세션 IPv4 prefix</span><span class="sxs-lookup"><span data-stu-id="a2393-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="a2393-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2393-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2393-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="a2393-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2393-130">-ResourceId</span></span>
<span data-ttu-id="a2393-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-131">The resource id string name.</span></span>

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

### <span data-ttu-id="a2393-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2393-132">-Confirm</span></span>
<span data-ttu-id="a2393-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2393-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2393-134">-WhatIf</span></span>
<span data-ttu-id="a2393-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a2393-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2393-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2393-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2393-137">CommonParameters</span></span>
<span data-ttu-id="a2393-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2393-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2393-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2393-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2393-140">입력</span><span class="sxs-lookup"><span data-stu-id="a2393-140">INPUTS</span></span>

### <span data-ttu-id="a2393-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a2393-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a2393-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a2393-142">System.String</span></span>

## <span data-ttu-id="a2393-143">출력</span><span class="sxs-lookup"><span data-stu-id="a2393-143">OUTPUTS</span></span>

### <span data-ttu-id="a2393-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a2393-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a2393-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2393-145">NOTES</span></span>

## <span data-ttu-id="a2393-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2393-146">RELATED LINKS</span></span>

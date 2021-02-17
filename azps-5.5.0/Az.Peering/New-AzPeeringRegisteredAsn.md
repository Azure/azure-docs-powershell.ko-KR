---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202268"
---
# <span data-ttu-id="0af5a-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="0af5a-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="0af5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af5a-102">SYNOPSIS</span></span>
<span data-ttu-id="0af5a-103">피어링을 위해 등록된 ASN 만들기</span><span class="sxs-lookup"><span data-stu-id="0af5a-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="0af5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0af5a-104">SYNTAX</span></span>

### <span data-ttu-id="0af5a-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0af5a-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af5a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0af5a-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af5a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0af5a-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af5a-108">설명</span><span class="sxs-lookup"><span data-stu-id="0af5a-108">DESCRIPTION</span></span>
<span data-ttu-id="0af5a-109">피어링 개체에 대해 등록된 ASNS를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="0af5a-110">예제</span><span class="sxs-lookup"><span data-stu-id="0af5a-110">EXAMPLES</span></span>

### <span data-ttu-id="0af5a-111">피어링을 만들고 등록된 ASN 만들기</span><span class="sxs-lookup"><span data-stu-id="0af5a-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="0af5a-112">등록된 ASN을 추가하려는 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="0af5a-113">그런 다음 commandlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="0af5a-114">피어링 resourceId를 사용하여 등록된 asn 만들기</span><span class="sxs-lookup"><span data-stu-id="0af5a-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="0af5a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0af5a-115">PARAMETERS</span></span>

### <span data-ttu-id="0af5a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0af5a-116">-AsJob</span></span>
<span data-ttu-id="0af5a-117">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-117">Run in the background.</span></span>

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

### <span data-ttu-id="0af5a-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="0af5a-118">-Asn</span></span>
<span data-ttu-id="0af5a-119">등록할 ASN</span><span class="sxs-lookup"><span data-stu-id="0af5a-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af5a-120">-DefaultProfile</span></span>
<span data-ttu-id="0af5a-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af5a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0af5a-122">-InputObject</span></span>
<span data-ttu-id="0af5a-123">다음 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="0af5a-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="0af5a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0af5a-124">-Name</span></span>
<span data-ttu-id="0af5a-125">등록할 ASN</span><span class="sxs-lookup"><span data-stu-id="0af5a-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="0af5a-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="0af5a-126">-PeeringName</span></span>
<span data-ttu-id="0af5a-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="0af5a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af5a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0af5a-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="0af5a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0af5a-130">-ResourceId</span></span>
<span data-ttu-id="0af5a-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-131">The resource id string name.</span></span>

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

### <span data-ttu-id="0af5a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0af5a-132">-Confirm</span></span>
<span data-ttu-id="0af5a-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af5a-134">-WhatIf</span></span>
<span data-ttu-id="0af5a-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0af5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0af5a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af5a-137">CommonParameters</span></span>
<span data-ttu-id="0af5a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0af5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af5a-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0af5a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af5a-140">입력</span><span class="sxs-lookup"><span data-stu-id="0af5a-140">INPUTS</span></span>

### <span data-ttu-id="0af5a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="0af5a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="0af5a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0af5a-142">System.String</span></span>

## <span data-ttu-id="0af5a-143">출력</span><span class="sxs-lookup"><span data-stu-id="0af5a-143">OUTPUTS</span></span>

### <span data-ttu-id="0af5a-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="0af5a-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="0af5a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0af5a-145">NOTES</span></span>

## <span data-ttu-id="0af5a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0af5a-146">RELATED LINKS</span></span>

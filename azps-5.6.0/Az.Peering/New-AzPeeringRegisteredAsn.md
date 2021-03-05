---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 8d5567d99d7ba7470fb44738bed128d8a438c733
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989352"
---
# <span data-ttu-id="6be35-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6be35-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6be35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6be35-102">SYNOPSIS</span></span>
<span data-ttu-id="6be35-103">피어링을 위해 등록된 ASN 만들기</span><span class="sxs-lookup"><span data-stu-id="6be35-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="6be35-104">구문</span><span class="sxs-lookup"><span data-stu-id="6be35-104">SYNTAX</span></span>

### <span data-ttu-id="6be35-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6be35-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6be35-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6be35-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6be35-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6be35-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6be35-108">설명</span><span class="sxs-lookup"><span data-stu-id="6be35-108">DESCRIPTION</span></span>
<span data-ttu-id="6be35-109">개체 피어링을 위해 등록된 ASNS를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="6be35-110">예제</span><span class="sxs-lookup"><span data-stu-id="6be35-110">EXAMPLES</span></span>

### <span data-ttu-id="6be35-111">피어링 및 등록된 ASN 만들기</span><span class="sxs-lookup"><span data-stu-id="6be35-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="6be35-112">등록된 ASN을 추가할 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="6be35-113">그런 다음 명령줄에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="6be35-114">피어링 resourceId를 사용하여 등록된 asn을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="6be35-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6be35-115">PARAMETERS</span></span>

### <span data-ttu-id="6be35-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6be35-116">-AsJob</span></span>
<span data-ttu-id="6be35-117">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-117">Run in the background.</span></span>

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

### <span data-ttu-id="6be35-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="6be35-118">-Asn</span></span>
<span data-ttu-id="6be35-119">등록할 ASN</span><span class="sxs-lookup"><span data-stu-id="6be35-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="6be35-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be35-120">-DefaultProfile</span></span>
<span data-ttu-id="6be35-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be35-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6be35-122">-InputObject</span></span>
<span data-ttu-id="6be35-123">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6be35-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="6be35-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6be35-124">-Name</span></span>
<span data-ttu-id="6be35-125">등록할 ASN</span><span class="sxs-lookup"><span data-stu-id="6be35-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="6be35-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="6be35-126">-PeeringName</span></span>
<span data-ttu-id="6be35-127">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="6be35-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be35-128">-ResourceGroupName</span></span>
<span data-ttu-id="6be35-129">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="6be35-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6be35-130">-ResourceId</span></span>
<span data-ttu-id="6be35-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-131">The resource id string name.</span></span>

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

### <span data-ttu-id="6be35-132">-확인</span><span class="sxs-lookup"><span data-stu-id="6be35-132">-Confirm</span></span>
<span data-ttu-id="6be35-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6be35-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6be35-134">-WhatIf</span></span>
<span data-ttu-id="6be35-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be35-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6be35-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be35-137">CommonParameters</span></span>
<span data-ttu-id="6be35-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6be35-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be35-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6be35-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be35-140">입력</span><span class="sxs-lookup"><span data-stu-id="6be35-140">INPUTS</span></span>

### <span data-ttu-id="6be35-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6be35-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="6be35-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6be35-142">System.String</span></span>

## <span data-ttu-id="6be35-143">출력</span><span class="sxs-lookup"><span data-stu-id="6be35-143">OUTPUTS</span></span>

### <span data-ttu-id="6be35-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6be35-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6be35-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6be35-145">NOTES</span></span>

## <span data-ttu-id="6be35-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6be35-146">RELATED LINKS</span></span>

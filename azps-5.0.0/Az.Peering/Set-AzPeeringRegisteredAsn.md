---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310139"
---
# <span data-ttu-id="52ed2-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="52ed2-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="52ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="52ed2-103">부모 피어 링 리소스에서 등록 된 ASN을 설정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="52ed2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52ed2-104">SYNTAX</span></span>

### <span data-ttu-id="52ed2-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="52ed2-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ed2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="52ed2-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ed2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="52ed2-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ed2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="52ed2-108">DESCRIPTION</span></span>
<span data-ttu-id="52ed2-109">부모 피어 링 리소스에서 등록 된 ASN을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="52ed2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="52ed2-110">EXAMPLES</span></span>

### <span data-ttu-id="52ed2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="52ed2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="52ed2-112">리소스 id를 기준으로 ASN을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="52ed2-113">변수</span><span class="sxs-lookup"><span data-stu-id="52ed2-113">PARAMETERS</span></span>

### <span data-ttu-id="52ed2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52ed2-114">-AsJob</span></span>
<span data-ttu-id="52ed2-115">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-115">Run in the background.</span></span>

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

### <span data-ttu-id="52ed2-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="52ed2-116">-Asn</span></span>
<span data-ttu-id="52ed2-117">등록할 ASN</span><span class="sxs-lookup"><span data-stu-id="52ed2-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="52ed2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ed2-118">-DefaultProfile</span></span>
<span data-ttu-id="52ed2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ed2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52ed2-120">-InputObject</span></span>
<span data-ttu-id="52ed2-121">Get-AzPeering 사용</span><span class="sxs-lookup"><span data-stu-id="52ed2-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52ed2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="52ed2-122">-Name</span></span>
<span data-ttu-id="52ed2-123">등록할 ASN</span><span class="sxs-lookup"><span data-stu-id="52ed2-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="52ed2-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="52ed2-124">-PeeringName</span></span>
<span data-ttu-id="52ed2-125">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="52ed2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ed2-126">-ResourceGroupName</span></span>
<span data-ttu-id="52ed2-127">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="52ed2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52ed2-128">-ResourceId</span></span>
<span data-ttu-id="52ed2-129">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-129">The resource id string name.</span></span>

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

### <span data-ttu-id="52ed2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="52ed2-130">-Confirm</span></span>
<span data-ttu-id="52ed2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ed2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ed2-132">-WhatIf</span></span>
<span data-ttu-id="52ed2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ed2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ed2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ed2-135">CommonParameters</span></span>
<span data-ttu-id="52ed2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52ed2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ed2-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52ed2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ed2-138">입력</span><span class="sxs-lookup"><span data-stu-id="52ed2-138">INPUTS</span></span>

### <span data-ttu-id="52ed2-139">PSPeeringRegisteredAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52ed2-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="52ed2-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52ed2-140">System.String</span></span>

## <span data-ttu-id="52ed2-141">출력</span><span class="sxs-lookup"><span data-stu-id="52ed2-141">OUTPUTS</span></span>

### <span data-ttu-id="52ed2-142">PSPeeringRegisteredAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52ed2-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="52ed2-143">상속자</span><span class="sxs-lookup"><span data-stu-id="52ed2-143">NOTES</span></span>

## <span data-ttu-id="52ed2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52ed2-144">RELATED LINKS</span></span>

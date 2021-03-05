---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 212daeffe2ded2dd2571d78afe79fd238349bf3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989347"
---
# <span data-ttu-id="a2144-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a2144-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a2144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2144-102">SYNOPSIS</span></span>
<span data-ttu-id="a2144-103">피어링 개체에 대한 등록된 프리세이프를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="a2144-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2144-104">SYNTAX</span></span>

### <span data-ttu-id="a2144-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a2144-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2144-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2144-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2144-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2144-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2144-108">설명</span><span class="sxs-lookup"><span data-stu-id="a2144-108">DESCRIPTION</span></span>
<span data-ttu-id="a2144-109">피어링 개체에 대한 등록된 프리세이프를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="a2144-110">예제</span><span class="sxs-lookup"><span data-stu-id="a2144-110">EXAMPLES</span></span>

### <span data-ttu-id="a2144-111">피어링 및 등록된 연결선 만들기</span><span class="sxs-lookup"><span data-stu-id="a2144-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="a2144-112">등록된 연결부를 추가할 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="a2144-113">그런 다음 명령줄에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="a2144-114">피어링 resourceId를 사용하여 등록된 asn을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="a2144-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2144-115">PARAMETERS</span></span>

### <span data-ttu-id="a2144-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2144-116">-AsJob</span></span>
<span data-ttu-id="a2144-117">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-117">Run in the background.</span></span>

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

### <span data-ttu-id="a2144-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2144-118">-DefaultProfile</span></span>
<span data-ttu-id="a2144-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2144-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2144-120">-InputObject</span></span>
<span data-ttu-id="a2144-121">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a2144-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="a2144-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2144-122">-Name</span></span>
<span data-ttu-id="a2144-123">도두사 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-123">The name of prefix.</span></span>

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

### <span data-ttu-id="a2144-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a2144-124">-PeeringName</span></span>
<span data-ttu-id="a2144-125">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a2144-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a2144-126">-Prefix</span></span>
<span data-ttu-id="a2144-127">세션 IPv4 연결선</span><span class="sxs-lookup"><span data-stu-id="a2144-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="a2144-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2144-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2144-129">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="a2144-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2144-130">-ResourceId</span></span>
<span data-ttu-id="a2144-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-131">The resource id string name.</span></span>

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

### <span data-ttu-id="a2144-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a2144-132">-Confirm</span></span>
<span data-ttu-id="a2144-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2144-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2144-134">-WhatIf</span></span>
<span data-ttu-id="a2144-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2144-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2144-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2144-137">CommonParameters</span></span>
<span data-ttu-id="a2144-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2144-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2144-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2144-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2144-140">입력</span><span class="sxs-lookup"><span data-stu-id="a2144-140">INPUTS</span></span>

### <span data-ttu-id="a2144-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a2144-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a2144-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a2144-142">System.String</span></span>

## <span data-ttu-id="a2144-143">출력</span><span class="sxs-lookup"><span data-stu-id="a2144-143">OUTPUTS</span></span>

### <span data-ttu-id="a2144-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a2144-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a2144-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2144-145">NOTES</span></span>

## <span data-ttu-id="a2144-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2144-146">RELATED LINKS</span></span>

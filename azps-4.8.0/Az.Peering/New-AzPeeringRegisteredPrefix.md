---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214290"
---
# <span data-ttu-id="d46ea-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d46ea-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d46ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d46ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d46ea-103">피어 링 개체에 대해 등록 된 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="d46ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d46ea-104">SYNTAX</span></span>

### <span data-ttu-id="d46ea-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d46ea-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46ea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d46ea-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d46ea-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46ea-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d46ea-108">DESCRIPTION</span></span>
<span data-ttu-id="d46ea-109">피어 링 개체에 대해 등록 된 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="d46ea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d46ea-110">EXAMPLES</span></span>

### <span data-ttu-id="d46ea-111">피어 링을 얻고 등록 된 접두사 만들기</span><span class="sxs-lookup"><span data-stu-id="d46ea-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="d46ea-112">등록 된 접두사를 추가 하려는 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="d46ea-113">그런 다음이를 이상으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="d46ea-114">피어 링 resourceId를 사용 하 여 등록 된 asn 만들기</span><span class="sxs-lookup"><span data-stu-id="d46ea-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="d46ea-115">변수</span><span class="sxs-lookup"><span data-stu-id="d46ea-115">PARAMETERS</span></span>

### <span data-ttu-id="d46ea-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d46ea-116">-AsJob</span></span>
<span data-ttu-id="d46ea-117">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-117">Run in the background.</span></span>

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

### <span data-ttu-id="d46ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46ea-118">-DefaultProfile</span></span>
<span data-ttu-id="d46ea-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d46ea-120">-InputObject</span></span>
<span data-ttu-id="d46ea-121">Get-AzPeering 사용</span><span class="sxs-lookup"><span data-stu-id="d46ea-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="d46ea-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d46ea-122">-Name</span></span>
<span data-ttu-id="d46ea-123">접두사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-123">The name of prefix.</span></span>

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

### <span data-ttu-id="d46ea-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d46ea-124">-PeeringName</span></span>
<span data-ttu-id="d46ea-125">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="d46ea-126">-접두사</span><span class="sxs-lookup"><span data-stu-id="d46ea-126">-Prefix</span></span>
<span data-ttu-id="d46ea-127">세션 IPv4 접두사</span><span class="sxs-lookup"><span data-stu-id="d46ea-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="d46ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="d46ea-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d46ea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d46ea-130">-ResourceId</span></span>
<span data-ttu-id="d46ea-131">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-131">The resource id string name.</span></span>

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

### <span data-ttu-id="d46ea-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d46ea-132">-Confirm</span></span>
<span data-ttu-id="d46ea-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46ea-134">-WhatIf</span></span>
<span data-ttu-id="d46ea-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46ea-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46ea-137">CommonParameters</span></span>
<span data-ttu-id="d46ea-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46ea-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d46ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46ea-140">입력</span><span class="sxs-lookup"><span data-stu-id="d46ea-140">INPUTS</span></span>

### <span data-ttu-id="d46ea-141">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d46ea-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="d46ea-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d46ea-142">System.String</span></span>

## <span data-ttu-id="d46ea-143">출력</span><span class="sxs-lookup"><span data-stu-id="d46ea-143">OUTPUTS</span></span>

### <span data-ttu-id="d46ea-144">PSPeeringRegisteredPrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d46ea-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d46ea-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d46ea-145">NOTES</span></span>

## <span data-ttu-id="d46ea-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d46ea-146">RELATED LINKS</span></span>

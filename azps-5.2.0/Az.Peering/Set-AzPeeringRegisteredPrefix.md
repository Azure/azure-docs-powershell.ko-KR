---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352154"
---
# <span data-ttu-id="718dd-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="718dd-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="718dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="718dd-102">SYNOPSIS</span></span>
<span data-ttu-id="718dd-103">부모 피어링 리소스에서 등록된 prefix를 설정하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="718dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="718dd-104">SYNTAX</span></span>

### <span data-ttu-id="718dd-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="718dd-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="718dd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="718dd-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="718dd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="718dd-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="718dd-108">설명</span><span class="sxs-lookup"><span data-stu-id="718dd-108">DESCRIPTION</span></span>
<span data-ttu-id="718dd-109">부모 피어링 리소스에서 등록된 Prefix를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="718dd-110">예제</span><span class="sxs-lookup"><span data-stu-id="718dd-110">EXAMPLES</span></span>

### <span data-ttu-id="718dd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="718dd-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="718dd-112">리소스 ID를 통해 prefix를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="718dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="718dd-113">PARAMETERS</span></span>

### <span data-ttu-id="718dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="718dd-114">-AsJob</span></span>
<span data-ttu-id="718dd-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-115">Run in the background.</span></span>

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

### <span data-ttu-id="718dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718dd-116">-DefaultProfile</span></span>
<span data-ttu-id="718dd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718dd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="718dd-118">-InputObject</span></span>
<span data-ttu-id="718dd-119">다음 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="718dd-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="718dd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="718dd-120">-Name</span></span>
<span data-ttu-id="718dd-121">prefix의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-121">The name of prefix.</span></span>

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

### <span data-ttu-id="718dd-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="718dd-122">-PeeringName</span></span>
<span data-ttu-id="718dd-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="718dd-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="718dd-124">-Prefix</span></span>
<span data-ttu-id="718dd-125">세션 IPv4 prefix</span><span class="sxs-lookup"><span data-stu-id="718dd-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="718dd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718dd-126">-ResourceGroupName</span></span>
<span data-ttu-id="718dd-127">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="718dd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="718dd-128">-ResourceId</span></span>
<span data-ttu-id="718dd-129">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-129">The resource id string name.</span></span>

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

### <span data-ttu-id="718dd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="718dd-130">-Confirm</span></span>
<span data-ttu-id="718dd-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="718dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="718dd-132">-WhatIf</span></span>
<span data-ttu-id="718dd-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="718dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="718dd-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="718dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718dd-135">CommonParameters</span></span>
<span data-ttu-id="718dd-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="718dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718dd-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="718dd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718dd-138">입력</span><span class="sxs-lookup"><span data-stu-id="718dd-138">INPUTS</span></span>

### <span data-ttu-id="718dd-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="718dd-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="718dd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="718dd-140">System.String</span></span>

## <span data-ttu-id="718dd-141">출력</span><span class="sxs-lookup"><span data-stu-id="718dd-141">OUTPUTS</span></span>

### <span data-ttu-id="718dd-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="718dd-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="718dd-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="718dd-143">NOTES</span></span>

## <span data-ttu-id="718dd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="718dd-144">RELATED LINKS</span></span>

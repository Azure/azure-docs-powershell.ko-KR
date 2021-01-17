---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384679"
---
# <span data-ttu-id="46a50-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="46a50-101">Remove-AzPeering</span></span>

## <span data-ttu-id="46a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a50-102">SYNOPSIS</span></span>
<span data-ttu-id="46a50-103">피어링을 삭제하거나 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-103">Delete or remove a peering.</span></span> <span data-ttu-id="46a50-104">이렇게 하면 모든 자식 리소스 또는 리소스에 대한 경고가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="46a50-105">구문</span><span class="sxs-lookup"><span data-stu-id="46a50-105">SYNTAX</span></span>

### <span data-ttu-id="46a50-106">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="46a50-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a50-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="46a50-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a50-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46a50-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a50-109">설명</span><span class="sxs-lookup"><span data-stu-id="46a50-109">DESCRIPTION</span></span>
<span data-ttu-id="46a50-110">피어링 리소스를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="46a50-111">예제</span><span class="sxs-lookup"><span data-stu-id="46a50-111">EXAMPLES</span></span>

### <span data-ttu-id="46a50-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="46a50-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="46a50-113">리소스 ID로 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="46a50-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46a50-114">PARAMETERS</span></span>

### <span data-ttu-id="46a50-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46a50-115">-AsJob</span></span>
<span data-ttu-id="46a50-116">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-116">Run in the background.</span></span>

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

### <span data-ttu-id="46a50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a50-117">-DefaultProfile</span></span>
<span data-ttu-id="46a50-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a50-119">-Force</span><span class="sxs-lookup"><span data-stu-id="46a50-119">-Force</span></span>
<span data-ttu-id="46a50-120">작업을 강제로 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="46a50-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46a50-121">-InputObject</span></span>
<span data-ttu-id="46a50-122">이 Get-AzPeering 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46a50-123">-Name</span><span class="sxs-lookup"><span data-stu-id="46a50-123">-Name</span></span>
<span data-ttu-id="46a50-124">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a50-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46a50-125">-PassThru</span></span>
<span data-ttu-id="46a50-126">완료된 경우 true 반환</span><span class="sxs-lookup"><span data-stu-id="46a50-126">Return true if complete</span></span>

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

### <span data-ttu-id="46a50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a50-127">-ResourceGroupName</span></span>
<span data-ttu-id="46a50-128">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a50-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a50-129">-ResourceId</span></span>
<span data-ttu-id="46a50-130">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a50-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46a50-131">-Confirm</span></span>
<span data-ttu-id="46a50-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a50-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a50-133">-WhatIf</span></span>
<span data-ttu-id="46a50-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46a50-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a50-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a50-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a50-136">CommonParameters</span></span>
<span data-ttu-id="46a50-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46a50-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a50-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46a50-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a50-139">입력</span><span class="sxs-lookup"><span data-stu-id="46a50-139">INPUTS</span></span>

### <span data-ttu-id="46a50-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="46a50-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="46a50-141">System.String</span><span class="sxs-lookup"><span data-stu-id="46a50-141">System.String</span></span>

## <span data-ttu-id="46a50-142">출력</span><span class="sxs-lookup"><span data-stu-id="46a50-142">OUTPUTS</span></span>

### <span data-ttu-id="46a50-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46a50-143">System.Boolean</span></span>

## <span data-ttu-id="46a50-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46a50-144">NOTES</span></span>

## <span data-ttu-id="46a50-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46a50-145">RELATED LINKS</span></span>

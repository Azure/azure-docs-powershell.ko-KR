---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492576"
---
# <span data-ttu-id="10cea-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10cea-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="10cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10cea-102">SYNOPSIS</span></span>
<span data-ttu-id="10cea-103">Azure IpGroup을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="10cea-104">구문</span><span class="sxs-lookup"><span data-stu-id="10cea-104">SYNTAX</span></span>

### <span data-ttu-id="10cea-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10cea-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10cea-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10cea-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10cea-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10cea-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10cea-108">설명</span><span class="sxs-lookup"><span data-stu-id="10cea-108">DESCRIPTION</span></span>
<span data-ttu-id="10cea-109">**Remove-AzIpGroup** cmdlet은 Azure IpGroup을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="10cea-110">예제</span><span class="sxs-lookup"><span data-stu-id="10cea-110">EXAMPLES</span></span>

### <span data-ttu-id="10cea-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="10cea-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="10cea-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="10cea-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="10cea-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="10cea-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="10cea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10cea-114">PARAMETERS</span></span>

### <span data-ttu-id="10cea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10cea-115">-AsJob</span></span>
<span data-ttu-id="10cea-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="10cea-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cea-117">-DefaultProfile</span></span>
<span data-ttu-id="10cea-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-119">-Force</span><span class="sxs-lookup"><span data-stu-id="10cea-119">-Force</span></span>
<span data-ttu-id="10cea-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="10cea-121">-IpGroup</span></span>
<span data-ttu-id="10cea-122">ipGroup 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-123">-Name</span><span class="sxs-lookup"><span data-stu-id="10cea-123">-Name</span></span>
<span data-ttu-id="10cea-124">ipgroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10cea-125">-PassThru</span></span>
<span data-ttu-id="10cea-126">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-126">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10cea-127">-ResourceGroupName</span></span>
<span data-ttu-id="10cea-128">ipgroup의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10cea-129">-ResourceId</span></span>
<span data-ttu-id="10cea-130">ipgroup 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10cea-131">-Confirm</span></span>
<span data-ttu-id="10cea-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10cea-133">-WhatIf</span></span>
<span data-ttu-id="10cea-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10cea-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10cea-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cea-136">CommonParameters</span></span>
<span data-ttu-id="10cea-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10cea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cea-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10cea-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cea-139">입력</span><span class="sxs-lookup"><span data-stu-id="10cea-139">INPUTS</span></span>

### <span data-ttu-id="10cea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="10cea-140">System.String</span></span>

### <span data-ttu-id="10cea-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="10cea-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="10cea-142">출력</span><span class="sxs-lookup"><span data-stu-id="10cea-142">OUTPUTS</span></span>

### <span data-ttu-id="10cea-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10cea-143">System.Boolean</span></span>

## <span data-ttu-id="10cea-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10cea-144">NOTES</span></span>

## <span data-ttu-id="10cea-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10cea-145">RELATED LINKS</span></span>

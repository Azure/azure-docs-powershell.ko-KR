---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363469"
---
# <span data-ttu-id="e6b2f-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="e6b2f-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="e6b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b2f-103">Azure IpAllocation을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="e6b2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6b2f-104">SYNTAX</span></span>

### <span data-ttu-id="e6b2f-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b2f-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b2f-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b2f-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b2f-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b2f-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6b2f-108">설명</span><span class="sxs-lookup"><span data-stu-id="e6b2f-108">DESCRIPTION</span></span>
<span data-ttu-id="e6b2f-109">**Remove-AzIpAllocation** cmdlet은 Azure IpAllocation을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="e6b2f-110">예제</span><span class="sxs-lookup"><span data-stu-id="e6b2f-110">EXAMPLES</span></span>

### <span data-ttu-id="e6b2f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6b2f-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="e6b2f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6b2f-112">PARAMETERS</span></span>

### <span data-ttu-id="e6b2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6b2f-113">-AsJob</span></span>
<span data-ttu-id="e6b2f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6b2f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6b2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b2f-115">-DefaultProfile</span></span>
<span data-ttu-id="e6b2f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b2f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e6b2f-117">-Force</span></span>
<span data-ttu-id="e6b2f-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e6b2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6b2f-119">-InputObject</span></span>
<span data-ttu-id="e6b2f-120">{{ InputObject 설명 입력 }}</span><span class="sxs-lookup"><span data-stu-id="e6b2f-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b2f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e6b2f-121">-Name</span></span>
<span data-ttu-id="e6b2f-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b2f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6b2f-123">-PassThru</span></span>
<span data-ttu-id="e6b2f-124">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6b2f-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6b2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6b2f-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b2f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b2f-128">-ResourceId</span></span>
<span data-ttu-id="e6b2f-129">IpAllocation 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b2f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6b2f-130">-Confirm</span></span>
<span data-ttu-id="e6b2f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6b2f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6b2f-132">-WhatIf</span></span>
<span data-ttu-id="e6b2f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e6b2f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6b2f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6b2f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b2f-135">CommonParameters</span></span>
<span data-ttu-id="e6b2f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b2f-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b2f-138">입력</span><span class="sxs-lookup"><span data-stu-id="e6b2f-138">INPUTS</span></span>

### <span data-ttu-id="e6b2f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e6b2f-139">System.String</span></span>

## <span data-ttu-id="e6b2f-140">출력</span><span class="sxs-lookup"><span data-stu-id="e6b2f-140">OUTPUTS</span></span>

### <span data-ttu-id="e6b2f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6b2f-141">System.Boolean</span></span>

## <span data-ttu-id="e6b2f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6b2f-142">NOTES</span></span>

## <span data-ttu-id="e6b2f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6b2f-143">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 707f3157cead45d501cdfdaf357222cdaceac826
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015227"
---
# <span data-ttu-id="19ac2-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="19ac2-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="19ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="19ac2-103">WAF 정책 제거</span><span class="sxs-lookup"><span data-stu-id="19ac2-103">Remove WAF policy</span></span>

## <span data-ttu-id="19ac2-104">구문</span><span class="sxs-lookup"><span data-stu-id="19ac2-104">SYNTAX</span></span>

### <span data-ttu-id="19ac2-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="19ac2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ac2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19ac2-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ac2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19ac2-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19ac2-108">설명</span><span class="sxs-lookup"><span data-stu-id="19ac2-108">DESCRIPTION</span></span>
<span data-ttu-id="19ac2-109">**Remove-AzFrontDoorWafPolicy** cmdlet은 현재 구독에서 WAF 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="19ac2-110">예제</span><span class="sxs-lookup"><span data-stu-id="19ac2-110">EXAMPLES</span></span>

### <span data-ttu-id="19ac2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="19ac2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="19ac2-112">에서 $policyName WAF 정책을 $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="19ac2-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="19ac2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="19ac2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="19ac2-114">모든 WAF 정책을 $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="19ac2-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="19ac2-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19ac2-115">PARAMETERS</span></span>

### <span data-ttu-id="19ac2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ac2-116">-DefaultProfile</span></span>
<span data-ttu-id="19ac2-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19ac2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19ac2-118">-InputObject</span></span>
<span data-ttu-id="19ac2-119">삭제할 WAF 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19ac2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="19ac2-120">-Name</span></span>
<span data-ttu-id="19ac2-121">삭제할 WAF 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ac2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19ac2-122">-PassThru</span></span>
<span data-ttu-id="19ac2-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="19ac2-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="19ac2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ac2-124">-ResourceGroupName</span></span>
<span data-ttu-id="19ac2-125">WAF 정책이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ac2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19ac2-126">-ResourceId</span></span>
<span data-ttu-id="19ac2-127">삭제할 WAF 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="19ac2-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19ac2-128">-확인</span><span class="sxs-lookup"><span data-stu-id="19ac2-128">-Confirm</span></span>
<span data-ttu-id="19ac2-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ac2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ac2-130">-WhatIf</span></span>
<span data-ttu-id="19ac2-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ac2-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ac2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ac2-133">CommonParameters</span></span>
<span data-ttu-id="19ac2-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19ac2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ac2-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19ac2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ac2-136">입력</span><span class="sxs-lookup"><span data-stu-id="19ac2-136">INPUTS</span></span>

### <span data-ttu-id="19ac2-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="19ac2-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="19ac2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="19ac2-138">System.String</span></span>

## <span data-ttu-id="19ac2-139">출력</span><span class="sxs-lookup"><span data-stu-id="19ac2-139">OUTPUTS</span></span>

### <span data-ttu-id="19ac2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19ac2-140">System.Boolean</span></span>

## <span data-ttu-id="19ac2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19ac2-141">NOTES</span></span>

## <span data-ttu-id="19ac2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19ac2-142">RELATED LINKS</span></span>

<span data-ttu-id="19ac2-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="19ac2-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>

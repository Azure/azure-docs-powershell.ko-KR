---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185916"
---
# <span data-ttu-id="06e58-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="06e58-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="06e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e58-102">SYNOPSIS</span></span>
<span data-ttu-id="06e58-103">WAF 정책 제거</span><span class="sxs-lookup"><span data-stu-id="06e58-103">Remove WAF policy</span></span>

## <span data-ttu-id="06e58-104">구문</span><span class="sxs-lookup"><span data-stu-id="06e58-104">SYNTAX</span></span>

### <span data-ttu-id="06e58-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="06e58-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e58-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e58-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e58-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e58-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e58-108">설명</span><span class="sxs-lookup"><span data-stu-id="06e58-108">DESCRIPTION</span></span>
<span data-ttu-id="06e58-109">**Remove-AzFrontDoorWafPolicy** cmdlet은 현재 구독에서 WAF 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="06e58-110">예제</span><span class="sxs-lookup"><span data-stu-id="06e58-110">EXAMPLES</span></span>

### <span data-ttu-id="06e58-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="06e58-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="06e58-112">다음 목록에서 $policyName WAF 정책을 $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="06e58-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="06e58-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="06e58-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="06e58-114">모든 WAF 정책은 $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="06e58-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="06e58-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06e58-115">PARAMETERS</span></span>

### <span data-ttu-id="06e58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e58-116">-DefaultProfile</span></span>
<span data-ttu-id="06e58-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e58-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06e58-118">-InputObject</span></span>
<span data-ttu-id="06e58-119">삭제할 WAF 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="06e58-120">-Name</span><span class="sxs-lookup"><span data-stu-id="06e58-120">-Name</span></span>
<span data-ttu-id="06e58-121">삭제할 WAF 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="06e58-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06e58-122">-PassThru</span></span>
<span data-ttu-id="06e58-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="06e58-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="06e58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e58-124">-ResourceGroupName</span></span>
<span data-ttu-id="06e58-125">WAF 정책이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="06e58-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e58-126">-ResourceId</span></span>
<span data-ttu-id="06e58-127">삭제할 WAF 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="06e58-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="06e58-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06e58-128">-Confirm</span></span>
<span data-ttu-id="06e58-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e58-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e58-130">-WhatIf</span></span>
<span data-ttu-id="06e58-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06e58-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e58-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e58-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e58-133">CommonParameters</span></span>
<span data-ttu-id="06e58-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06e58-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e58-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06e58-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e58-136">입력</span><span class="sxs-lookup"><span data-stu-id="06e58-136">INPUTS</span></span>

### <span data-ttu-id="06e58-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="06e58-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="06e58-138">System.String</span><span class="sxs-lookup"><span data-stu-id="06e58-138">System.String</span></span>

## <span data-ttu-id="06e58-139">출력</span><span class="sxs-lookup"><span data-stu-id="06e58-139">OUTPUTS</span></span>

### <span data-ttu-id="06e58-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06e58-140">System.Boolean</span></span>

## <span data-ttu-id="06e58-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06e58-141">NOTES</span></span>

## <span data-ttu-id="06e58-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06e58-142">RELATED LINKS</span></span>

<span data-ttu-id="06e58-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="06e58-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>

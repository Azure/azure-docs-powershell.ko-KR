---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047748"
---
# <span data-ttu-id="a98d4-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="a98d4-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="a98d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a98d4-103">WAF 정책 제거</span><span class="sxs-lookup"><span data-stu-id="a98d4-103">Remove WAF policy</span></span>

## <span data-ttu-id="a98d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a98d4-104">SYNTAX</span></span>

### <span data-ttu-id="a98d4-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a98d4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a98d4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a98d4-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a98d4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a98d4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a98d4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a98d4-108">DESCRIPTION</span></span>
<span data-ttu-id="a98d4-109">AzFrontDoorWafPolicy cmdlet은 현재 구독에서 WAF 정책을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="a98d4-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="a98d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a98d4-110">EXAMPLES</span></span>

### <span data-ttu-id="a98d4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a98d4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="a98d4-112">$ResourceGroupName에서 $policyName 이라는 WAF 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="a98d4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a98d4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="a98d4-114">$ResourceGroupName에서 모든 WAF 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="a98d4-115">변수</span><span class="sxs-lookup"><span data-stu-id="a98d4-115">PARAMETERS</span></span>

### <span data-ttu-id="a98d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98d4-116">-DefaultProfile</span></span>
<span data-ttu-id="a98d4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a98d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a98d4-118">-InputObject</span></span>
<span data-ttu-id="a98d4-119">삭제할 WAF 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="a98d4-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a98d4-120">-Name</span></span>
<span data-ttu-id="a98d4-121">삭제할 WAF 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="a98d4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a98d4-122">-PassThru</span></span>
<span data-ttu-id="a98d4-123">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="a98d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a98d4-125">WAF 정책이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="a98d4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a98d4-126">-ResourceId</span></span>
<span data-ttu-id="a98d4-127">삭제할 WAF 정책의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="a98d4-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a98d4-128">-Confirm</span></span>
<span data-ttu-id="a98d4-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a98d4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a98d4-130">-WhatIf</span></span>
<span data-ttu-id="a98d4-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a98d4-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a98d4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98d4-133">CommonParameters</span></span>
<span data-ttu-id="a98d4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98d4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98d4-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a98d4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98d4-136">입력</span><span class="sxs-lookup"><span data-stu-id="a98d4-136">INPUTS</span></span>

### <span data-ttu-id="a98d4-137">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="a98d4-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="a98d4-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a98d4-138">System.String</span></span>

## <span data-ttu-id="a98d4-139">출력</span><span class="sxs-lookup"><span data-stu-id="a98d4-139">OUTPUTS</span></span>

### <span data-ttu-id="a98d4-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a98d4-140">System.Boolean</span></span>

## <span data-ttu-id="a98d4-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a98d4-141">NOTES</span></span>

## <span data-ttu-id="a98d4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a98d4-142">RELATED LINKS</span></span>

<span data-ttu-id="a98d4-143">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a98d4-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>

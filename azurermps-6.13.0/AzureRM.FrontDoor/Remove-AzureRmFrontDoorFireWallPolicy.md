---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524400"
---
# <span data-ttu-id="f9ea6-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="f9ea6-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="f9ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ea6-103">WAF 정책 제거</span><span class="sxs-lookup"><span data-stu-id="f9ea6-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9ea6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9ea6-104">SYNTAX</span></span>

### <span data-ttu-id="f9ea6-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9ea6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ea6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9ea6-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ea6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9ea6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ea6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f9ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ea6-109">AzureRmFrontDoor cmdlet은 현재 구독에서 WAF 정책을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="f9ea6-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="f9ea6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f9ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="f9ea6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9ea6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="f9ea6-112">$ResourceGroup에서 $name 이라는 WAF 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="f9ea6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f9ea6-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="f9ea6-114">$ResourceGroup에서 모든 WAF 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="f9ea6-115">변수</span><span class="sxs-lookup"><span data-stu-id="f9ea6-115">PARAMETERS</span></span>

### <span data-ttu-id="f9ea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ea6-116">-DefaultProfile</span></span>
<span data-ttu-id="f9ea6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ea6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9ea6-118">-InputObject</span></span>
<span data-ttu-id="f9ea6-119">삭제할 WAF 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="f9ea6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f9ea6-120">-Name</span></span>
<span data-ttu-id="f9ea6-121">삭제할 WAF 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="f9ea6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9ea6-122">-PassThru</span></span>
<span data-ttu-id="f9ea6-123">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="f9ea6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9ea6-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9ea6-125">WAF 정책이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="f9ea6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ea6-126">-ResourceId</span></span>
<span data-ttu-id="f9ea6-127">삭제할 WAF 정책의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ea6-128">-확인</span><span class="sxs-lookup"><span data-stu-id="f9ea6-128">-Confirm</span></span>
<span data-ttu-id="f9ea6-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ea6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ea6-130">-WhatIf</span></span>
<span data-ttu-id="f9ea6-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ea6-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ea6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ea6-133">CommonParameters</span></span>
<span data-ttu-id="f9ea6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ea6-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ea6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ea6-136">입력</span><span class="sxs-lookup"><span data-stu-id="f9ea6-136">INPUTS</span></span>

### <span data-ttu-id="f9ea6-137">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="f9ea6-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9ea6-138">System.String</span></span>

### <span data-ttu-id="f9ea6-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9ea6-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9ea6-140">출력</span><span class="sxs-lookup"><span data-stu-id="f9ea6-140">OUTPUTS</span></span>

### <span data-ttu-id="f9ea6-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f9ea6-141">System.Boolean</span></span>

## <span data-ttu-id="f9ea6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f9ea6-142">NOTES</span></span>

## <span data-ttu-id="f9ea6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9ea6-143">RELATED LINKS</span></span>

<span data-ttu-id="f9ea6-144">[새로운 AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f9ea6-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212231"
---
# <span data-ttu-id="85e50-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="85e50-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="85e50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85e50-102">SYNOPSIS</span></span>
<span data-ttu-id="85e50-103">전방 도어 부하 분산 제거</span><span class="sxs-lookup"><span data-stu-id="85e50-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="85e50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85e50-104">SYNTAX</span></span>

### <span data-ttu-id="85e50-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="85e50-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e50-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e50-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e50-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e50-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85e50-108">설명은</span><span class="sxs-lookup"><span data-stu-id="85e50-108">DESCRIPTION</span></span>
<span data-ttu-id="85e50-109">**AzFrontDoor** cmdlet은 현재 구독에서 프론트 도어 부하 분산 장치를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="85e50-110">예제의</span><span class="sxs-lookup"><span data-stu-id="85e50-110">EXAMPLES</span></span>

### <span data-ttu-id="85e50-111">예제 1: 현재 구독 아래의 리소스 그룹 "rg1"에서 "frontdoor1"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="85e50-112">현재 구독에서 리소스 그룹 "rg1"에 있는 "frontdoor1"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="85e50-113">예제 2: 현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="85e50-114">현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="85e50-115">예제 3: 현재 구독에서 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="85e50-116">현재 구독에서 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="85e50-117">예제 4: 현재 구독에서 이름이 "frontdoor1" 인 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="85e50-118">현재 구독에서 이름이 "frontdoor1" 인 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="85e50-119">변수</span><span class="sxs-lookup"><span data-stu-id="85e50-119">PARAMETERS</span></span>

### <span data-ttu-id="85e50-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e50-120">-DefaultProfile</span></span>
<span data-ttu-id="85e50-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85e50-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85e50-122">-InputObject</span></span>
<span data-ttu-id="85e50-123">삭제할 전방 도어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85e50-124">-이름</span><span class="sxs-lookup"><span data-stu-id="85e50-124">-Name</span></span>
<span data-ttu-id="85e50-125">삭제할 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="85e50-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85e50-126">-PassThru</span></span>
<span data-ttu-id="85e50-127">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="85e50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e50-128">-ResourceGroupName</span></span>
<span data-ttu-id="85e50-129">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="85e50-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85e50-130">-ResourceId</span></span>
<span data-ttu-id="85e50-131">삭제할 앞면 도어의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="85e50-132">-확인</span><span class="sxs-lookup"><span data-stu-id="85e50-132">-Confirm</span></span>
<span data-ttu-id="85e50-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85e50-134">-WhatIf</span></span>
<span data-ttu-id="85e50-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85e50-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e50-137">CommonParameters</span></span>
<span data-ttu-id="85e50-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85e50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e50-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85e50-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e50-140">입력</span><span class="sxs-lookup"><span data-stu-id="85e50-140">INPUTS</span></span>

### <span data-ttu-id="85e50-141">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="85e50-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="85e50-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="85e50-142">System.String</span></span>

## <span data-ttu-id="85e50-143">출력</span><span class="sxs-lookup"><span data-stu-id="85e50-143">OUTPUTS</span></span>

### <span data-ttu-id="85e50-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="85e50-144">System.Boolean</span></span>

## <span data-ttu-id="85e50-145">상속자</span><span class="sxs-lookup"><span data-stu-id="85e50-145">NOTES</span></span>

## <span data-ttu-id="85e50-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85e50-146">RELATED LINKS</span></span>

<span data-ttu-id="85e50-147">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="85e50-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>
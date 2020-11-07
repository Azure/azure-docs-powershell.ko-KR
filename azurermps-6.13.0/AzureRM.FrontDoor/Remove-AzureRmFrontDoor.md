---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701969"
---
# <span data-ttu-id="63f3f-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="63f3f-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="63f3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="63f3f-103">전방 도어 부하 분산 제거</span><span class="sxs-lookup"><span data-stu-id="63f3f-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63f3f-104">SYNTAX</span></span>

### <span data-ttu-id="63f3f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="63f3f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f3f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63f3f-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f3f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63f3f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f3f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="63f3f-108">DESCRIPTION</span></span>
<span data-ttu-id="63f3f-109">**AzureRmFrontDoor** cmdlet은 현재 구독에서 프론트 도어 부하 분산 장치를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="63f3f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="63f3f-110">EXAMPLES</span></span>

### <span data-ttu-id="63f3f-111">예제 1: 현재 구독 아래의 리소스 그룹 "rg1"에서 "frontdoor1"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="63f3f-112">현재 구독에서 리소스 그룹 "rg1"에 있는 "frontdoor1"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="63f3f-113">예제 2: 현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="63f3f-114">현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="63f3f-115">예제 3: 현재 구독에서 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="63f3f-116">현재 구독에서 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="63f3f-117">예제 4: 현재 구독에서 이름이 "frontdoor1" 인 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="63f3f-118">현재 구독에서 이름이 "frontdoor1" 인 모든 FrontDoors를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="63f3f-119">변수</span><span class="sxs-lookup"><span data-stu-id="63f3f-119">PARAMETERS</span></span>

### <span data-ttu-id="63f3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f3f-120">-DefaultProfile</span></span>
<span data-ttu-id="63f3f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f3f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63f3f-122">-InputObject</span></span>
<span data-ttu-id="63f3f-123">삭제할 전방 도어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="63f3f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="63f3f-124">-Name</span></span>
<span data-ttu-id="63f3f-125">삭제할 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="63f3f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63f3f-126">-PassThru</span></span>
<span data-ttu-id="63f3f-127">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="63f3f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f3f-128">-ResourceGroupName</span></span>
<span data-ttu-id="63f3f-129">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="63f3f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63f3f-130">-ResourceId</span></span>
<span data-ttu-id="63f3f-131">삭제할 앞면 도어의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="63f3f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="63f3f-132">-Confirm</span></span>
<span data-ttu-id="63f3f-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f3f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f3f-134">-WhatIf</span></span>
<span data-ttu-id="63f3f-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f3f-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f3f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f3f-137">CommonParameters</span></span>
<span data-ttu-id="63f3f-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63f3f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f3f-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f3f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f3f-140">입력</span><span class="sxs-lookup"><span data-stu-id="63f3f-140">INPUTS</span></span>

### <span data-ttu-id="63f3f-141">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="63f3f-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="63f3f-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63f3f-142">System.String</span></span>

### <span data-ttu-id="63f3f-143">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="63f3f-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63f3f-144">출력</span><span class="sxs-lookup"><span data-stu-id="63f3f-144">OUTPUTS</span></span>

### <span data-ttu-id="63f3f-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="63f3f-145">System.Boolean</span></span>

## <span data-ttu-id="63f3f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="63f3f-146">NOTES</span></span>

## <span data-ttu-id="63f3f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63f3f-147">RELATED LINKS</span></span>

<span data-ttu-id="63f3f-148">[새로운 AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="63f3f-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>

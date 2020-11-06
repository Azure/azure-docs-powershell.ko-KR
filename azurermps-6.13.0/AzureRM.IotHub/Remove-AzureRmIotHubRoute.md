---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
ms.openlocfilehash: 9af711bd449bc8c69808f30dc99ceea806dee00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535888"
---
# <span data-ttu-id="20486-101">Remove-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="20486-101">Remove-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="20486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20486-102">SYNOPSIS</span></span>
<span data-ttu-id="20486-103">IoT Hub에서 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="20486-103">Delete a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20486-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20486-104">SYNTAX</span></span>

### <span data-ttu-id="20486-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="20486-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20486-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20486-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20486-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="20486-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20486-108">설명은</span><span class="sxs-lookup"><span data-stu-id="20486-108">DESCRIPTION</span></span>
<span data-ttu-id="20486-109">끝점에 대 한 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="20486-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="20486-110">예제의</span><span class="sxs-lookup"><span data-stu-id="20486-110">EXAMPLES</span></span>

### <span data-ttu-id="20486-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="20486-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="20486-112">"Myiothub" IoT Hub에서 "R1" 경로를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20486-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="20486-113">변수</span><span class="sxs-lookup"><span data-stu-id="20486-113">PARAMETERS</span></span>

### <span data-ttu-id="20486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20486-114">-DefaultProfile</span></span>
<span data-ttu-id="20486-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20486-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20486-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20486-116">-InputObject</span></span>
<span data-ttu-id="20486-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="20486-117">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20486-118">-이름</span><span class="sxs-lookup"><span data-stu-id="20486-118">-Name</span></span>
<span data-ttu-id="20486-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="20486-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20486-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20486-120">-PassThru</span></span>
<span data-ttu-id="20486-121">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20486-121">Allows to return the boolean object.</span></span> <span data-ttu-id="20486-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20486-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20486-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20486-123">-ResourceGroupName</span></span>
<span data-ttu-id="20486-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20486-124">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20486-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20486-125">-ResourceId</span></span>
<span data-ttu-id="20486-126">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="20486-126">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20486-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="20486-127">-RouteName</span></span>
<span data-ttu-id="20486-128">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="20486-128">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20486-129">-확인</span><span class="sxs-lookup"><span data-stu-id="20486-129">-Confirm</span></span>
<span data-ttu-id="20486-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20486-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20486-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20486-131">-WhatIf</span></span>
<span data-ttu-id="20486-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20486-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20486-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20486-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20486-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20486-134">CommonParameters</span></span>
<span data-ttu-id="20486-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20486-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20486-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20486-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20486-137">입력</span><span class="sxs-lookup"><span data-stu-id="20486-137">INPUTS</span></span>

### <span data-ttu-id="20486-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="20486-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="20486-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20486-139">System.String</span></span>

## <span data-ttu-id="20486-140">출력</span><span class="sxs-lookup"><span data-stu-id="20486-140">OUTPUTS</span></span>

### <span data-ttu-id="20486-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="20486-141">System.Boolean</span></span>

## <span data-ttu-id="20486-142">상속자</span><span class="sxs-lookup"><span data-stu-id="20486-142">NOTES</span></span>

## <span data-ttu-id="20486-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20486-143">RELATED LINKS</span></span>

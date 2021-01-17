---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343581"
---
# <span data-ttu-id="483f7-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="483f7-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="483f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483f7-102">SYNOPSIS</span></span>
<span data-ttu-id="483f7-103">IoT 디바이스 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="483f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="483f7-104">SYNTAX</span></span>

### <span data-ttu-id="483f7-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="483f7-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483f7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="483f7-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483f7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="483f7-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483f7-108">설명</span><span class="sxs-lookup"><span data-stu-id="483f7-108">DESCRIPTION</span></span>
<span data-ttu-id="483f7-109">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="483f7-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="483f7-110">예제</span><span class="sxs-lookup"><span data-stu-id="483f7-110">EXAMPLES</span></span>

### <span data-ttu-id="483f7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="483f7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="483f7-112">IoT 디바이스 구성을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="483f7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="483f7-113">PARAMETERS</span></span>

### <span data-ttu-id="483f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483f7-114">-DefaultProfile</span></span>
<span data-ttu-id="483f7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="483f7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="483f7-116">-InputObject</span></span>
<span data-ttu-id="483f7-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="483f7-117">IotHub object</span></span>

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

### <span data-ttu-id="483f7-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="483f7-118">-IotHubName</span></span>
<span data-ttu-id="483f7-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="483f7-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="483f7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="483f7-120">-Name</span></span>
<span data-ttu-id="483f7-121">구성에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="483f7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="483f7-122">-PassThru</span></span>
<span data-ttu-id="483f7-123">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="483f7-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="483f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="483f7-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="483f7-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="483f7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="483f7-127">-ResourceId</span></span>
<span data-ttu-id="483f7-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="483f7-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="483f7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="483f7-129">-Confirm</span></span>
<span data-ttu-id="483f7-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483f7-131">-WhatIf</span></span>
<span data-ttu-id="483f7-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="483f7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483f7-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483f7-134">CommonParameters</span></span>
<span data-ttu-id="483f7-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="483f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483f7-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="483f7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483f7-137">입력</span><span class="sxs-lookup"><span data-stu-id="483f7-137">INPUTS</span></span>

### <span data-ttu-id="483f7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="483f7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="483f7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="483f7-139">System.String</span></span>

## <span data-ttu-id="483f7-140">출력</span><span class="sxs-lookup"><span data-stu-id="483f7-140">OUTPUTS</span></span>

### <span data-ttu-id="483f7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="483f7-141">System.Boolean</span></span>

## <span data-ttu-id="483f7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="483f7-142">NOTES</span></span>

## <span data-ttu-id="483f7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="483f7-143">RELATED LINKS</span></span>

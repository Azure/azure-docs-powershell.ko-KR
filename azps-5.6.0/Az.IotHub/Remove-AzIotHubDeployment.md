---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: a125bd402a58bc138e1fa74ec2f68d659f2a1d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970784"
---
# <span data-ttu-id="72151-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="72151-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="72151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72151-102">SYNOPSIS</span></span>
<span data-ttu-id="72151-103">IoT Edge 배포를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="72151-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="72151-104">구문</span><span class="sxs-lookup"><span data-stu-id="72151-104">SYNTAX</span></span>

### <span data-ttu-id="72151-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="72151-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72151-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72151-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72151-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72151-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72151-108">설명</span><span class="sxs-lookup"><span data-stu-id="72151-108">DESCRIPTION</span></span>
<span data-ttu-id="72151-109">자세한 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="72151-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="72151-110">예제</span><span class="sxs-lookup"><span data-stu-id="72151-110">EXAMPLES</span></span>

### <span data-ttu-id="72151-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="72151-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="72151-112">IoT Edge 배포를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="72151-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="72151-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="72151-113">PARAMETERS</span></span>

### <span data-ttu-id="72151-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72151-114">-DefaultProfile</span></span>
<span data-ttu-id="72151-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72151-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72151-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72151-116">-InputObject</span></span>
<span data-ttu-id="72151-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="72151-117">IotHub object</span></span>

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

### <span data-ttu-id="72151-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="72151-118">-IotHubName</span></span>
<span data-ttu-id="72151-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="72151-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="72151-120">-Name</span><span class="sxs-lookup"><span data-stu-id="72151-120">-Name</span></span>
<span data-ttu-id="72151-121">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="72151-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="72151-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72151-122">-PassThru</span></span>
<span data-ttu-id="72151-123">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72151-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="72151-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72151-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72151-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72151-125">-ResourceGroupName</span></span>
<span data-ttu-id="72151-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="72151-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="72151-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72151-127">-ResourceId</span></span>
<span data-ttu-id="72151-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="72151-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="72151-129">-확인</span><span class="sxs-lookup"><span data-stu-id="72151-129">-Confirm</span></span>
<span data-ttu-id="72151-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="72151-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72151-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72151-131">-WhatIf</span></span>
<span data-ttu-id="72151-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="72151-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72151-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72151-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72151-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72151-134">CommonParameters</span></span>
<span data-ttu-id="72151-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="72151-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72151-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="72151-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72151-137">입력</span><span class="sxs-lookup"><span data-stu-id="72151-137">INPUTS</span></span>

### <span data-ttu-id="72151-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="72151-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="72151-139">System.String</span><span class="sxs-lookup"><span data-stu-id="72151-139">System.String</span></span>

## <span data-ttu-id="72151-140">출력</span><span class="sxs-lookup"><span data-stu-id="72151-140">OUTPUTS</span></span>

### <span data-ttu-id="72151-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="72151-141">System.Boolean</span></span>

## <span data-ttu-id="72151-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="72151-142">NOTES</span></span>

## <span data-ttu-id="72151-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72151-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354950"
---
# <span data-ttu-id="e2f60-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="e2f60-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="e2f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f60-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f60-103">단일 에지 디바이스에 에지 모듈을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="e2f60-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2f60-104">SYNTAX</span></span>

### <span data-ttu-id="e2f60-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2f60-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f60-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2f60-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f60-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e2f60-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2f60-108">설명</span><span class="sxs-lookup"><span data-stu-id="e2f60-108">DESCRIPTION</span></span>
<span data-ttu-id="e2f60-109">제공된 모듈 구성 콘텐츠를 지정된 에지 디바이스에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="e2f60-110">참고: 실행 시 명령은 디바이스에 적용된 모듈 컬렉션을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="e2f60-111">예제</span><span class="sxs-lookup"><span data-stu-id="e2f60-111">EXAMPLES</span></span>

### <span data-ttu-id="e2f60-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2f60-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="e2f60-113">대상 디바이스에서 모듈을 설정하여 개발하는 동안 에지 모듈을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="e2f60-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2f60-114">PARAMETERS</span></span>

### <span data-ttu-id="e2f60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f60-115">-DefaultProfile</span></span>
<span data-ttu-id="e2f60-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f60-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e2f60-117">-DeviceId</span></span>
<span data-ttu-id="e2f60-118">대상 Edge 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f60-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f60-119">-InputObject</span></span>
<span data-ttu-id="e2f60-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e2f60-120">IotHub object</span></span>

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

### <span data-ttu-id="e2f60-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e2f60-121">-IotHubName</span></span>
<span data-ttu-id="e2f60-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e2f60-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e2f60-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="e2f60-123">-ModulesContent</span></span>
<span data-ttu-id="e2f60-124">IoT Edge 디바이스에 대한 모듈의 구성 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f60-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2f60-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e2f60-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e2f60-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f60-127">-ResourceId</span></span>
<span data-ttu-id="e2f60-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e2f60-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e2f60-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f60-129">-Confirm</span></span>
<span data-ttu-id="e2f60-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f60-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f60-131">-WhatIf</span></span>
<span data-ttu-id="e2f60-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2f60-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f60-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f60-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f60-134">CommonParameters</span></span>
<span data-ttu-id="e2f60-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f60-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f60-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2f60-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f60-137">입력</span><span class="sxs-lookup"><span data-stu-id="e2f60-137">INPUTS</span></span>

### <span data-ttu-id="e2f60-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2f60-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e2f60-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e2f60-139">System.String</span></span>

## <span data-ttu-id="e2f60-140">출력</span><span class="sxs-lookup"><span data-stu-id="e2f60-140">OUTPUTS</span></span>

### <span data-ttu-id="e2f60-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="e2f60-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="e2f60-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2f60-142">NOTES</span></span>

## <span data-ttu-id="e2f60-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2f60-143">RELATED LINKS</span></span>

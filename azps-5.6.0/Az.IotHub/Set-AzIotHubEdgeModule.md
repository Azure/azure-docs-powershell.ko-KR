---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: f3bc819c7050300c82f039981b1df34010771eb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952624"
---
# <span data-ttu-id="af9c7-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="af9c7-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="af9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="af9c7-103">단일 에지 디바이스에서 에지 모듈을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="af9c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="af9c7-104">SYNTAX</span></span>

### <span data-ttu-id="af9c7-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="af9c7-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af9c7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af9c7-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af9c7-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9c7-108">설명</span><span class="sxs-lookup"><span data-stu-id="af9c7-108">DESCRIPTION</span></span>
<span data-ttu-id="af9c7-109">지정된 에지 장치에 제공된 모듈 구성 콘텐츠를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="af9c7-110">참고: 실행 시 명령은 디바이스에 적용된 모듈의 컬렉션을 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="af9c7-111">예제</span><span class="sxs-lookup"><span data-stu-id="af9c7-111">EXAMPLES</span></span>

### <span data-ttu-id="af9c7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="af9c7-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="af9c7-113">대상 디바이스에 모듈을 설정하여 개발 중 에지 모듈을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="af9c7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="af9c7-114">PARAMETERS</span></span>

### <span data-ttu-id="af9c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9c7-115">-DefaultProfile</span></span>
<span data-ttu-id="af9c7-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9c7-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="af9c7-117">-DeviceId</span></span>
<span data-ttu-id="af9c7-118">대상 에지 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="af9c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9c7-119">-InputObject</span></span>
<span data-ttu-id="af9c7-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="af9c7-120">IotHub object</span></span>

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

### <span data-ttu-id="af9c7-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="af9c7-121">-IotHubName</span></span>
<span data-ttu-id="af9c7-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="af9c7-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="af9c7-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="af9c7-123">-ModulesContent</span></span>
<span data-ttu-id="af9c7-124">IoT Edge 디바이스용 모듈의 구성 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="af9c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="af9c7-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="af9c7-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="af9c7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9c7-127">-ResourceId</span></span>
<span data-ttu-id="af9c7-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="af9c7-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="af9c7-129">-확인</span><span class="sxs-lookup"><span data-stu-id="af9c7-129">-Confirm</span></span>
<span data-ttu-id="af9c7-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9c7-131">-WhatIf</span></span>
<span data-ttu-id="af9c7-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9c7-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9c7-134">CommonParameters</span></span>
<span data-ttu-id="af9c7-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af9c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9c7-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af9c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9c7-137">입력</span><span class="sxs-lookup"><span data-stu-id="af9c7-137">INPUTS</span></span>

### <span data-ttu-id="af9c7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="af9c7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="af9c7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="af9c7-139">System.String</span></span>

## <span data-ttu-id="af9c7-140">출력</span><span class="sxs-lookup"><span data-stu-id="af9c7-140">OUTPUTS</span></span>

### <span data-ttu-id="af9c7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="af9c7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="af9c7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af9c7-142">NOTES</span></span>

## <span data-ttu-id="af9c7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af9c7-143">RELATED LINKS</span></span>

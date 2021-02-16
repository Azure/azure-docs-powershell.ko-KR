---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203876"
---
# <span data-ttu-id="96a38-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="96a38-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="96a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a38-102">SYNOPSIS</span></span>
<span data-ttu-id="96a38-103">IoT Hub의 대상 IoT 디바이스에서 모듈을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="96a38-104">구문</span><span class="sxs-lookup"><span data-stu-id="96a38-104">SYNTAX</span></span>

### <span data-ttu-id="96a38-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="96a38-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96a38-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96a38-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a38-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="96a38-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a38-108">설명</span><span class="sxs-lookup"><span data-stu-id="96a38-108">DESCRIPTION</span></span>
<span data-ttu-id="96a38-109">IoT Hub의 대상 IoT 디바이스에서 모듈을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="96a38-110">예제</span><span class="sxs-lookup"><span data-stu-id="96a38-110">EXAMPLES</span></span>

### <span data-ttu-id="96a38-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="96a38-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="96a38-112">Iot 디바이스 모듈을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="96a38-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="96a38-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="96a38-114">모든 Iot 디바이스 모듈을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="96a38-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a38-115">PARAMETERS</span></span>

### <span data-ttu-id="96a38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a38-116">-DefaultProfile</span></span>
<span data-ttu-id="96a38-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a38-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="96a38-118">-DeviceId</span></span>
<span data-ttu-id="96a38-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a38-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96a38-120">-InputObject</span></span>
<span data-ttu-id="96a38-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="96a38-121">IotHub object</span></span>

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

### <span data-ttu-id="96a38-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="96a38-122">-IotHubName</span></span>
<span data-ttu-id="96a38-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="96a38-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="96a38-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="96a38-124">-ModuleId</span></span>
<span data-ttu-id="96a38-125">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-125">Target Module Id.</span></span>

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

### <span data-ttu-id="96a38-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96a38-126">-PassThru</span></span>
<span data-ttu-id="96a38-127">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="96a38-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96a38-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a38-129">-ResourceGroupName</span></span>
<span data-ttu-id="96a38-130">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="96a38-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="96a38-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a38-131">-ResourceId</span></span>
<span data-ttu-id="96a38-132">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="96a38-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="96a38-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a38-133">-Confirm</span></span>
<span data-ttu-id="96a38-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a38-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a38-135">-WhatIf</span></span>
<span data-ttu-id="96a38-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="96a38-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a38-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a38-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a38-138">CommonParameters</span></span>
<span data-ttu-id="96a38-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96a38-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a38-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96a38-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a38-141">입력</span><span class="sxs-lookup"><span data-stu-id="96a38-141">INPUTS</span></span>

### <span data-ttu-id="96a38-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="96a38-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="96a38-143">System.String</span><span class="sxs-lookup"><span data-stu-id="96a38-143">System.String</span></span>

## <span data-ttu-id="96a38-144">출력</span><span class="sxs-lookup"><span data-stu-id="96a38-144">OUTPUTS</span></span>

### <span data-ttu-id="96a38-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96a38-145">System.Boolean</span></span>

## <span data-ttu-id="96a38-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96a38-146">NOTES</span></span>

## <span data-ttu-id="96a38-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96a38-147">RELATED LINKS</span></span>
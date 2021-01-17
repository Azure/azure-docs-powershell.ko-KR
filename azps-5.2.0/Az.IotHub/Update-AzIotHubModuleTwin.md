---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361712"
---
# <span data-ttu-id="94c71-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="94c71-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="94c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c71-102">SYNOPSIS</span></span>
<span data-ttu-id="94c71-103">IoT 디바이스 모듈 쌍의 태그 및 desired 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="94c71-104">구문</span><span class="sxs-lookup"><span data-stu-id="94c71-104">SYNTAX</span></span>

### <span data-ttu-id="94c71-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="94c71-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c71-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94c71-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94c71-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94c71-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94c71-108">설명</span><span class="sxs-lookup"><span data-stu-id="94c71-108">DESCRIPTION</span></span>
<span data-ttu-id="94c71-109">디바이스 쌍을 업데이트하거나 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="94c71-110">자세한 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94c71-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="94c71-111">예제</span><span class="sxs-lookup"><span data-stu-id="94c71-111">EXAMPLES</span></span>

### <span data-ttu-id="94c71-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="94c71-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="94c71-113">업데이트된 디바이스 모듈 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="94c71-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="94c71-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="94c71-115">업데이트된 desired 속성을 사용하여 디바이스 모듈 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="94c71-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="94c71-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="94c71-117">업데이트된 태그 속성이 있는 디바이스 모듈 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="94c71-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="94c71-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="94c71-119">대체된 디바이스 모듈 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="94c71-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94c71-120">PARAMETERS</span></span>

### <span data-ttu-id="94c71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c71-121">-DefaultProfile</span></span>
<span data-ttu-id="94c71-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c71-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="94c71-123">-Desired</span></span>
<span data-ttu-id="94c71-124">모듈 쌍에서 desired 속성을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-124">Add or update the desired property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c71-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="94c71-125">-DeviceId</span></span>
<span data-ttu-id="94c71-126">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-126">Target Device Id.</span></span>

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

### <span data-ttu-id="94c71-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94c71-127">-InputObject</span></span>
<span data-ttu-id="94c71-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="94c71-128">IotHub object</span></span>

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

### <span data-ttu-id="94c71-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="94c71-129">-IotHubName</span></span>
<span data-ttu-id="94c71-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="94c71-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="94c71-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="94c71-131">-ModuleId</span></span>
<span data-ttu-id="94c71-132">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-132">Target Module Id.</span></span>

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

### <span data-ttu-id="94c71-133">-Partial</span><span class="sxs-lookup"><span data-stu-id="94c71-133">-Partial</span></span>
<span data-ttu-id="94c71-134">모듈 쌍의 태그 및 desired 속성만 부분적으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="94c71-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c71-135">-ResourceGroupName</span></span>
<span data-ttu-id="94c71-136">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="94c71-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="94c71-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94c71-137">-ResourceId</span></span>
<span data-ttu-id="94c71-138">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="94c71-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="94c71-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="94c71-139">-Tag</span></span>
<span data-ttu-id="94c71-140">모듈 쌍에서 태그 속성을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-140">Add or update the tags property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c71-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94c71-141">-Confirm</span></span>
<span data-ttu-id="94c71-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c71-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c71-143">-WhatIf</span></span>
<span data-ttu-id="94c71-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="94c71-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c71-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c71-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c71-146">CommonParameters</span></span>
<span data-ttu-id="94c71-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94c71-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c71-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94c71-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c71-149">입력</span><span class="sxs-lookup"><span data-stu-id="94c71-149">INPUTS</span></span>

### <span data-ttu-id="94c71-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="94c71-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="94c71-151">System.String</span><span class="sxs-lookup"><span data-stu-id="94c71-151">System.String</span></span>

## <span data-ttu-id="94c71-152">출력</span><span class="sxs-lookup"><span data-stu-id="94c71-152">OUTPUTS</span></span>

### <span data-ttu-id="94c71-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="94c71-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="94c71-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94c71-154">NOTES</span></span>

## <span data-ttu-id="94c71-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94c71-155">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386415"
---
# <span data-ttu-id="82ea4-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="82ea4-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="82ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="82ea4-103">디바이스 쌍의 태그 및 desired 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="82ea4-104">구문</span><span class="sxs-lookup"><span data-stu-id="82ea4-104">SYNTAX</span></span>

### <span data-ttu-id="82ea4-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="82ea4-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ea4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82ea4-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82ea4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82ea4-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ea4-108">설명</span><span class="sxs-lookup"><span data-stu-id="82ea4-108">DESCRIPTION</span></span>
<span data-ttu-id="82ea4-109">디바이스 쌍을 업데이트하거나 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="82ea4-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82ea4-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="82ea4-111">예제</span><span class="sxs-lookup"><span data-stu-id="82ea4-111">EXAMPLES</span></span>

### <span data-ttu-id="82ea4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="82ea4-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="82ea4-113">업데이트된 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="82ea4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="82ea4-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="82ea4-115">업데이트된 desired 속성을 사용하여 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="82ea4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="82ea4-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="82ea4-117">업데이트된 태그 속성을 사용하여 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="82ea4-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="82ea4-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="82ea4-119">대체된 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="82ea4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82ea4-120">PARAMETERS</span></span>

### <span data-ttu-id="82ea4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ea4-121">-DefaultProfile</span></span>
<span data-ttu-id="82ea4-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82ea4-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="82ea4-123">-Desired</span></span>
<span data-ttu-id="82ea4-124">디바이스 쌍에서 desired 속성을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="82ea4-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="82ea4-125">-DeviceId</span></span>
<span data-ttu-id="82ea4-126">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-126">Target Device Id.</span></span>

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

### <span data-ttu-id="82ea4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82ea4-127">-InputObject</span></span>
<span data-ttu-id="82ea4-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="82ea4-128">IotHub object</span></span>

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

### <span data-ttu-id="82ea4-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="82ea4-129">-IotHubName</span></span>
<span data-ttu-id="82ea4-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="82ea4-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="82ea4-131">-Partial</span><span class="sxs-lookup"><span data-stu-id="82ea4-131">-Partial</span></span>
<span data-ttu-id="82ea4-132">디바이스 쌍의 태그 및 desired 속성만 부분적으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="82ea4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ea4-133">-ResourceGroupName</span></span>
<span data-ttu-id="82ea4-134">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="82ea4-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="82ea4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ea4-135">-ResourceId</span></span>
<span data-ttu-id="82ea4-136">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="82ea4-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="82ea4-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="82ea4-137">-Tag</span></span>
<span data-ttu-id="82ea4-138">디바이스 쌍에서 태그 속성을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="82ea4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82ea4-139">-Confirm</span></span>
<span data-ttu-id="82ea4-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ea4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ea4-141">-WhatIf</span></span>
<span data-ttu-id="82ea4-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82ea4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ea4-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ea4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ea4-144">CommonParameters</span></span>
<span data-ttu-id="82ea4-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82ea4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ea4-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82ea4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ea4-147">입력</span><span class="sxs-lookup"><span data-stu-id="82ea4-147">INPUTS</span></span>

### <span data-ttu-id="82ea4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="82ea4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="82ea4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="82ea4-149">System.String</span></span>

## <span data-ttu-id="82ea4-150">출력</span><span class="sxs-lookup"><span data-stu-id="82ea4-150">OUTPUTS</span></span>

### <span data-ttu-id="82ea4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="82ea4-151">System.String</span></span>

## <span data-ttu-id="82ea4-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82ea4-152">NOTES</span></span>

## <span data-ttu-id="82ea4-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82ea4-153">RELATED LINKS</span></span>

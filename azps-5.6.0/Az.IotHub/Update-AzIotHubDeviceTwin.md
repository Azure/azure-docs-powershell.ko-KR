---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 84f1485f84996c1c0e98768914afffd501722ab7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978480"
---
# <span data-ttu-id="fa22a-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="fa22a-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="fa22a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa22a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa22a-103">디바이스 쌍의 태그 및 원하는 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="fa22a-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa22a-104">SYNTAX</span></span>

### <span data-ttu-id="fa22a-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fa22a-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa22a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa22a-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa22a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa22a-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa22a-108">설명</span><span class="sxs-lookup"><span data-stu-id="fa22a-108">DESCRIPTION</span></span>
<span data-ttu-id="fa22a-109">디바이스 쌍을 업데이트하거나 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="fa22a-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa22a-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="fa22a-111">예제</span><span class="sxs-lookup"><span data-stu-id="fa22a-111">EXAMPLES</span></span>

### <span data-ttu-id="fa22a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa22a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="fa22a-113">업데이트된 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="fa22a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="fa22a-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="fa22a-115">업데이트된 원하는 속성으로 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="fa22a-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="fa22a-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="fa22a-117">업데이트된 태그 속성을 사용하여 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="fa22a-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="fa22a-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="fa22a-119">대체된 디바이스 쌍 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="fa22a-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa22a-120">PARAMETERS</span></span>

### <span data-ttu-id="fa22a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa22a-121">-DefaultProfile</span></span>
<span data-ttu-id="fa22a-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa22a-123">-desired</span><span class="sxs-lookup"><span data-stu-id="fa22a-123">-Desired</span></span>
<span data-ttu-id="fa22a-124">디바이스 쌍에서 원하는 속성을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="fa22a-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fa22a-125">-DeviceId</span></span>
<span data-ttu-id="fa22a-126">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-126">Target Device Id.</span></span>

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

### <span data-ttu-id="fa22a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa22a-127">-InputObject</span></span>
<span data-ttu-id="fa22a-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fa22a-128">IotHub object</span></span>

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

### <span data-ttu-id="fa22a-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fa22a-129">-IotHubName</span></span>
<span data-ttu-id="fa22a-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fa22a-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fa22a-131">-부분</span><span class="sxs-lookup"><span data-stu-id="fa22a-131">-Partial</span></span>
<span data-ttu-id="fa22a-132">디바이스 쌍의 태그 및 원하는 속성만 부분적으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="fa22a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa22a-133">-ResourceGroupName</span></span>
<span data-ttu-id="fa22a-134">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fa22a-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fa22a-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa22a-135">-ResourceId</span></span>
<span data-ttu-id="fa22a-136">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fa22a-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fa22a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa22a-137">-Tag</span></span>
<span data-ttu-id="fa22a-138">디바이스 쌍에서 태그 속성을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="fa22a-139">-확인</span><span class="sxs-lookup"><span data-stu-id="fa22a-139">-Confirm</span></span>
<span data-ttu-id="fa22a-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa22a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa22a-141">-WhatIf</span></span>
<span data-ttu-id="fa22a-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa22a-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa22a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa22a-144">CommonParameters</span></span>
<span data-ttu-id="fa22a-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa22a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa22a-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa22a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa22a-147">입력</span><span class="sxs-lookup"><span data-stu-id="fa22a-147">INPUTS</span></span>

### <span data-ttu-id="fa22a-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fa22a-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fa22a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fa22a-149">System.String</span></span>

## <span data-ttu-id="fa22a-150">출력</span><span class="sxs-lookup"><span data-stu-id="fa22a-150">OUTPUTS</span></span>

### <span data-ttu-id="fa22a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="fa22a-151">System.String</span></span>

## <span data-ttu-id="fa22a-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa22a-152">NOTES</span></span>

## <span data-ttu-id="fa22a-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa22a-153">RELATED LINKS</span></span>

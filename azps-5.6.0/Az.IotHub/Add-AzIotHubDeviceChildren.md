---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997901"
---
# <span data-ttu-id="fc4fb-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="fc4fb-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="fc4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4fb-103">에지가 아닌 디바이스를 에지 디바이스에 자식으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="fc4fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc4fb-104">SYNTAX</span></span>

### <span data-ttu-id="fc4fb-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc4fb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc4fb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc4fb-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4fb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc4fb-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4fb-108">설명</span><span class="sxs-lookup"><span data-stu-id="fc4fb-108">DESCRIPTION</span></span>
<span data-ttu-id="fc4fb-109">지정된 에지 디바이스의 자식으로 에지가 아닌 디바이스 ID의 지정된 콤마로 구분된 목록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="fc4fb-110">예제</span><span class="sxs-lookup"><span data-stu-id="fc4fb-110">EXAMPLES</span></span>

### <span data-ttu-id="fc4fb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc4fb-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="fc4fb-112">에지가 아닌 디바이스를 에지 디바이스에 자식으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="fc4fb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fc4fb-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="fc4fb-114">에지가 아닌 디바이스를 에지 디바이스에 자식으로 추가합니다. 비에지 디바이스는 이미 다른 에지 디바이스의 자식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="fc4fb-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc4fb-115">PARAMETERS</span></span>

### <span data-ttu-id="fc4fb-116">-Children</span><span class="sxs-lookup"><span data-stu-id="fc4fb-116">-Children</span></span>
<span data-ttu-id="fc4fb-117">자식 디바이스 목록(분리된 콤마)에는 에지가 아닌 디바이스만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc4fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4fb-118">-DefaultProfile</span></span>
<span data-ttu-id="fc4fb-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc4fb-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fc4fb-120">-DeviceId</span></span>
<span data-ttu-id="fc4fb-121">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-121">Id of edge device.</span></span>

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

### <span data-ttu-id="fc4fb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fc4fb-122">-Force</span></span>
<span data-ttu-id="fc4fb-123">에지가 아닌 디바이스의 부모 디바이스를 덮어 덮어 덮어 니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="fc4fb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc4fb-124">-InputObject</span></span>
<span data-ttu-id="fc4fb-125">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fc4fb-125">IotHub object</span></span>

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

### <span data-ttu-id="fc4fb-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fc4fb-126">-IotHubName</span></span>
<span data-ttu-id="fc4fb-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fc4fb-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fc4fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc4fb-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fc4fb-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc4fb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc4fb-130">-ResourceId</span></span>
<span data-ttu-id="fc4fb-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fc4fb-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fc4fb-132">-확인</span><span class="sxs-lookup"><span data-stu-id="fc4fb-132">-Confirm</span></span>
<span data-ttu-id="fc4fb-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4fb-134">-WhatIf</span></span>
<span data-ttu-id="fc4fb-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4fb-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4fb-137">CommonParameters</span></span>
<span data-ttu-id="fc4fb-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4fb-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4fb-140">입력</span><span class="sxs-lookup"><span data-stu-id="fc4fb-140">INPUTS</span></span>

### <span data-ttu-id="fc4fb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fc4fb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fc4fb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fc4fb-142">System.String</span></span>

## <span data-ttu-id="fc4fb-143">출력</span><span class="sxs-lookup"><span data-stu-id="fc4fb-143">OUTPUTS</span></span>

### <span data-ttu-id="fc4fb-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="fc4fb-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="fc4fb-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc4fb-145">NOTES</span></span>

## <span data-ttu-id="fc4fb-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc4fb-146">RELATED LINKS</span></span>

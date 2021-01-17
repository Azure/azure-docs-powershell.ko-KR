---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338894"
---
# <span data-ttu-id="0529c-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="0529c-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="0529c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0529c-102">SYNOPSIS</span></span>
<span data-ttu-id="0529c-103">에지가 아닌 디바이스를 에지 디바이스에 자식으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="0529c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0529c-104">SYNTAX</span></span>

### <span data-ttu-id="0529c-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0529c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0529c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0529c-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0529c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0529c-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0529c-108">설명</span><span class="sxs-lookup"><span data-stu-id="0529c-108">DESCRIPTION</span></span>
<span data-ttu-id="0529c-109">지정된 에지 디바이스의 자식으로 에지가 아닌 디바이스 ID의 지정된 콤마로 구분된 목록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="0529c-110">예제</span><span class="sxs-lookup"><span data-stu-id="0529c-110">EXAMPLES</span></span>

### <span data-ttu-id="0529c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0529c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="0529c-112">에지가 아닌 디바이스를 에지 디바이스에 자식으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="0529c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0529c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="0529c-114">비에지 디바이스를 에지 디바이스에 자식으로 추가합니다. 비에지 디바이스는 이미 다른 에지 디바이스의 자식입니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="0529c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0529c-115">PARAMETERS</span></span>

### <span data-ttu-id="0529c-116">-Children</span><span class="sxs-lookup"><span data-stu-id="0529c-116">-Children</span></span>
<span data-ttu-id="0529c-117">자식 디바이스 목록(콤마로 구분)에는 에지가 아닌 디바이스만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="0529c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0529c-118">-DefaultProfile</span></span>
<span data-ttu-id="0529c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0529c-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0529c-120">-DeviceId</span></span>
<span data-ttu-id="0529c-121">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-121">Id of edge device.</span></span>

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

### <span data-ttu-id="0529c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0529c-122">-Force</span></span>
<span data-ttu-id="0529c-123">비에지 디바이스의 부모 디바이스를 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="0529c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0529c-124">-InputObject</span></span>
<span data-ttu-id="0529c-125">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="0529c-125">IotHub object</span></span>

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

### <span data-ttu-id="0529c-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0529c-126">-IotHubName</span></span>
<span data-ttu-id="0529c-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="0529c-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0529c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0529c-128">-ResourceGroupName</span></span>
<span data-ttu-id="0529c-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0529c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0529c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0529c-130">-ResourceId</span></span>
<span data-ttu-id="0529c-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0529c-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0529c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0529c-132">-Confirm</span></span>
<span data-ttu-id="0529c-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0529c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0529c-134">-WhatIf</span></span>
<span data-ttu-id="0529c-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0529c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0529c-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0529c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0529c-137">CommonParameters</span></span>
<span data-ttu-id="0529c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0529c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0529c-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0529c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0529c-140">입력</span><span class="sxs-lookup"><span data-stu-id="0529c-140">INPUTS</span></span>

### <span data-ttu-id="0529c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0529c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0529c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0529c-142">System.String</span></span>

## <span data-ttu-id="0529c-143">출력</span><span class="sxs-lookup"><span data-stu-id="0529c-143">OUTPUTS</span></span>

### <span data-ttu-id="0529c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="0529c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="0529c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0529c-145">NOTES</span></span>

## <span data-ttu-id="0529c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0529c-146">RELATED LINKS</span></span>

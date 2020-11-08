---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044340"
---
# <span data-ttu-id="5db07-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="5db07-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="5db07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db07-102">SYNOPSIS</span></span>
<span data-ttu-id="5db07-103">Edge 장치에 타사 장치를 자식으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="5db07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5db07-104">SYNTAX</span></span>

### <span data-ttu-id="5db07-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5db07-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5db07-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5db07-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5db07-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db07-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5db07-108">DESCRIPTION</span></span>
<span data-ttu-id="5db07-109">Edge 장치 id의 지정 된 쉼표 구분 목록을 지정 된 edge 장치의 자식으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="5db07-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5db07-110">EXAMPLES</span></span>

### <span data-ttu-id="5db07-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5db07-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="5db07-112">Edge 장치에 타사 장치를 자식으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="5db07-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5db07-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="5db07-114">Edge 장치에 대 한 비 대 디바이스를 자식으로 추가 각각의 비 경계 장치는 이미 다른 edge 장치의 자식입니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="5db07-115">변수</span><span class="sxs-lookup"><span data-stu-id="5db07-115">PARAMETERS</span></span>

### <span data-ttu-id="5db07-116">-하위</span><span class="sxs-lookup"><span data-stu-id="5db07-116">-Children</span></span>
<span data-ttu-id="5db07-117">자식 장치 목록 (쉼표로 구분)에는 비 edge 장치만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="5db07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db07-118">-DefaultProfile</span></span>
<span data-ttu-id="5db07-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db07-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5db07-120">-DeviceId</span></span>
<span data-ttu-id="5db07-121">Edge 디바이스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-121">Id of edge device.</span></span>

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

### <span data-ttu-id="5db07-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5db07-122">-Force</span></span>
<span data-ttu-id="5db07-123">비 경계 장치의 상위 장치를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="5db07-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5db07-124">-InputObject</span></span>
<span data-ttu-id="5db07-125">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="5db07-125">IotHub object</span></span>

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

### <span data-ttu-id="5db07-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5db07-126">-IotHubName</span></span>
<span data-ttu-id="5db07-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="5db07-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5db07-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db07-128">-ResourceGroupName</span></span>
<span data-ttu-id="5db07-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5db07-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5db07-130">-ResourceId</span></span>
<span data-ttu-id="5db07-131">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5db07-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5db07-132">-확인</span><span class="sxs-lookup"><span data-stu-id="5db07-132">-Confirm</span></span>
<span data-ttu-id="5db07-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db07-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db07-134">-WhatIf</span></span>
<span data-ttu-id="5db07-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db07-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db07-137">CommonParameters</span></span>
<span data-ttu-id="5db07-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db07-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db07-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db07-140">입력</span><span class="sxs-lookup"><span data-stu-id="5db07-140">INPUTS</span></span>

### <span data-ttu-id="5db07-141">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="5db07-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5db07-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5db07-142">System.String</span></span>

## <span data-ttu-id="5db07-143">출력</span><span class="sxs-lookup"><span data-stu-id="5db07-143">OUTPUTS</span></span>

### <span data-ttu-id="5db07-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="5db07-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="5db07-145">상속자</span><span class="sxs-lookup"><span data-stu-id="5db07-145">NOTES</span></span>

## <span data-ttu-id="5db07-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5db07-146">RELATED LINKS</span></span>

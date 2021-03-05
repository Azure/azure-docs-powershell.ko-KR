---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 296793309dbcae7317353e41f9f3562a020c9be2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013008"
---
# <span data-ttu-id="e59a1-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e59a1-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="e59a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e59a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e59a1-103">에지가 아닌 디바이스를 지정된 에지 장치에서 자식으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="e59a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="e59a1-104">SYNTAX</span></span>

### <span data-ttu-id="e59a1-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e59a1-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e59a1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e59a1-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e59a1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e59a1-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e59a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="e59a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e59a1-109">에지가 아닌 모든 디바이스를 자식으로 지정한 에지 디바이스로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="e59a1-110">예제</span><span class="sxs-lookup"><span data-stu-id="e59a1-110">EXAMPLES</span></span>

### <span data-ttu-id="e59a1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e59a1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="e59a1-112">지정된 디바이스의 자식으로 언급된 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="e59a1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e59a1-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="e59a1-114">에지가 아닌 모든 디바이스를 자식 지정 에지 디바이스로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="e59a1-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e59a1-115">PARAMETERS</span></span>

### <span data-ttu-id="e59a1-116">-Children</span><span class="sxs-lookup"><span data-stu-id="e59a1-116">-Children</span></span>
<span data-ttu-id="e59a1-117">자식 디바이스 목록(분리된 콤마)에는 에지가 아닌 디바이스만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e59a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59a1-118">-DefaultProfile</span></span>
<span data-ttu-id="e59a1-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59a1-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e59a1-120">-DeviceId</span></span>
<span data-ttu-id="e59a1-121">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-121">Id of edge device.</span></span>

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

### <span data-ttu-id="e59a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e59a1-122">-InputObject</span></span>
<span data-ttu-id="e59a1-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e59a1-123">IotHub object</span></span>

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

### <span data-ttu-id="e59a1-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e59a1-124">-IotHubName</span></span>
<span data-ttu-id="e59a1-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e59a1-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e59a1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e59a1-126">-PassThru</span></span>
<span data-ttu-id="e59a1-127">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="e59a1-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e59a1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e59a1-129">-ResourceGroupName</span></span>
<span data-ttu-id="e59a1-130">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e59a1-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e59a1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e59a1-131">-ResourceId</span></span>
<span data-ttu-id="e59a1-132">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e59a1-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e59a1-133">-확인</span><span class="sxs-lookup"><span data-stu-id="e59a1-133">-Confirm</span></span>
<span data-ttu-id="e59a1-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59a1-135">-WhatIf</span></span>
<span data-ttu-id="e59a1-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e59a1-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59a1-138">CommonParameters</span></span>
<span data-ttu-id="e59a1-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e59a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59a1-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e59a1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59a1-141">입력</span><span class="sxs-lookup"><span data-stu-id="e59a1-141">INPUTS</span></span>

### <span data-ttu-id="e59a1-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e59a1-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e59a1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e59a1-143">System.String</span></span>

## <span data-ttu-id="e59a1-144">출력</span><span class="sxs-lookup"><span data-stu-id="e59a1-144">OUTPUTS</span></span>

### <span data-ttu-id="e59a1-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e59a1-145">System.Boolean</span></span>

## <span data-ttu-id="e59a1-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e59a1-146">NOTES</span></span>

## <span data-ttu-id="e59a1-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e59a1-147">RELATED LINKS</span></span>

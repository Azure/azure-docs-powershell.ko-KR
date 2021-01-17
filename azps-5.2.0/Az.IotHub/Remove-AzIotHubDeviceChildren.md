---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353042"
---
# <span data-ttu-id="179da-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="179da-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="179da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179da-102">SYNOPSIS</span></span>
<span data-ttu-id="179da-103">지정된 에지 디바이스에서 자식으로 비에지 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="179da-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="179da-104">구문</span><span class="sxs-lookup"><span data-stu-id="179da-104">SYNTAX</span></span>

### <span data-ttu-id="179da-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="179da-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="179da-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="179da-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="179da-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="179da-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="179da-108">설명</span><span class="sxs-lookup"><span data-stu-id="179da-108">DESCRIPTION</span></span>
<span data-ttu-id="179da-109">자식 지정 에지 디바이스로 모든 또는 언급된 비에지 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="179da-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="179da-110">예제</span><span class="sxs-lookup"><span data-stu-id="179da-110">EXAMPLES</span></span>

### <span data-ttu-id="179da-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="179da-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="179da-112">지정된 디바이스의 자식으로 언급된 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="179da-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="179da-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="179da-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="179da-114">자식으로 지정된 에지 디바이스로 에지가 아닌 모든 디바이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="179da-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="179da-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="179da-115">PARAMETERS</span></span>

### <span data-ttu-id="179da-116">-Children</span><span class="sxs-lookup"><span data-stu-id="179da-116">-Children</span></span>
<span data-ttu-id="179da-117">자식 디바이스 목록(콤마로 구분)에는 에지가 아닌 디바이스만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="179da-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="179da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179da-118">-DefaultProfile</span></span>
<span data-ttu-id="179da-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="179da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="179da-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="179da-120">-DeviceId</span></span>
<span data-ttu-id="179da-121">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="179da-121">Id of edge device.</span></span>

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

### <span data-ttu-id="179da-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="179da-122">-InputObject</span></span>
<span data-ttu-id="179da-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="179da-123">IotHub object</span></span>

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

### <span data-ttu-id="179da-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="179da-124">-IotHubName</span></span>
<span data-ttu-id="179da-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="179da-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="179da-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="179da-126">-PassThru</span></span>
<span data-ttu-id="179da-127">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179da-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="179da-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="179da-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="179da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="179da-129">-ResourceGroupName</span></span>
<span data-ttu-id="179da-130">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="179da-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="179da-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="179da-131">-ResourceId</span></span>
<span data-ttu-id="179da-132">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="179da-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="179da-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="179da-133">-Confirm</span></span>
<span data-ttu-id="179da-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="179da-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="179da-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="179da-135">-WhatIf</span></span>
<span data-ttu-id="179da-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="179da-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="179da-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="179da-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="179da-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179da-138">CommonParameters</span></span>
<span data-ttu-id="179da-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="179da-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179da-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="179da-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179da-141">입력</span><span class="sxs-lookup"><span data-stu-id="179da-141">INPUTS</span></span>

### <span data-ttu-id="179da-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="179da-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="179da-143">System.String</span><span class="sxs-lookup"><span data-stu-id="179da-143">System.String</span></span>

## <span data-ttu-id="179da-144">출력</span><span class="sxs-lookup"><span data-stu-id="179da-144">OUTPUTS</span></span>

### <span data-ttu-id="179da-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="179da-145">System.Boolean</span></span>

## <span data-ttu-id="179da-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="179da-146">NOTES</span></span>

## <span data-ttu-id="179da-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="179da-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 15a8f9aa8ed3c0746b402b29967999d395794fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007883"
---
# <span data-ttu-id="fa781-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="fa781-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="fa781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa781-102">SYNOPSIS</span></span>
<span data-ttu-id="fa781-103">IoT Hub 디바이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="fa781-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa781-104">SYNTAX</span></span>

### <span data-ttu-id="fa781-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fa781-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa781-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa781-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa781-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa781-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa781-108">설명</span><span class="sxs-lookup"><span data-stu-id="fa781-108">DESCRIPTION</span></span>
<span data-ttu-id="fa781-109">Iot Hub에서 모든 디바이스 또는 특정 디바이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="fa781-110">예제</span><span class="sxs-lookup"><span data-stu-id="fa781-110">EXAMPLES</span></span>

### <span data-ttu-id="fa781-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa781-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="fa781-112">모든 Iot Hub 디바이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="fa781-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fa781-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="fa781-114">Iot Hub 디바이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="fa781-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa781-115">PARAMETERS</span></span>

### <span data-ttu-id="fa781-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa781-116">-DefaultProfile</span></span>
<span data-ttu-id="fa781-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa781-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fa781-118">-DeviceId</span></span>
<span data-ttu-id="fa781-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-119">Target Device Id.</span></span>

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

### <span data-ttu-id="fa781-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa781-120">-InputObject</span></span>
<span data-ttu-id="fa781-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="fa781-121">IotHub object</span></span>

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

### <span data-ttu-id="fa781-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fa781-122">-IotHubName</span></span>
<span data-ttu-id="fa781-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="fa781-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fa781-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa781-124">-PassThru</span></span>
<span data-ttu-id="fa781-125">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="fa781-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa781-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa781-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa781-128">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fa781-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fa781-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa781-129">-ResourceId</span></span>
<span data-ttu-id="fa781-130">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fa781-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fa781-131">-확인</span><span class="sxs-lookup"><span data-stu-id="fa781-131">-Confirm</span></span>
<span data-ttu-id="fa781-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa781-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa781-133">-WhatIf</span></span>
<span data-ttu-id="fa781-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa781-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa781-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa781-136">CommonParameters</span></span>
<span data-ttu-id="fa781-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa781-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa781-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa781-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa781-139">입력</span><span class="sxs-lookup"><span data-stu-id="fa781-139">INPUTS</span></span>

### <span data-ttu-id="fa781-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fa781-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fa781-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fa781-141">System.String</span></span>

## <span data-ttu-id="fa781-142">출력</span><span class="sxs-lookup"><span data-stu-id="fa781-142">OUTPUTS</span></span>

### <span data-ttu-id="fa781-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa781-143">System.Boolean</span></span>

## <span data-ttu-id="fa781-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa781-144">NOTES</span></span>

## <span data-ttu-id="fa781-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa781-145">RELATED LINKS</span></span>

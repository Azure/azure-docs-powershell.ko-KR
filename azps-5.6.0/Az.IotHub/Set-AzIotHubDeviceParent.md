---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955835"
---
# <span data-ttu-id="b626b-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="b626b-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="b626b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b626b-102">SYNOPSIS</span></span>
<span data-ttu-id="b626b-103">지정된 장치의 부모 디바이스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="b626b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b626b-104">SYNTAX</span></span>

### <span data-ttu-id="b626b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b626b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b626b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b626b-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b626b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b626b-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b626b-108">설명</span><span class="sxs-lookup"><span data-stu-id="b626b-108">DESCRIPTION</span></span>
<span data-ttu-id="b626b-109">지정된 비에지 디바이스의 부모 디바이스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="b626b-110">예제</span><span class="sxs-lookup"><span data-stu-id="b626b-110">EXAMPLES</span></span>

### <span data-ttu-id="b626b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b626b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="b626b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b626b-112">PARAMETERS</span></span>

### <span data-ttu-id="b626b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b626b-113">-DefaultProfile</span></span>
<span data-ttu-id="b626b-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b626b-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b626b-115">-DeviceId</span></span>
<span data-ttu-id="b626b-116">비에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="b626b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b626b-117">-Force</span></span>
<span data-ttu-id="b626b-118">에지가 아닌 디바이스의 부모 디바이스를 덮어 덮어 덮어 니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="b626b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b626b-119">-InputObject</span></span>
<span data-ttu-id="b626b-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="b626b-120">IotHub object</span></span>

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

### <span data-ttu-id="b626b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b626b-121">-IotHubName</span></span>
<span data-ttu-id="b626b-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="b626b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b626b-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="b626b-123">-ParentDeviceId</span></span>
<span data-ttu-id="b626b-124">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b626b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b626b-125">-ResourceGroupName</span></span>
<span data-ttu-id="b626b-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b626b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b626b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b626b-127">-ResourceId</span></span>
<span data-ttu-id="b626b-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b626b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b626b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b626b-129">-Confirm</span></span>
<span data-ttu-id="b626b-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b626b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b626b-131">-WhatIf</span></span>
<span data-ttu-id="b626b-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b626b-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b626b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b626b-134">CommonParameters</span></span>
<span data-ttu-id="b626b-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b626b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b626b-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b626b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b626b-137">입력</span><span class="sxs-lookup"><span data-stu-id="b626b-137">INPUTS</span></span>

### <span data-ttu-id="b626b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b626b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b626b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b626b-139">System.String</span></span>

## <span data-ttu-id="b626b-140">출력</span><span class="sxs-lookup"><span data-stu-id="b626b-140">OUTPUTS</span></span>

### <span data-ttu-id="b626b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSD에비스</span><span class="sxs-lookup"><span data-stu-id="b626b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="b626b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b626b-142">NOTES</span></span>

## <span data-ttu-id="b626b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b626b-143">RELATED LINKS</span></span>

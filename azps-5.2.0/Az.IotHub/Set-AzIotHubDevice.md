---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354957"
---
# <span data-ttu-id="27128-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27128-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="27128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27128-102">SYNOPSIS</span></span>
<span data-ttu-id="27128-103">IoT Hub 디바이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27128-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="27128-104">구문</span><span class="sxs-lookup"><span data-stu-id="27128-104">SYNTAX</span></span>

### <span data-ttu-id="27128-105">ResourceSetForStatus(기본값)</span><span class="sxs-lookup"><span data-stu-id="27128-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="27128-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="27128-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="27128-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="27128-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27128-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="27128-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="27128-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="27128-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27128-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="27128-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27128-114">설명</span><span class="sxs-lookup"><span data-stu-id="27128-114">DESCRIPTION</span></span>
<span data-ttu-id="27128-115">IoT Hub 디바이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27128-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="27128-116">예제</span><span class="sxs-lookup"><span data-stu-id="27128-116">EXAMPLES</span></span>

### <span data-ttu-id="27128-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="27128-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="27128-118">디바이스에 대한 에지 기능을 니다.</span><span class="sxs-lookup"><span data-stu-id="27128-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="27128-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="27128-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="27128-120">디바이스 상태를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="27128-120">Disable device status.</span></span>

### <span data-ttu-id="27128-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="27128-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="27128-122">Iot Hub 디바이스의 권한 부여 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27128-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="27128-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27128-123">PARAMETERS</span></span>

### <span data-ttu-id="27128-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="27128-124">-AuthMethod</span></span>
<span data-ttu-id="27128-125">엔터티를 만들 권한 부여 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27128-126">-DefaultProfile</span></span>
<span data-ttu-id="27128-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27128-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="27128-128">-DeviceId</span></span>
<span data-ttu-id="27128-129">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-129">Target Device Id.</span></span>

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

### <span data-ttu-id="27128-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="27128-130">-EdgeEnabled</span></span>
<span data-ttu-id="27128-131">에지 사용률을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27128-132">-InputObject</span></span>
<span data-ttu-id="27128-133">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="27128-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27128-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27128-134">-IotHubName</span></span>
<span data-ttu-id="27128-135">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="27128-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="27128-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="27128-137">기본 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27128-138">-ResourceGroupName</span></span>
<span data-ttu-id="27128-139">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="27128-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27128-140">-ResourceId</span></span>
<span data-ttu-id="27128-141">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="27128-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27128-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="27128-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="27128-143">보조 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-144">-Status</span><span class="sxs-lookup"><span data-stu-id="27128-144">-Status</span></span>
<span data-ttu-id="27128-145">생성 시 디바이스 상태를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27128-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="27128-146">-StatusReason</span></span>
<span data-ttu-id="27128-147">디바이스 상태에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="27128-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27128-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27128-148">-Confirm</span></span>
<span data-ttu-id="27128-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27128-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27128-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27128-150">-WhatIf</span></span>
<span data-ttu-id="27128-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="27128-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27128-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27128-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27128-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27128-153">CommonParameters</span></span>
<span data-ttu-id="27128-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27128-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27128-155">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27128-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27128-156">입력</span><span class="sxs-lookup"><span data-stu-id="27128-156">INPUTS</span></span>

### <span data-ttu-id="27128-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27128-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27128-158">System.String</span><span class="sxs-lookup"><span data-stu-id="27128-158">System.String</span></span>

## <span data-ttu-id="27128-159">출력</span><span class="sxs-lookup"><span data-stu-id="27128-159">OUTPUTS</span></span>

### <span data-ttu-id="27128-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="27128-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="27128-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27128-161">NOTES</span></span>

## <span data-ttu-id="27128-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27128-162">RELATED LINKS</span></span>

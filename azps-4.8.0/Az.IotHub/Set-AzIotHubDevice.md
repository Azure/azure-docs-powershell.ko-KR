---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056707"
---
# <span data-ttu-id="ddc5e-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ddc5e-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="ddc5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc5e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc5e-103">IoT Hub 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="ddc5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ddc5e-104">SYNTAX</span></span>

### <span data-ttu-id="ddc5e-105">ResourceSetForStatus (기본값)</span><span class="sxs-lookup"><span data-stu-id="ddc5e-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="ddc5e-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="ddc5e-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ddc5e-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="ddc5e-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ddc5e-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="ddc5e-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="ddc5e-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5e-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ddc5e-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc5e-114">설명은</span><span class="sxs-lookup"><span data-stu-id="ddc5e-114">DESCRIPTION</span></span>
<span data-ttu-id="ddc5e-115">IoT Hub 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="ddc5e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ddc5e-116">EXAMPLES</span></span>

### <span data-ttu-id="ddc5e-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="ddc5e-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="ddc5e-118">장치에 대 한 edge 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="ddc5e-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="ddc5e-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="ddc5e-120">장치 상태를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-120">Disable device status.</span></span>

### <span data-ttu-id="ddc5e-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="ddc5e-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="ddc5e-122">Iot Hub 장치의 인증 유형 업데이트</span><span class="sxs-lookup"><span data-stu-id="ddc5e-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="ddc5e-123">변수</span><span class="sxs-lookup"><span data-stu-id="ddc5e-123">PARAMETERS</span></span>

### <span data-ttu-id="ddc5e-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="ddc5e-124">-AuthMethod</span></span>
<span data-ttu-id="ddc5e-125">엔터티를 만들 권한 부여 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="ddc5e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc5e-126">-DefaultProfile</span></span>
<span data-ttu-id="ddc5e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc5e-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ddc5e-128">-DeviceId</span></span>
<span data-ttu-id="ddc5e-129">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-129">Target Device Id.</span></span>

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

### <span data-ttu-id="ddc5e-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ddc5e-130">-EdgeEnabled</span></span>
<span data-ttu-id="ddc5e-131">가장자리를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="ddc5e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc5e-132">-InputObject</span></span>
<span data-ttu-id="ddc5e-133">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="ddc5e-133">IotHub object</span></span>

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

### <span data-ttu-id="ddc5e-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ddc5e-134">-IotHubName</span></span>
<span data-ttu-id="ddc5e-135">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ddc5e-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ddc5e-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ddc5e-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="ddc5e-137">기본 키에 사용할 명시적인 자체 서명 된 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="ddc5e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc5e-138">-ResourceGroupName</span></span>
<span data-ttu-id="ddc5e-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ddc5e-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc5e-140">-ResourceId</span></span>
<span data-ttu-id="ddc5e-141">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ddc5e-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ddc5e-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ddc5e-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="ddc5e-143">보조 키에 사용할 명시적인 자체 서명 된 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="ddc5e-144">-상태</span><span class="sxs-lookup"><span data-stu-id="ddc5e-144">-Status</span></span>
<span data-ttu-id="ddc5e-145">만들기에 디바이스 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="ddc5e-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="ddc5e-146">-StatusReason</span></span>
<span data-ttu-id="ddc5e-147">디바이스 상태에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-147">Description for device status.</span></span>

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

### <span data-ttu-id="ddc5e-148">-확인</span><span class="sxs-lookup"><span data-stu-id="ddc5e-148">-Confirm</span></span>
<span data-ttu-id="ddc5e-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc5e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc5e-150">-WhatIf</span></span>
<span data-ttu-id="ddc5e-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc5e-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc5e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc5e-153">CommonParameters</span></span>
<span data-ttu-id="ddc5e-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddc5e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc5e-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc5e-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc5e-156">입력</span><span class="sxs-lookup"><span data-stu-id="ddc5e-156">INPUTS</span></span>

### <span data-ttu-id="ddc5e-157">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="ddc5e-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ddc5e-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ddc5e-158">System.String</span></span>

## <span data-ttu-id="ddc5e-159">출력</span><span class="sxs-lookup"><span data-stu-id="ddc5e-159">OUTPUTS</span></span>

### <span data-ttu-id="ddc5e-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="ddc5e-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="ddc5e-161">상속자</span><span class="sxs-lookup"><span data-stu-id="ddc5e-161">NOTES</span></span>

## <span data-ttu-id="ddc5e-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddc5e-162">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044341"
---
# <span data-ttu-id="44280-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="44280-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="44280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44280-102">SYNOPSIS</span></span>
<span data-ttu-id="44280-103">IoT Hub에서 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44280-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="44280-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44280-104">SYNTAX</span></span>

### <span data-ttu-id="44280-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="44280-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44280-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44280-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44280-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44280-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44280-108">설명은</span><span class="sxs-lookup"><span data-stu-id="44280-108">DESCRIPTION</span></span>
<span data-ttu-id="44280-109">IoT Hub에서 다른 권한 부여 형식을 사용 하 여 디바이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44280-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="44280-110">예제의</span><span class="sxs-lookup"><span data-stu-id="44280-110">EXAMPLES</span></span>

### <span data-ttu-id="44280-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="44280-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="44280-112">기본 권한 부여 (공유 개인 키)를 사용 하 여 edge 사용 IoT 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44280-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="44280-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="44280-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="44280-114">사용 안 함 상태 및 이유를 사용 하 여 루트 CA 권한 부여를 사용 하 여 IoT 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44280-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="44280-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="44280-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="44280-116">Edge 사용 IoT 장치를 만들고 여기에 자식 디바이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44280-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="44280-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="44280-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="44280-118">IoT 장치를 만들고 해당 상위 장치를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44280-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="44280-119">변수</span><span class="sxs-lookup"><span data-stu-id="44280-119">PARAMETERS</span></span>

### <span data-ttu-id="44280-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="44280-120">-AuthMethod</span></span>
<span data-ttu-id="44280-121">엔터티를 만들 권한 부여 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44280-122">-하위</span><span class="sxs-lookup"><span data-stu-id="44280-122">-Children</span></span>
<span data-ttu-id="44280-123">하위 장치 목록 추가 (쉼표로 구분)에는 비 edge 장치만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44280-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="44280-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44280-124">-DefaultProfile</span></span>
<span data-ttu-id="44280-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44280-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="44280-126">-DeviceId</span></span>
<span data-ttu-id="44280-127">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-127">Target Device Id.</span></span>

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

### <span data-ttu-id="44280-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="44280-128">-EdgeEnabled</span></span>
<span data-ttu-id="44280-129">가장자리를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="44280-130">-Force</span><span class="sxs-lookup"><span data-stu-id="44280-130">-Force</span></span>
<span data-ttu-id="44280-131">비 경계 장치의 상위 장치를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="44280-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="44280-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44280-132">-InputObject</span></span>
<span data-ttu-id="44280-133">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="44280-133">IotHub object</span></span>

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

### <span data-ttu-id="44280-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="44280-134">-IotHubName</span></span>
<span data-ttu-id="44280-135">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="44280-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="44280-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="44280-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="44280-137">기본 키에 사용할 명시적인 자체 서명 된 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="44280-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44280-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="44280-138">-ParentDeviceId</span></span>
<span data-ttu-id="44280-139">Edge 디바이스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-139">Id of edge device.</span></span>

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

### <span data-ttu-id="44280-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44280-140">-ResourceGroupName</span></span>
<span data-ttu-id="44280-141">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44280-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44280-142">-ResourceId</span></span>
<span data-ttu-id="44280-143">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="44280-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="44280-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="44280-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="44280-145">보조 키에 사용할 명시적인 자체 서명 된 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="44280-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="44280-146">-상태</span><span class="sxs-lookup"><span data-stu-id="44280-146">-Status</span></span>
<span data-ttu-id="44280-147">만들기에 디바이스 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44280-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44280-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="44280-148">-StatusReason</span></span>
<span data-ttu-id="44280-149">디바이스 상태에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="44280-149">Description for device status.</span></span>

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

### <span data-ttu-id="44280-150">-확인</span><span class="sxs-lookup"><span data-stu-id="44280-150">-Confirm</span></span>
<span data-ttu-id="44280-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44280-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44280-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44280-152">-WhatIf</span></span>
<span data-ttu-id="44280-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44280-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44280-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44280-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44280-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44280-155">CommonParameters</span></span>
<span data-ttu-id="44280-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44280-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44280-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44280-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44280-158">입력</span><span class="sxs-lookup"><span data-stu-id="44280-158">INPUTS</span></span>

### <span data-ttu-id="44280-159">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="44280-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="44280-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44280-160">System.String</span></span>

## <span data-ttu-id="44280-161">출력</span><span class="sxs-lookup"><span data-stu-id="44280-161">OUTPUTS</span></span>

### <span data-ttu-id="44280-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="44280-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="44280-163">상속자</span><span class="sxs-lookup"><span data-stu-id="44280-163">NOTES</span></span>

## <span data-ttu-id="44280-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44280-164">RELATED LINKS</span></span>

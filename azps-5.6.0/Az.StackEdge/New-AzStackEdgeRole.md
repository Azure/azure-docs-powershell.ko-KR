---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: 785c092333d0e083ed3ee356a0c4e76d6188b96b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005264"
---
# <span data-ttu-id="a76fe-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a76fe-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="a76fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a76fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a76fe-103">디바이스에 대한 새 역할 생성</span><span class="sxs-lookup"><span data-stu-id="a76fe-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="a76fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="a76fe-104">SYNTAX</span></span>

### <span data-ttu-id="a76fe-105">ConnectionStringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a76fe-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76fe-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="a76fe-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a76fe-107">설명</span><span class="sxs-lookup"><span data-stu-id="a76fe-107">DESCRIPTION</span></span>
<span data-ttu-id="a76fe-108">**New-AzStackEdgeRole** cmdlet은 Stack Edge 디바이스에 대한 새 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a76fe-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="a76fe-109">예제</span><span class="sxs-lookup"><span data-stu-id="a76fe-109">EXAMPLES</span></span>

### <span data-ttu-id="a76fe-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a76fe-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="a76fe-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a76fe-111">PARAMETERS</span></span>

### <span data-ttu-id="a76fe-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a76fe-112">-AsJob</span></span>
<span data-ttu-id="a76fe-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a76fe-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a76fe-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a76fe-114">-ConnectionString</span></span>
<span data-ttu-id="a76fe-115">연결 문자열을 제공</span><span class="sxs-lookup"><span data-stu-id="a76fe-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76fe-116">-DefaultProfile</span></span>
<span data-ttu-id="a76fe-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a76fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a76fe-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a76fe-118">-DeviceName</span></span>
<span data-ttu-id="a76fe-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="a76fe-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="a76fe-120">-DeviceProperty</span></span>
<span data-ttu-id="a76fe-121">디바이스 속성을 제공하려면</span><span class="sxs-lookup"><span data-stu-id="a76fe-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a76fe-122">-EncryptionKey</span></span>
<span data-ttu-id="a76fe-123">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="a76fe-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="a76fe-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="a76fe-125">Iot Device Access 키</span><span class="sxs-lookup"><span data-stu-id="a76fe-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a76fe-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="a76fe-127">IOT 디바이스의 연결 문자열을 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="a76fe-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="a76fe-128">-IotDeviceId</span></span>
<span data-ttu-id="a76fe-129">Iot 디바이스의 디바이스 ID</span><span class="sxs-lookup"><span data-stu-id="a76fe-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="a76fe-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="a76fe-131">Iot Edge 디바이스의 액세스 키</span><span class="sxs-lookup"><span data-stu-id="a76fe-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a76fe-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="a76fe-133">Edge Device의 연결 문자열을 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="a76fe-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="a76fe-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="a76fe-135">Iot Edge 디바이스의 ID</span><span class="sxs-lookup"><span data-stu-id="a76fe-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="a76fe-136">-IotHostHub</span></span>
<span data-ttu-id="a76fe-137">호스트hub 주소</span><span class="sxs-lookup"><span data-stu-id="a76fe-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a76fe-138">-Name</span></span>
<span data-ttu-id="a76fe-139">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="a76fe-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="a76fe-140">-Platform</span></span>
<span data-ttu-id="a76fe-141">예: Linux의 경우 플랫폼 제공</span><span class="sxs-lookup"><span data-stu-id="a76fe-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="a76fe-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76fe-142">-ResourceGroupName</span></span>
<span data-ttu-id="a76fe-143">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a76fe-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76fe-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="a76fe-144">-RoleStatus</span></span>
<span data-ttu-id="a76fe-145">상태 사용/사용 안 하도록 설정 제공</span><span class="sxs-lookup"><span data-stu-id="a76fe-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="a76fe-146">-확인</span><span class="sxs-lookup"><span data-stu-id="a76fe-146">-Confirm</span></span>
<span data-ttu-id="a76fe-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a76fe-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76fe-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76fe-148">-WhatIf</span></span>
<span data-ttu-id="a76fe-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a76fe-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a76fe-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a76fe-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76fe-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76fe-151">CommonParameters</span></span>
<span data-ttu-id="a76fe-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a76fe-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76fe-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a76fe-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76fe-154">입력</span><span class="sxs-lookup"><span data-stu-id="a76fe-154">INPUTS</span></span>

### <span data-ttu-id="a76fe-155">없음</span><span class="sxs-lookup"><span data-stu-id="a76fe-155">None</span></span>

## <span data-ttu-id="a76fe-156">출력</span><span class="sxs-lookup"><span data-stu-id="a76fe-156">OUTPUTS</span></span>

### <span data-ttu-id="a76fe-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="a76fe-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="a76fe-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a76fe-158">NOTES</span></span>

## <span data-ttu-id="a76fe-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a76fe-159">RELATED LINKS</span></span>

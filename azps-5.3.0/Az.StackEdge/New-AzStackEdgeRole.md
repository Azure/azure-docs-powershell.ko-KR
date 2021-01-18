---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495528"
---
# <span data-ttu-id="591d3-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="591d3-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="591d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591d3-102">SYNOPSIS</span></span>
<span data-ttu-id="591d3-103">디바이스에 대한 새 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="591d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="591d3-104">SYNTAX</span></span>

### <span data-ttu-id="591d3-105">ConnectionStringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="591d3-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591d3-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="591d3-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="591d3-107">설명</span><span class="sxs-lookup"><span data-stu-id="591d3-107">DESCRIPTION</span></span>
<span data-ttu-id="591d3-108">**New-AzStackEdgeRole** cmdlet은 Stack Edge 디바이스에 대한 새 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="591d3-109">예제</span><span class="sxs-lookup"><span data-stu-id="591d3-109">EXAMPLES</span></span>

### <span data-ttu-id="591d3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="591d3-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="591d3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591d3-111">PARAMETERS</span></span>

### <span data-ttu-id="591d3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="591d3-112">-AsJob</span></span>
<span data-ttu-id="591d3-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="591d3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="591d3-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="591d3-114">-ConnectionString</span></span>
<span data-ttu-id="591d3-115">연결 문자열을 제공</span><span class="sxs-lookup"><span data-stu-id="591d3-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="591d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591d3-116">-DefaultProfile</span></span>
<span data-ttu-id="591d3-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="591d3-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="591d3-118">-DeviceName</span></span>
<span data-ttu-id="591d3-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="591d3-119">Device Name</span></span>

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

### <span data-ttu-id="591d3-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="591d3-120">-DeviceProperty</span></span>
<span data-ttu-id="591d3-121">디바이스 속성을 제공하려면</span><span class="sxs-lookup"><span data-stu-id="591d3-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="591d3-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="591d3-122">-EncryptionKey</span></span>
<span data-ttu-id="591d3-123">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="591d3-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="591d3-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="591d3-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="591d3-125">Iot 디바이스 액세스 키</span><span class="sxs-lookup"><span data-stu-id="591d3-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="591d3-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="591d3-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="591d3-127">IOT 디바이스의 연결 문자열을 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="591d3-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="591d3-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="591d3-128">-IotDeviceId</span></span>
<span data-ttu-id="591d3-129">Iot 디바이스의 디바이스 ID</span><span class="sxs-lookup"><span data-stu-id="591d3-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="591d3-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="591d3-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="591d3-131">Iot Edge 디바이스의 액세스 키</span><span class="sxs-lookup"><span data-stu-id="591d3-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="591d3-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="591d3-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="591d3-133">Edge 디바이스의 연결 문자열을 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="591d3-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="591d3-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="591d3-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="591d3-135">Iot Edge 디바이스의 ID</span><span class="sxs-lookup"><span data-stu-id="591d3-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="591d3-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="591d3-136">-IotHostHub</span></span>
<span data-ttu-id="591d3-137">Hosthub 주소</span><span class="sxs-lookup"><span data-stu-id="591d3-137">Hosthub address</span></span>

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

### <span data-ttu-id="591d3-138">-Name</span><span class="sxs-lookup"><span data-stu-id="591d3-138">-Name</span></span>
<span data-ttu-id="591d3-139">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="591d3-139">Resource Name</span></span>

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

### <span data-ttu-id="591d3-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="591d3-140">-Platform</span></span>
<span data-ttu-id="591d3-141">Linux의 경우 플랫폼을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="591d3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591d3-142">-ResourceGroupName</span></span>
<span data-ttu-id="591d3-143">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="591d3-143">Resource Group Name</span></span>

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

### <span data-ttu-id="591d3-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="591d3-144">-RoleStatus</span></span>
<span data-ttu-id="591d3-145">사용/사용 안 하도록 상태 제공</span><span class="sxs-lookup"><span data-stu-id="591d3-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="591d3-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="591d3-146">-Confirm</span></span>
<span data-ttu-id="591d3-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591d3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591d3-148">-WhatIf</span></span>
<span data-ttu-id="591d3-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="591d3-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="591d3-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591d3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591d3-151">CommonParameters</span></span>
<span data-ttu-id="591d3-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="591d3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591d3-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="591d3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591d3-154">입력</span><span class="sxs-lookup"><span data-stu-id="591d3-154">INPUTS</span></span>

### <span data-ttu-id="591d3-155">없음</span><span class="sxs-lookup"><span data-stu-id="591d3-155">None</span></span>

## <span data-ttu-id="591d3-156">출력</span><span class="sxs-lookup"><span data-stu-id="591d3-156">OUTPUTS</span></span>

### <span data-ttu-id="591d3-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="591d3-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="591d3-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="591d3-158">NOTES</span></span>

## <span data-ttu-id="591d3-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="591d3-159">RELATED LINKS</span></span>

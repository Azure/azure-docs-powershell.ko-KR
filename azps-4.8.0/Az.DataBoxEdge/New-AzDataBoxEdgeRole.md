---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212552"
---
# <span data-ttu-id="e4c04-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e4c04-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="e4c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c04-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c04-103">장치에 대 한 새 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="e4c04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4c04-104">SYNTAX</span></span>

### <span data-ttu-id="e4c04-105">ConnectionStringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4c04-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c04-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c04-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4c04-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4c04-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c04-108">**AzDataBoxEdgeRole** Cmdlet은 데이터 상자 가장자리 장치에 대 한 새 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="e4c04-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e4c04-109">EXAMPLES</span></span>

### <span data-ttu-id="e4c04-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4c04-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="e4c04-111">변수</span><span class="sxs-lookup"><span data-stu-id="e4c04-111">PARAMETERS</span></span>

### <span data-ttu-id="e4c04-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4c04-112">-AsJob</span></span>
<span data-ttu-id="e4c04-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e4c04-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4c04-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4c04-114">-ConnectionString</span></span>
<span data-ttu-id="e4c04-115">연결 문자열을 제공 하려면</span><span class="sxs-lookup"><span data-stu-id="e4c04-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="e4c04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c04-116">-DefaultProfile</span></span>
<span data-ttu-id="e4c04-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c04-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="e4c04-118">-DeviceName</span></span>
<span data-ttu-id="e4c04-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="e4c04-119">Device Name</span></span>

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

### <span data-ttu-id="e4c04-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="e4c04-120">-DeviceProperty</span></span>
<span data-ttu-id="e4c04-121">장치 속성을 제공 하려면</span><span class="sxs-lookup"><span data-stu-id="e4c04-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="e4c04-122">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="e4c04-122">-EncryptionKey</span></span>
<span data-ttu-id="e4c04-123">Edge 장치의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="e4c04-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="e4c04-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="e4c04-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="e4c04-125">Iot 장치 선택 키</span><span class="sxs-lookup"><span data-stu-id="e4c04-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="e4c04-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4c04-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="e4c04-127">IOT 디바이스의 연결 문자열을 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4c04-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="e4c04-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="e4c04-128">-IotDeviceId</span></span>
<span data-ttu-id="e4c04-129">Iot 장치의 장치 Id</span><span class="sxs-lookup"><span data-stu-id="e4c04-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="e4c04-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="e4c04-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="e4c04-131">Iot Edge 장치의 선택 키</span><span class="sxs-lookup"><span data-stu-id="e4c04-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="e4c04-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4c04-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="e4c04-133">Edge 장치의 연결 문자열을 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4c04-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="e4c04-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="e4c04-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="e4c04-135">Iot Edge 장치의 Id</span><span class="sxs-lookup"><span data-stu-id="e4c04-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="e4c04-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="e4c04-136">-IotHostHub</span></span>
<span data-ttu-id="e4c04-137">Hosthub 주소</span><span class="sxs-lookup"><span data-stu-id="e4c04-137">Hosthub address</span></span>

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

### <span data-ttu-id="e4c04-138">-이름</span><span class="sxs-lookup"><span data-stu-id="e4c04-138">-Name</span></span>
<span data-ttu-id="e4c04-139">자원 이름</span><span class="sxs-lookup"><span data-stu-id="e4c04-139">Resource Name</span></span>

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

### <span data-ttu-id="e4c04-140">-플랫폼</span><span class="sxs-lookup"><span data-stu-id="e4c04-140">-Platform</span></span>
<span data-ttu-id="e4c04-141">플랫폼을 제공 합니다 (예: Linux).</span><span class="sxs-lookup"><span data-stu-id="e4c04-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="e4c04-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c04-142">-ResourceGroupName</span></span>
<span data-ttu-id="e4c04-143">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e4c04-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c04-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="e4c04-144">-RoleStatus</span></span>
<span data-ttu-id="e4c04-145">상태를 사용/사용 안 함으로 지정</span><span class="sxs-lookup"><span data-stu-id="e4c04-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="e4c04-146">-확인</span><span class="sxs-lookup"><span data-stu-id="e4c04-146">-Confirm</span></span>
<span data-ttu-id="e4c04-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c04-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c04-148">-WhatIf</span></span>
<span data-ttu-id="e4c04-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4c04-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c04-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c04-151">CommonParameters</span></span>
<span data-ttu-id="e4c04-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c04-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c04-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4c04-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c04-154">입력</span><span class="sxs-lookup"><span data-stu-id="e4c04-154">INPUTS</span></span>

### <span data-ttu-id="e4c04-155">않아야</span><span class="sxs-lookup"><span data-stu-id="e4c04-155">None</span></span>

## <span data-ttu-id="e4c04-156">출력</span><span class="sxs-lookup"><span data-stu-id="e4c04-156">OUTPUTS</span></span>

### <span data-ttu-id="e4c04-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e4c04-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e4c04-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e4c04-158">NOTES</span></span>

## <span data-ttu-id="e4c04-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4c04-159">RELATED LINKS</span></span>

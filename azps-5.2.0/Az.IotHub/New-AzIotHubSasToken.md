---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334521"
---
# <span data-ttu-id="b9ef6-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="b9ef6-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="b9ef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ef6-103">대상 IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="b9ef6-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9ef6-104">SYNTAX</span></span>

### <span data-ttu-id="b9ef6-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9ef6-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ef6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9ef6-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9ef6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b9ef6-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9ef6-108">설명</span><span class="sxs-lookup"><span data-stu-id="b9ef6-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ef6-109">디바이스 SAS 토큰의 경우 정책 매개 변수는 디바이스 레지스트리에만 액세스하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="b9ef6-110">따라서 정책은 레지스트리에 대한 읽기 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="b9ef6-111">IoT Hub 토큰의 경우 정책은 SAS의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="b9ef6-112">예제</span><span class="sxs-lookup"><span data-stu-id="b9ef6-112">EXAMPLES</span></span>

### <span data-ttu-id="b9ef6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9ef6-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="b9ef6-114">iothubowner 정책 및 기본 키를 사용하여 IoT Hub SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="b9ef6-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b9ef6-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="b9ef6-116">registryRead 정책 및 보조 키를 사용하여 IoT Hub SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="b9ef6-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="b9ef6-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="b9ef6-118">iothubowner 정책을 사용하여 {iothub_name} 디바이스 레지스트리에 액세스하는 디바이스 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="b9ef6-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="b9ef6-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="b9ef6-120">iothubowner 정책을 사용하여 {iothub_name} 디바이스 레지스트리에 액세스하는 모듈 SAS 토큰을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="b9ef6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9ef6-121">PARAMETERS</span></span>

### <span data-ttu-id="b9ef6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ef6-122">-DefaultProfile</span></span>
<span data-ttu-id="b9ef6-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ef6-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b9ef6-124">-DeviceId</span></span>
<span data-ttu-id="b9ef6-125">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-125">Target Device Id.</span></span>

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

### <span data-ttu-id="b9ef6-126">-Duration</span><span class="sxs-lookup"><span data-stu-id="b9ef6-126">-Duration</span></span>
<span data-ttu-id="b9ef6-127">생성될 토큰의 향후 만료(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="b9ef6-128">기본값은 3600입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ef6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9ef6-129">-InputObject</span></span>
<span data-ttu-id="b9ef6-130">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="b9ef6-130">IotHub object</span></span>

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

### <span data-ttu-id="b9ef6-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b9ef6-131">-IotHubName</span></span>
<span data-ttu-id="b9ef6-132">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="b9ef6-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b9ef6-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b9ef6-133">-KeyName</span></span>
<span data-ttu-id="b9ef6-134">액세스 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-134">Access key name.</span></span>

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

### <span data-ttu-id="b9ef6-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b9ef6-135">-KeyType</span></span>
<span data-ttu-id="b9ef6-136">선택키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ef6-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="b9ef6-137">-ModuleId</span></span>
<span data-ttu-id="b9ef6-138">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-138">Target Module Id.</span></span>

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

### <span data-ttu-id="b9ef6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ef6-139">-ResourceGroupName</span></span>
<span data-ttu-id="b9ef6-140">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b9ef6-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b9ef6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ef6-141">-ResourceId</span></span>
<span data-ttu-id="b9ef6-142">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b9ef6-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b9ef6-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9ef6-143">-Confirm</span></span>
<span data-ttu-id="b9ef6-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ef6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ef6-145">-WhatIf</span></span>
<span data-ttu-id="b9ef6-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b9ef6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ef6-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ef6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ef6-148">CommonParameters</span></span>
<span data-ttu-id="b9ef6-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ef6-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9ef6-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ef6-151">입력</span><span class="sxs-lookup"><span data-stu-id="b9ef6-151">INPUTS</span></span>

### <span data-ttu-id="b9ef6-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b9ef6-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b9ef6-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b9ef6-153">System.String</span></span>

## <span data-ttu-id="b9ef6-154">출력</span><span class="sxs-lookup"><span data-stu-id="b9ef6-154">OUTPUTS</span></span>

### <span data-ttu-id="b9ef6-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b9ef6-155">System.String</span></span>

## <span data-ttu-id="b9ef6-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9ef6-156">NOTES</span></span>

## <span data-ttu-id="b9ef6-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9ef6-157">RELATED LINKS</span></span>

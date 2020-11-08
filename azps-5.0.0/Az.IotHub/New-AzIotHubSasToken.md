---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217735"
---
# <span data-ttu-id="5fe69-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="5fe69-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="5fe69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe69-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe69-103">대상 IoT Hub, 장치 또는 모듈에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="5fe69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5fe69-104">SYNTAX</span></span>

### <span data-ttu-id="5fe69-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5fe69-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fe69-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fe69-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fe69-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5fe69-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe69-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5fe69-108">DESCRIPTION</span></span>
<span data-ttu-id="5fe69-109">장치 SAS 토큰의 경우 정책 매개 변수는 장치 레지스트리에만 액세스 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="5fe69-110">따라서 정책에는 레지스트리에 대 한 읽기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="5fe69-111">IoT Hub 토큰의 경우 정책은 SA의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="5fe69-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5fe69-112">EXAMPLES</span></span>

### <span data-ttu-id="5fe69-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="5fe69-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="5fe69-114">Iothubowner 정책 및 기본 키를 사용 하 여 IoT Hub SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="5fe69-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="5fe69-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="5fe69-116">RegistryRead 정책 및 보조 키를 사용 하 여 IoT Hub SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="5fe69-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="5fe69-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="5fe69-118">Iothubowner 정책을 사용 하 여 {iothub_name} 장치 레지스트리에 액세스 하는 디바이스 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="5fe69-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="5fe69-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="5fe69-120">Iothubowner 정책을 사용 하 여 {iothub_name} 장치 레지스트리에 액세스 하는 모듈 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="5fe69-121">변수</span><span class="sxs-lookup"><span data-stu-id="5fe69-121">PARAMETERS</span></span>

### <span data-ttu-id="5fe69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe69-122">-DefaultProfile</span></span>
<span data-ttu-id="5fe69-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe69-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5fe69-124">-DeviceId</span></span>
<span data-ttu-id="5fe69-125">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-125">Target Device Id.</span></span>

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

### <span data-ttu-id="5fe69-126">-기간</span><span class="sxs-lookup"><span data-stu-id="5fe69-126">-Duration</span></span>
<span data-ttu-id="5fe69-127">생성 되는 토큰의 이후 만료 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="5fe69-128">기본값은 3600입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-128">Default is 3600.</span></span>

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

### <span data-ttu-id="5fe69-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fe69-129">-InputObject</span></span>
<span data-ttu-id="5fe69-130">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="5fe69-130">IotHub object</span></span>

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

### <span data-ttu-id="5fe69-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5fe69-131">-IotHubName</span></span>
<span data-ttu-id="5fe69-132">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="5fe69-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5fe69-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5fe69-133">-KeyName</span></span>
<span data-ttu-id="5fe69-134">선택 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-134">Access key name.</span></span>

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

### <span data-ttu-id="5fe69-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5fe69-135">-KeyType</span></span>
<span data-ttu-id="5fe69-136">선택 키 형식.</span><span class="sxs-lookup"><span data-stu-id="5fe69-136">Access key type.</span></span>

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

### <span data-ttu-id="5fe69-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="5fe69-137">-ModuleId</span></span>
<span data-ttu-id="5fe69-138">대상 모듈 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-138">Target Module Id.</span></span>

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

### <span data-ttu-id="5fe69-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe69-139">-ResourceGroupName</span></span>
<span data-ttu-id="5fe69-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5fe69-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fe69-141">-ResourceId</span></span>
<span data-ttu-id="5fe69-142">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5fe69-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5fe69-143">-확인</span><span class="sxs-lookup"><span data-stu-id="5fe69-143">-Confirm</span></span>
<span data-ttu-id="5fe69-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe69-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe69-145">-WhatIf</span></span>
<span data-ttu-id="5fe69-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe69-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe69-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe69-148">CommonParameters</span></span>
<span data-ttu-id="5fe69-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fe69-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe69-150">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe69-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe69-151">입력</span><span class="sxs-lookup"><span data-stu-id="5fe69-151">INPUTS</span></span>

### <span data-ttu-id="5fe69-152">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="5fe69-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5fe69-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5fe69-153">System.String</span></span>

## <span data-ttu-id="5fe69-154">출력</span><span class="sxs-lookup"><span data-stu-id="5fe69-154">OUTPUTS</span></span>

### <span data-ttu-id="5fe69-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5fe69-155">System.String</span></span>

## <span data-ttu-id="5fe69-156">상속자</span><span class="sxs-lookup"><span data-stu-id="5fe69-156">NOTES</span></span>

## <span data-ttu-id="5fe69-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fe69-157">RELATED LINKS</span></span>

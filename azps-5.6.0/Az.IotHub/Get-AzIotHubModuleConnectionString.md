---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987947"
---
# <span data-ttu-id="21a18-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="21a18-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="21a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21a18-102">SYNOPSIS</span></span>
<span data-ttu-id="21a18-103">Iot Hub에서 대상 IoT 디바이스 모듈의 연결 문자열을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="21a18-104">구문</span><span class="sxs-lookup"><span data-stu-id="21a18-104">SYNTAX</span></span>

### <span data-ttu-id="21a18-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="21a18-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a18-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="21a18-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a18-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="21a18-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a18-108">설명</span><span class="sxs-lookup"><span data-stu-id="21a18-108">DESCRIPTION</span></span>
<span data-ttu-id="21a18-109">모든 모듈의 연결 문자열 또는 Azure IoT Hub 내에 포함된 대상 IoT 디바이스의 지정된 모듈을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="21a18-110">예제</span><span class="sxs-lookup"><span data-stu-id="21a18-110">EXAMPLES</span></span>

### <span data-ttu-id="21a18-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="21a18-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="21a18-112">Iot Hub에서 대상 IoT 디바이스의 모든 모듈 연결 문자열을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="21a18-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="21a18-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="21a18-114">Iot Hub에서 대상 IoT 디바이스의 보조 모듈 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="21a18-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21a18-115">PARAMETERS</span></span>

### <span data-ttu-id="21a18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a18-116">-DefaultProfile</span></span>
<span data-ttu-id="21a18-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a18-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="21a18-118">-DeviceId</span></span>
<span data-ttu-id="21a18-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-119">Target Device Id.</span></span>

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

### <span data-ttu-id="21a18-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a18-120">-InputObject</span></span>
<span data-ttu-id="21a18-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="21a18-121">IotHub object</span></span>

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

### <span data-ttu-id="21a18-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="21a18-122">-IotHubName</span></span>
<span data-ttu-id="21a18-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="21a18-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="21a18-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="21a18-124">-KeyType</span></span>
<span data-ttu-id="21a18-125">공개에 대한 공유 액세스 정책 키 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="21a18-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="21a18-126">-ModuleId</span></span>
<span data-ttu-id="21a18-127">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-127">Target Module Id.</span></span>

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

### <span data-ttu-id="21a18-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a18-128">-ResourceGroupName</span></span>
<span data-ttu-id="21a18-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="21a18-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="21a18-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21a18-130">-ResourceId</span></span>
<span data-ttu-id="21a18-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="21a18-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="21a18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a18-132">CommonParameters</span></span>
<span data-ttu-id="21a18-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21a18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a18-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21a18-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a18-135">입력</span><span class="sxs-lookup"><span data-stu-id="21a18-135">INPUTS</span></span>

### <span data-ttu-id="21a18-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="21a18-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="21a18-137">System.String</span><span class="sxs-lookup"><span data-stu-id="21a18-137">System.String</span></span>

## <span data-ttu-id="21a18-138">출력</span><span class="sxs-lookup"><span data-stu-id="21a18-138">OUTPUTS</span></span>

### <span data-ttu-id="21a18-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="21a18-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="21a18-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21a18-140">NOTES</span></span>

## <span data-ttu-id="21a18-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21a18-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348093"
---
# <span data-ttu-id="d5512-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="d5512-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="d5512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5512-102">SYNOPSIS</span></span>
<span data-ttu-id="d5512-103">IoT Hub에서 대상 IoT 디바이스 모듈의 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="d5512-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5512-104">SYNTAX</span></span>

### <span data-ttu-id="d5512-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d5512-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5512-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5512-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5512-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5512-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5512-108">설명</span><span class="sxs-lookup"><span data-stu-id="d5512-108">DESCRIPTION</span></span>
<span data-ttu-id="d5512-109">Azure IoT Hub 내에 포함된 대상 IoT 디바이스의 모든 모듈 또는 지정된 모듈의 연결 문자열을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="d5512-110">예제</span><span class="sxs-lookup"><span data-stu-id="d5512-110">EXAMPLES</span></span>

### <span data-ttu-id="d5512-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5512-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="d5512-112">IoT Hub에서 대상 IoT 디바이스의 모든 모듈 연결 문자열을 보여 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="d5512-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d5512-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="d5512-114">IoT Hub에서 대상 IoT 디바이스의 보조 모듈 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="d5512-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5512-115">PARAMETERS</span></span>

### <span data-ttu-id="d5512-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5512-116">-DefaultProfile</span></span>
<span data-ttu-id="d5512-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5512-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d5512-118">-DeviceId</span></span>
<span data-ttu-id="d5512-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-119">Target Device Id.</span></span>

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

### <span data-ttu-id="d5512-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5512-120">-InputObject</span></span>
<span data-ttu-id="d5512-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d5512-121">IotHub object</span></span>

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

### <span data-ttu-id="d5512-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d5512-122">-IotHubName</span></span>
<span data-ttu-id="d5512-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d5512-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d5512-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d5512-124">-KeyType</span></span>
<span data-ttu-id="d5512-125">공유 액세스 정책 키 형식(auth)입니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="d5512-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="d5512-126">-ModuleId</span></span>
<span data-ttu-id="d5512-127">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-127">Target Module Id.</span></span>

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

### <span data-ttu-id="d5512-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5512-128">-ResourceGroupName</span></span>
<span data-ttu-id="d5512-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d5512-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d5512-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5512-130">-ResourceId</span></span>
<span data-ttu-id="d5512-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d5512-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d5512-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5512-132">CommonParameters</span></span>
<span data-ttu-id="d5512-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5512-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5512-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d5512-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5512-135">입력</span><span class="sxs-lookup"><span data-stu-id="d5512-135">INPUTS</span></span>

### <span data-ttu-id="d5512-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d5512-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d5512-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d5512-137">System.String</span></span>

## <span data-ttu-id="d5512-138">출력</span><span class="sxs-lookup"><span data-stu-id="d5512-138">OUTPUTS</span></span>

### <span data-ttu-id="d5512-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="d5512-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="d5512-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5512-140">NOTES</span></span>

## <span data-ttu-id="d5512-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5512-141">RELATED LINKS</span></span>

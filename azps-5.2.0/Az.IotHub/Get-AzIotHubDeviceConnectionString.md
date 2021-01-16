---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329978"
---
# <span data-ttu-id="dbbe6-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="dbbe6-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="dbbe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbe6-103">IoT Hub에서 대상 IoT 디바이스의 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="dbbe6-104">구문</span><span class="sxs-lookup"><span data-stu-id="dbbe6-104">SYNTAX</span></span>

### <span data-ttu-id="dbbe6-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dbbe6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbe6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbbe6-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbbe6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dbbe6-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbbe6-108">설명</span><span class="sxs-lookup"><span data-stu-id="dbbe6-108">DESCRIPTION</span></span>
<span data-ttu-id="dbbe6-109">Azure IoT Hub 내에 포함된 모든 디바이스 또는 대상 IoT 디바이스의 연결 문자열을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="dbbe6-110">예제</span><span class="sxs-lookup"><span data-stu-id="dbbe6-110">EXAMPLES</span></span>

### <span data-ttu-id="dbbe6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbbe6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="dbbe6-112">Iot Hub의 모든 디바이스 연결 문자열을 보여 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="dbbe6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dbbe6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="dbbe6-114">IoT 디바이스의 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="dbbe6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbbe6-115">PARAMETERS</span></span>

### <span data-ttu-id="dbbe6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbe6-116">-DefaultProfile</span></span>
<span data-ttu-id="dbbe6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbbe6-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="dbbe6-118">-DeviceId</span></span>
<span data-ttu-id="dbbe6-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-119">Target Device Id.</span></span>

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

### <span data-ttu-id="dbbe6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbbe6-120">-InputObject</span></span>
<span data-ttu-id="dbbe6-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="dbbe6-121">IotHub object</span></span>

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

### <span data-ttu-id="dbbe6-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dbbe6-122">-IotHubName</span></span>
<span data-ttu-id="dbbe6-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="dbbe6-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dbbe6-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="dbbe6-124">-KeyType</span></span>
<span data-ttu-id="dbbe6-125">공유 액세스 정책 키 형식(auth)입니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="dbbe6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbbe6-126">-ResourceGroupName</span></span>
<span data-ttu-id="dbbe6-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="dbbe6-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dbbe6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbbe6-128">-ResourceId</span></span>
<span data-ttu-id="dbbe6-129">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dbbe6-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dbbe6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbe6-130">CommonParameters</span></span>
<span data-ttu-id="dbbe6-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbe6-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dbbe6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbe6-133">입력</span><span class="sxs-lookup"><span data-stu-id="dbbe6-133">INPUTS</span></span>

### <span data-ttu-id="dbbe6-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dbbe6-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dbbe6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dbbe6-135">System.String</span></span>

## <span data-ttu-id="dbbe6-136">출력</span><span class="sxs-lookup"><span data-stu-id="dbbe6-136">OUTPUTS</span></span>

### <span data-ttu-id="dbbe6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="dbbe6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="dbbe6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dbbe6-138">NOTES</span></span>

## <span data-ttu-id="dbbe6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbbe6-139">RELATED LINKS</span></span>

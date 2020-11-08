---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043000"
---
# <span data-ttu-id="aaac8-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="aaac8-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="aaac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaac8-102">SYNOPSIS</span></span>
<span data-ttu-id="aaac8-103">Iot Hub에서 대상 IoT 장치의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="aaac8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aaac8-104">SYNTAX</span></span>

### <span data-ttu-id="aaac8-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aaac8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaac8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aaac8-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaac8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aaac8-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaac8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aaac8-108">DESCRIPTION</span></span>
<span data-ttu-id="aaac8-109">Azure IoT Hub 내에 포함 된 모든 디바이스 또는 대상 IoT 장치에 대 한 연결 문자열을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="aaac8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aaac8-110">EXAMPLES</span></span>

### <span data-ttu-id="aaac8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aaac8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="aaac8-112">Iot Hub의 모든 디바이스 연결 문자열을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="aaac8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="aaac8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="aaac8-114">IoT 장치의 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="aaac8-115">변수</span><span class="sxs-lookup"><span data-stu-id="aaac8-115">PARAMETERS</span></span>

### <span data-ttu-id="aaac8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaac8-116">-DefaultProfile</span></span>
<span data-ttu-id="aaac8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaac8-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="aaac8-118">-DeviceId</span></span>
<span data-ttu-id="aaac8-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-119">Target Device Id.</span></span>

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

### <span data-ttu-id="aaac8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaac8-120">-InputObject</span></span>
<span data-ttu-id="aaac8-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="aaac8-121">IotHub object</span></span>

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

### <span data-ttu-id="aaac8-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="aaac8-122">-IotHubName</span></span>
<span data-ttu-id="aaac8-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="aaac8-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aaac8-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="aaac8-124">-KeyType</span></span>
<span data-ttu-id="aaac8-125">Auth에 대 한 공유 액세스 정책 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="aaac8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaac8-126">-ResourceGroupName</span></span>
<span data-ttu-id="aaac8-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aaac8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaac8-128">-ResourceId</span></span>
<span data-ttu-id="aaac8-129">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="aaac8-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aaac8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaac8-130">CommonParameters</span></span>
<span data-ttu-id="aaac8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaac8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaac8-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaac8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaac8-133">입력</span><span class="sxs-lookup"><span data-stu-id="aaac8-133">INPUTS</span></span>

### <span data-ttu-id="aaac8-134">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="aaac8-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aaac8-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aaac8-135">System.String</span></span>

## <span data-ttu-id="aaac8-136">출력</span><span class="sxs-lookup"><span data-stu-id="aaac8-136">OUTPUTS</span></span>

### <span data-ttu-id="aaac8-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="aaac8-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="aaac8-138">상속자</span><span class="sxs-lookup"><span data-stu-id="aaac8-138">NOTES</span></span>

## <span data-ttu-id="aaac8-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaac8-139">RELATED LINKS</span></span>

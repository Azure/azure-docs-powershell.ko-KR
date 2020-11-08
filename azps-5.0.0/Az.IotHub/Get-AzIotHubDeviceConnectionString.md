---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217753"
---
# <span data-ttu-id="18f78-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="18f78-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="18f78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f78-102">SYNOPSIS</span></span>
<span data-ttu-id="18f78-103">Iot Hub에서 대상 IoT 장치의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="18f78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18f78-104">SYNTAX</span></span>

### <span data-ttu-id="18f78-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="18f78-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18f78-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18f78-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18f78-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="18f78-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18f78-108">설명은</span><span class="sxs-lookup"><span data-stu-id="18f78-108">DESCRIPTION</span></span>
<span data-ttu-id="18f78-109">Azure IoT Hub 내에 포함 된 모든 디바이스 또는 대상 IoT 장치에 대 한 연결 문자열을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="18f78-110">예제의</span><span class="sxs-lookup"><span data-stu-id="18f78-110">EXAMPLES</span></span>

### <span data-ttu-id="18f78-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="18f78-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="18f78-112">Iot Hub의 모든 디바이스 연결 문자열을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="18f78-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="18f78-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="18f78-114">IoT 장치의 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="18f78-115">변수</span><span class="sxs-lookup"><span data-stu-id="18f78-115">PARAMETERS</span></span>

### <span data-ttu-id="18f78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f78-116">-DefaultProfile</span></span>
<span data-ttu-id="18f78-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f78-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="18f78-118">-DeviceId</span></span>
<span data-ttu-id="18f78-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-119">Target Device Id.</span></span>

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

### <span data-ttu-id="18f78-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18f78-120">-InputObject</span></span>
<span data-ttu-id="18f78-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="18f78-121">IotHub object</span></span>

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

### <span data-ttu-id="18f78-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="18f78-122">-IotHubName</span></span>
<span data-ttu-id="18f78-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="18f78-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="18f78-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="18f78-124">-KeyType</span></span>
<span data-ttu-id="18f78-125">Auth에 대 한 공유 액세스 정책 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="18f78-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18f78-126">-ResourceGroupName</span></span>
<span data-ttu-id="18f78-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="18f78-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18f78-128">-ResourceId</span></span>
<span data-ttu-id="18f78-129">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="18f78-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="18f78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f78-130">CommonParameters</span></span>
<span data-ttu-id="18f78-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18f78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f78-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f78-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f78-133">입력</span><span class="sxs-lookup"><span data-stu-id="18f78-133">INPUTS</span></span>

### <span data-ttu-id="18f78-134">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="18f78-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="18f78-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18f78-135">System.String</span></span>

## <span data-ttu-id="18f78-136">출력</span><span class="sxs-lookup"><span data-stu-id="18f78-136">OUTPUTS</span></span>

### <span data-ttu-id="18f78-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="18f78-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="18f78-138">상속자</span><span class="sxs-lookup"><span data-stu-id="18f78-138">NOTES</span></span>

## <span data-ttu-id="18f78-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18f78-139">RELATED LINKS</span></span>

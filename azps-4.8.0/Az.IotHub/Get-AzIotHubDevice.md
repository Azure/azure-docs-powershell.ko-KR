---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213366"
---
# <span data-ttu-id="b69a3-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b69a3-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="b69a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b69a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b69a3-103">모든 장치 또는 Azure IoT Hub 내에 포함 된 특정 장치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="b69a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b69a3-104">SYNTAX</span></span>

### <span data-ttu-id="b69a3-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b69a3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b69a3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b69a3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b69a3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b69a3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b69a3-108">DESCRIPTION</span></span>
<span data-ttu-id="b69a3-109">Iot Hub 장치의 세부 정보를 가져오거나 Iot Hub의 모든 장치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="b69a3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b69a3-110">EXAMPLES</span></span>

### <span data-ttu-id="b69a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b69a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="b69a3-112">Iot Hub의 모든 장치를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="b69a3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b69a3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="b69a3-114">IoT Hub 장치의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="b69a3-115">변수</span><span class="sxs-lookup"><span data-stu-id="b69a3-115">PARAMETERS</span></span>

### <span data-ttu-id="b69a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69a3-116">-DefaultProfile</span></span>
<span data-ttu-id="b69a3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b69a3-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-118">-DeviceId</span></span>
<span data-ttu-id="b69a3-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-119">Target Device Id.</span></span>

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

### <span data-ttu-id="b69a3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b69a3-120">-InputObject</span></span>
<span data-ttu-id="b69a3-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="b69a3-121">IotHub object</span></span>

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

### <span data-ttu-id="b69a3-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b69a3-122">-IotHubName</span></span>
<span data-ttu-id="b69a3-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="b69a3-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b69a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="b69a3-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b69a3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b69a3-126">-ResourceId</span></span>
<span data-ttu-id="b69a3-127">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b69a3-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b69a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69a3-128">CommonParameters</span></span>
<span data-ttu-id="b69a3-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b69a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69a3-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b69a3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69a3-131">입력</span><span class="sxs-lookup"><span data-stu-id="b69a3-131">INPUTS</span></span>

### <span data-ttu-id="b69a3-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="b69a3-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b69a3-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b69a3-133">System.String</span></span>

## <span data-ttu-id="b69a3-134">출력</span><span class="sxs-lookup"><span data-stu-id="b69a3-134">OUTPUTS</span></span>

### <span data-ttu-id="b69a3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="b69a3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="b69a3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices []</span><span class="sxs-lookup"><span data-stu-id="b69a3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="b69a3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b69a3-137">NOTES</span></span>

## <span data-ttu-id="b69a3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b69a3-138">RELATED LINKS</span></span>

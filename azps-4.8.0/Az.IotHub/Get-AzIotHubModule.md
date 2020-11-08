---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049042"
---
# <span data-ttu-id="d1edc-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d1edc-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="d1edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1edc-102">SYNOPSIS</span></span>
<span data-ttu-id="d1edc-103">Iot Hub의 IoT 장치에 있는 IoT 장치 모듈 또는 목록 모듈의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d1edc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1edc-104">SYNTAX</span></span>

### <span data-ttu-id="d1edc-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1edc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1edc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1edc-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1edc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d1edc-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1edc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d1edc-108">DESCRIPTION</span></span>
<span data-ttu-id="d1edc-109">Iot Hub의 IoT 장치에 있는 IoT 장치 모듈 또는 목록 모듈의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d1edc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d1edc-110">EXAMPLES</span></span>

### <span data-ttu-id="d1edc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1edc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="d1edc-112">IoT Hub의 IoT 장치 모듈에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="d1edc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d1edc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="d1edc-114">Iot Hub의 IoT 장치에 있는 모든 모듈을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d1edc-115">변수</span><span class="sxs-lookup"><span data-stu-id="d1edc-115">PARAMETERS</span></span>

### <span data-ttu-id="d1edc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1edc-116">-DefaultProfile</span></span>
<span data-ttu-id="d1edc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1edc-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d1edc-118">-DeviceId</span></span>
<span data-ttu-id="d1edc-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-119">Target Device Id.</span></span>

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

### <span data-ttu-id="d1edc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1edc-120">-InputObject</span></span>
<span data-ttu-id="d1edc-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d1edc-121">IotHub object</span></span>

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

### <span data-ttu-id="d1edc-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d1edc-122">-IotHubName</span></span>
<span data-ttu-id="d1edc-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d1edc-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d1edc-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="d1edc-124">-ModuleId</span></span>
<span data-ttu-id="d1edc-125">대상 모듈 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-125">Target Module Id.</span></span>

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

### <span data-ttu-id="d1edc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1edc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1edc-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d1edc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1edc-128">-ResourceId</span></span>
<span data-ttu-id="d1edc-129">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d1edc-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d1edc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1edc-130">CommonParameters</span></span>
<span data-ttu-id="d1edc-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1edc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1edc-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1edc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1edc-133">입력</span><span class="sxs-lookup"><span data-stu-id="d1edc-133">INPUTS</span></span>

### <span data-ttu-id="d1edc-134">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="d1edc-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d1edc-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1edc-135">System.String</span></span>

## <span data-ttu-id="d1edc-136">출력</span><span class="sxs-lookup"><span data-stu-id="d1edc-136">OUTPUTS</span></span>

### <span data-ttu-id="d1edc-137">IotHub. a i m/. a i m 모듈</span><span class="sxs-lookup"><span data-stu-id="d1edc-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="d1edc-138">IotHub. m a m a 모듈 []</span><span class="sxs-lookup"><span data-stu-id="d1edc-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="d1edc-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d1edc-139">NOTES</span></span>

## <span data-ttu-id="d1edc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1edc-140">RELATED LINKS</span></span>

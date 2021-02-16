---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185684"
---
# <span data-ttu-id="230ce-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="230ce-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="230ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="230ce-102">SYNOPSIS</span></span>
<span data-ttu-id="230ce-103">IoT Hub의 IoT 디바이스에 있는 IoT 디바이스 모듈 또는 목록 모듈의 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="230ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="230ce-104">SYNTAX</span></span>

### <span data-ttu-id="230ce-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="230ce-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="230ce-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="230ce-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="230ce-108">설명</span><span class="sxs-lookup"><span data-stu-id="230ce-108">DESCRIPTION</span></span>
<span data-ttu-id="230ce-109">IoT Hub의 IoT 디바이스에 있는 IoT 디바이스 모듈 또는 목록 모듈의 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="230ce-110">예제</span><span class="sxs-lookup"><span data-stu-id="230ce-110">EXAMPLES</span></span>

### <span data-ttu-id="230ce-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="230ce-111">Example 1</span></span>
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

<span data-ttu-id="230ce-112">IoT Hub에서 IoT 디바이스 모듈의 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="230ce-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="230ce-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="230ce-114">IoT Hub의 IoT 디바이스에 있는 모든 모듈을 보여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="230ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="230ce-115">PARAMETERS</span></span>

### <span data-ttu-id="230ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230ce-116">-DefaultProfile</span></span>
<span data-ttu-id="230ce-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="230ce-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="230ce-118">-DeviceId</span></span>
<span data-ttu-id="230ce-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-119">Target Device Id.</span></span>

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

### <span data-ttu-id="230ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="230ce-120">-InputObject</span></span>
<span data-ttu-id="230ce-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="230ce-121">IotHub object</span></span>

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

### <span data-ttu-id="230ce-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="230ce-122">-IotHubName</span></span>
<span data-ttu-id="230ce-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="230ce-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="230ce-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="230ce-124">-ModuleId</span></span>
<span data-ttu-id="230ce-125">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-125">Target Module Id.</span></span>

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

### <span data-ttu-id="230ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="230ce-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="230ce-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="230ce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="230ce-128">-ResourceId</span></span>
<span data-ttu-id="230ce-129">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="230ce-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="230ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230ce-130">CommonParameters</span></span>
<span data-ttu-id="230ce-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="230ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230ce-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="230ce-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230ce-133">입력</span><span class="sxs-lookup"><span data-stu-id="230ce-133">INPUTS</span></span>

### <span data-ttu-id="230ce-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="230ce-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="230ce-135">System.String</span><span class="sxs-lookup"><span data-stu-id="230ce-135">System.String</span></span>

## <span data-ttu-id="230ce-136">출력</span><span class="sxs-lookup"><span data-stu-id="230ce-136">OUTPUTS</span></span>

### <span data-ttu-id="230ce-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="230ce-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="230ce-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="230ce-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="230ce-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="230ce-139">NOTES</span></span>

## <span data-ttu-id="230ce-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="230ce-140">RELATED LINKS</span></span>

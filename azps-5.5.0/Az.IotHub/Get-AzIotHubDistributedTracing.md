---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185716"
---
# <span data-ttu-id="20705-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="20705-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="20705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20705-102">SYNOPSIS</span></span>
<span data-ttu-id="20705-103">디바이스에 대한 분산 추적 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20705-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="20705-104">구문</span><span class="sxs-lookup"><span data-stu-id="20705-104">SYNTAX</span></span>

### <span data-ttu-id="20705-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="20705-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20705-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20705-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20705-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="20705-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20705-108">설명</span><span class="sxs-lookup"><span data-stu-id="20705-108">DESCRIPTION</span></span>
<span data-ttu-id="20705-109">디바이스에 대한 분산 추적 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20705-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="20705-110">예제</span><span class="sxs-lookup"><span data-stu-id="20705-110">EXAMPLES</span></span>

### <span data-ttu-id="20705-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="20705-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="20705-112">디바이스에 대한 분산 추적 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20705-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="20705-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20705-113">PARAMETERS</span></span>

### <span data-ttu-id="20705-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20705-114">-DefaultProfile</span></span>
<span data-ttu-id="20705-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20705-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20705-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="20705-116">-DeviceId</span></span>
<span data-ttu-id="20705-117">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20705-117">Target Device Id.</span></span>

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

### <span data-ttu-id="20705-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20705-118">-InputObject</span></span>
<span data-ttu-id="20705-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="20705-119">IotHub object</span></span>

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

### <span data-ttu-id="20705-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="20705-120">-IotHubName</span></span>
<span data-ttu-id="20705-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="20705-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="20705-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20705-122">-ResourceGroupName</span></span>
<span data-ttu-id="20705-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="20705-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="20705-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20705-124">-ResourceId</span></span>
<span data-ttu-id="20705-125">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="20705-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="20705-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20705-126">CommonParameters</span></span>
<span data-ttu-id="20705-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20705-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20705-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20705-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20705-129">입력</span><span class="sxs-lookup"><span data-stu-id="20705-129">INPUTS</span></span>

### <span data-ttu-id="20705-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="20705-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="20705-131">System.String</span><span class="sxs-lookup"><span data-stu-id="20705-131">System.String</span></span>

## <span data-ttu-id="20705-132">출력</span><span class="sxs-lookup"><span data-stu-id="20705-132">OUTPUTS</span></span>

### <span data-ttu-id="20705-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="20705-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="20705-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20705-134">NOTES</span></span>

## <span data-ttu-id="20705-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20705-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94227007"
---
# <span data-ttu-id="62fec-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="62fec-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="62fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62fec-102">SYNOPSIS</span></span>
<span data-ttu-id="62fec-103">장치에 대 한 분산 추적 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="62fec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62fec-104">SYNTAX</span></span>

### <span data-ttu-id="62fec-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62fec-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62fec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62fec-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62fec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62fec-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62fec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="62fec-108">DESCRIPTION</span></span>
<span data-ttu-id="62fec-109">장치에 대 한 분산 추적 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="62fec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="62fec-110">EXAMPLES</span></span>

### <span data-ttu-id="62fec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="62fec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="62fec-112">장치에 대 한 분산 추적 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="62fec-113">변수</span><span class="sxs-lookup"><span data-stu-id="62fec-113">PARAMETERS</span></span>

### <span data-ttu-id="62fec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fec-114">-DefaultProfile</span></span>
<span data-ttu-id="62fec-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62fec-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="62fec-116">-DeviceId</span></span>
<span data-ttu-id="62fec-117">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-117">Target Device Id.</span></span>

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

### <span data-ttu-id="62fec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62fec-118">-InputObject</span></span>
<span data-ttu-id="62fec-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="62fec-119">IotHub object</span></span>

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

### <span data-ttu-id="62fec-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62fec-120">-IotHubName</span></span>
<span data-ttu-id="62fec-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="62fec-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62fec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62fec-122">-ResourceGroupName</span></span>
<span data-ttu-id="62fec-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62fec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62fec-124">-ResourceId</span></span>
<span data-ttu-id="62fec-125">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="62fec-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62fec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fec-126">CommonParameters</span></span>
<span data-ttu-id="62fec-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fec-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62fec-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fec-129">입력</span><span class="sxs-lookup"><span data-stu-id="62fec-129">INPUTS</span></span>

### <span data-ttu-id="62fec-130">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="62fec-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62fec-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62fec-131">System.String</span></span>

## <span data-ttu-id="62fec-132">출력</span><span class="sxs-lookup"><span data-stu-id="62fec-132">OUTPUTS</span></span>

### <span data-ttu-id="62fec-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="62fec-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="62fec-134">상속자</span><span class="sxs-lookup"><span data-stu-id="62fec-134">NOTES</span></span>

## <span data-ttu-id="62fec-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62fec-135">RELATED LINKS</span></span>

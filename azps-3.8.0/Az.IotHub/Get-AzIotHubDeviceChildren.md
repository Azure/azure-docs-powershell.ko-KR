---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041683"
---
# <span data-ttu-id="60ac4-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="60ac4-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="60ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="60ac4-103">지정 된 자식 장치를 쉼표로 구분한 목록 인쇄</span><span class="sxs-lookup"><span data-stu-id="60ac4-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="60ac4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60ac4-104">SYNTAX</span></span>

### <span data-ttu-id="60ac4-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="60ac4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ac4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="60ac4-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ac4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="60ac4-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ac4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="60ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="60ac4-109">모든 edge 장치 또는 지정 된 디바이스의 쉼표로 구분 된 목록으로 모든에 지 않은 디바이스를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="60ac4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="60ac4-110">EXAMPLES</span></span>

### <span data-ttu-id="60ac4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="60ac4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="60ac4-112">지정 된 모든 비 경계 장치를 쉼표로 구분한 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="60ac4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="60ac4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="60ac4-114">모든 edge 디바이스의 쉼표로 구분 된 목록으로 모든에 지 않은 디바이스를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="60ac4-115">변수</span><span class="sxs-lookup"><span data-stu-id="60ac4-115">PARAMETERS</span></span>

### <span data-ttu-id="60ac4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ac4-116">-DefaultProfile</span></span>
<span data-ttu-id="60ac4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ac4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="60ac4-118">-DeviceId</span></span>
<span data-ttu-id="60ac4-119">Edge 디바이스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-119">Id of edge device.</span></span>

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

### <span data-ttu-id="60ac4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60ac4-120">-InputObject</span></span>
<span data-ttu-id="60ac4-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="60ac4-121">IotHub object</span></span>

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

### <span data-ttu-id="60ac4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="60ac4-122">-IotHubName</span></span>
<span data-ttu-id="60ac4-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="60ac4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="60ac4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ac4-124">-ResourceGroupName</span></span>
<span data-ttu-id="60ac4-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="60ac4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60ac4-126">-ResourceId</span></span>
<span data-ttu-id="60ac4-127">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="60ac4-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="60ac4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ac4-128">CommonParameters</span></span>
<span data-ttu-id="60ac4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60ac4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ac4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ac4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ac4-131">입력</span><span class="sxs-lookup"><span data-stu-id="60ac4-131">INPUTS</span></span>

### <span data-ttu-id="60ac4-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="60ac4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="60ac4-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60ac4-133">System.String</span></span>

## <span data-ttu-id="60ac4-134">출력</span><span class="sxs-lookup"><span data-stu-id="60ac4-134">OUTPUTS</span></span>

### <span data-ttu-id="60ac4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="60ac4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="60ac4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="60ac4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="60ac4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="60ac4-137">NOTES</span></span>

## <span data-ttu-id="60ac4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60ac4-138">RELATED LINKS</span></span>

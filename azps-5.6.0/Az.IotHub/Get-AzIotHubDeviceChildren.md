---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: ec84ee72caadc4d49c29a72e1e5171e589dc11d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988078"
---
# <span data-ttu-id="b33a2-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b33a2-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="b33a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b33a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b33a2-103">할당된 자식 디바이스의 콤마로 구분된 목록을 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="b33a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="b33a2-104">SYNTAX</span></span>

### <span data-ttu-id="b33a2-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b33a2-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b33a2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b33a2-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b33a2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b33a2-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b33a2-108">설명</span><span class="sxs-lookup"><span data-stu-id="b33a2-108">DESCRIPTION</span></span>
<span data-ttu-id="b33a2-109">할당된 모든 비에지 디바이스를 모든 에지 디바이스 또는 지정된 디바이스의 콤마로 구분된 목록으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="b33a2-110">예제</span><span class="sxs-lookup"><span data-stu-id="b33a2-110">EXAMPLES</span></span>

### <span data-ttu-id="b33a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b33a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="b33a2-112">할당된 모든 비에지 디바이스를 콤마로 구분된 목록으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="b33a2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b33a2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="b33a2-114">할당된 모든 비에지 디바이스를 모든 에지 디바이스의 콤마로 구분된 목록으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="b33a2-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b33a2-115">PARAMETERS</span></span>

### <span data-ttu-id="b33a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33a2-116">-DefaultProfile</span></span>
<span data-ttu-id="b33a2-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33a2-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b33a2-118">-DeviceId</span></span>
<span data-ttu-id="b33a2-119">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-119">Id of edge device.</span></span>

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

### <span data-ttu-id="b33a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b33a2-120">-InputObject</span></span>
<span data-ttu-id="b33a2-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="b33a2-121">IotHub object</span></span>

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

### <span data-ttu-id="b33a2-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b33a2-122">-IotHubName</span></span>
<span data-ttu-id="b33a2-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="b33a2-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b33a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b33a2-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b33a2-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b33a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b33a2-126">-ResourceId</span></span>
<span data-ttu-id="b33a2-127">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b33a2-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b33a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33a2-128">CommonParameters</span></span>
<span data-ttu-id="b33a2-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b33a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33a2-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b33a2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33a2-131">입력</span><span class="sxs-lookup"><span data-stu-id="b33a2-131">INPUTS</span></span>

### <span data-ttu-id="b33a2-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b33a2-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b33a2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b33a2-133">System.String</span></span>

## <span data-ttu-id="b33a2-134">출력</span><span class="sxs-lookup"><span data-stu-id="b33a2-134">OUTPUTS</span></span>

### <span data-ttu-id="b33a2-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b33a2-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="b33a2-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span><span class="sxs-lookup"><span data-stu-id="b33a2-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="b33a2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b33a2-137">NOTES</span></span>

## <span data-ttu-id="b33a2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b33a2-138">RELATED LINKS</span></span>

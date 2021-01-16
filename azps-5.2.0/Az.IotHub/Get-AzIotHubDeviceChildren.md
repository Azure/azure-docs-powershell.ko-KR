---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329985"
---
# <span data-ttu-id="e54a8-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e54a8-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="e54a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e54a8-103">할당된 자식 디바이스의 콤마로 구분된 목록을 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="e54a8-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="e54a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="e54a8-104">SYNTAX</span></span>

### <span data-ttu-id="e54a8-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e54a8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e54a8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e54a8-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e54a8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e54a8-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e54a8-108">설명</span><span class="sxs-lookup"><span data-stu-id="e54a8-108">DESCRIPTION</span></span>
<span data-ttu-id="e54a8-109">할당된 모든 에지가 아닌 디바이스를 모든 에지 디바이스 또는 지정된 디바이스의 콤마로 구분된 목록으로 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="e54a8-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="e54a8-110">예제</span><span class="sxs-lookup"><span data-stu-id="e54a8-110">EXAMPLES</span></span>

### <span data-ttu-id="e54a8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e54a8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="e54a8-112">할당된 모든 비에지 디바이스를 콤마로 구분된 목록으로 표시</span><span class="sxs-lookup"><span data-stu-id="e54a8-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="e54a8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e54a8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="e54a8-114">할당된 모든 비에지 디바이스를 모든 에지 디바이스의 콤마로 구분된 목록으로 표시</span><span class="sxs-lookup"><span data-stu-id="e54a8-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="e54a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e54a8-115">PARAMETERS</span></span>

### <span data-ttu-id="e54a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54a8-116">-DefaultProfile</span></span>
<span data-ttu-id="e54a8-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e54a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e54a8-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e54a8-118">-DeviceId</span></span>
<span data-ttu-id="e54a8-119">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e54a8-119">Id of edge device.</span></span>

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

### <span data-ttu-id="e54a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e54a8-120">-InputObject</span></span>
<span data-ttu-id="e54a8-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e54a8-121">IotHub object</span></span>

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

### <span data-ttu-id="e54a8-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e54a8-122">-IotHubName</span></span>
<span data-ttu-id="e54a8-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e54a8-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e54a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="e54a8-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e54a8-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e54a8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e54a8-126">-ResourceId</span></span>
<span data-ttu-id="e54a8-127">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e54a8-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e54a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54a8-128">CommonParameters</span></span>
<span data-ttu-id="e54a8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e54a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54a8-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e54a8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54a8-131">입력</span><span class="sxs-lookup"><span data-stu-id="e54a8-131">INPUTS</span></span>

### <span data-ttu-id="e54a8-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e54a8-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e54a8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e54a8-133">System.String</span></span>

## <span data-ttu-id="e54a8-134">출력</span><span class="sxs-lookup"><span data-stu-id="e54a8-134">OUTPUTS</span></span>

### <span data-ttu-id="e54a8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e54a8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="e54a8-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span><span class="sxs-lookup"><span data-stu-id="e54a8-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="e54a8-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e54a8-137">NOTES</span></span>

## <span data-ttu-id="e54a8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e54a8-138">RELATED LINKS</span></span>

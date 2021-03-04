---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9dd4925224f2ed91770caff422b8ab6f5d924754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998634"
---
# <span data-ttu-id="8374a-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8374a-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="8374a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8374a-102">SYNOPSIS</span></span>
<span data-ttu-id="8374a-103">디바이스에 사용할 수 있는 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="8374a-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="8374a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8374a-104">SYNTAX</span></span>

### <span data-ttu-id="8374a-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8374a-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8374a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8374a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8374a-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8374a-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8374a-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8374a-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8374a-109">설명</span><span class="sxs-lookup"><span data-stu-id="8374a-109">DESCRIPTION</span></span>
<span data-ttu-id="8374a-110">**Get-AzDataBoxEdgeRole** cmdlet은 Data Box Edge 디바이스에 사용할 수 있는 IoT 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="8374a-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="8374a-111">이름 매개 변수를 언급하여 특정 IoT 역할의 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8374a-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="8374a-112">예제</span><span class="sxs-lookup"><span data-stu-id="8374a-112">EXAMPLES</span></span>

### <span data-ttu-id="8374a-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="8374a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="8374a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8374a-114">PARAMETERS</span></span>

### <span data-ttu-id="8374a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8374a-115">-DefaultProfile</span></span>
<span data-ttu-id="8374a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8374a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8374a-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8374a-117">-DeviceName</span></span>
<span data-ttu-id="8374a-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="8374a-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8374a-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8374a-119">-DeviceObject</span></span>
<span data-ttu-id="8374a-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="8374a-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8374a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8374a-121">-Name</span></span>
<span data-ttu-id="8374a-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="8374a-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8374a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8374a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8374a-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8374a-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8374a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8374a-125">-ResourceId</span></span>
<span data-ttu-id="8374a-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8374a-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8374a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8374a-127">CommonParameters</span></span>
<span data-ttu-id="8374a-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8374a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8374a-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8374a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8374a-130">입력</span><span class="sxs-lookup"><span data-stu-id="8374a-130">INPUTS</span></span>

### <span data-ttu-id="8374a-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8374a-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8374a-132">출력</span><span class="sxs-lookup"><span data-stu-id="8374a-132">OUTPUTS</span></span>

### <span data-ttu-id="8374a-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8374a-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8374a-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8374a-134">NOTES</span></span>

## <span data-ttu-id="8374a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8374a-135">RELATED LINKS</span></span>

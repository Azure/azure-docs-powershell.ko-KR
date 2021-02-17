---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204525"
---
# <span data-ttu-id="968f9-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="968f9-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="968f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="968f9-102">SYNOPSIS</span></span>
<span data-ttu-id="968f9-103">디바이스에 사용 가능한 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="968f9-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="968f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="968f9-104">SYNTAX</span></span>

### <span data-ttu-id="968f9-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="968f9-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="968f9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="968f9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="968f9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="968f9-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="968f9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="968f9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="968f9-109">설명</span><span class="sxs-lookup"><span data-stu-id="968f9-109">DESCRIPTION</span></span>
<span data-ttu-id="968f9-110">**Get-AzDataBoxEdgeRole** cmdlet은 Data Box Edge 디바이스에 사용 가능한 IoT 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="968f9-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="968f9-111">Name 매개 변수를 언급하여 특정 IoT 역할의 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="968f9-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="968f9-112">예제</span><span class="sxs-lookup"><span data-stu-id="968f9-112">EXAMPLES</span></span>

### <span data-ttu-id="968f9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="968f9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="968f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="968f9-114">PARAMETERS</span></span>

### <span data-ttu-id="968f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968f9-115">-DefaultProfile</span></span>
<span data-ttu-id="968f9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="968f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="968f9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="968f9-117">-DeviceName</span></span>
<span data-ttu-id="968f9-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="968f9-118">Device Name</span></span>

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

### <span data-ttu-id="968f9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="968f9-119">-DeviceObject</span></span>
<span data-ttu-id="968f9-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="968f9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="968f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="968f9-121">-Name</span></span>
<span data-ttu-id="968f9-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="968f9-122">Resource Name</span></span>

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

### <span data-ttu-id="968f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="968f9-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="968f9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="968f9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="968f9-125">-ResourceId</span></span>
<span data-ttu-id="968f9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="968f9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="968f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968f9-127">CommonParameters</span></span>
<span data-ttu-id="968f9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="968f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968f9-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="968f9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968f9-130">입력</span><span class="sxs-lookup"><span data-stu-id="968f9-130">INPUTS</span></span>

### <span data-ttu-id="968f9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="968f9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="968f9-132">출력</span><span class="sxs-lookup"><span data-stu-id="968f9-132">OUTPUTS</span></span>

### <span data-ttu-id="968f9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="968f9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="968f9-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="968f9-134">NOTES</span></span>

## <span data-ttu-id="968f9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="968f9-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0af708265a66ecf05bfe4eb5de37d7b81a21aa3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876829"
---
# <span data-ttu-id="bea24-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="bea24-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="bea24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea24-102">SYNOPSIS</span></span>
<span data-ttu-id="bea24-103">장치에 대해 사용 가능한 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="bea24-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="bea24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bea24-104">SYNTAX</span></span>

### <span data-ttu-id="bea24-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bea24-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea24-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea24-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea24-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea24-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea24-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea24-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="bea24-109">설명은</span><span class="sxs-lookup"><span data-stu-id="bea24-109">DESCRIPTION</span></span>
<span data-ttu-id="bea24-110">**AzDataBoxEdgeRole** Cmdlet은 데이터 상자 가장자리 장치에 사용할 수 있는 IoT 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="bea24-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="bea24-111">Name 매개 변수를 언급 하 여 특정 IoT 역할의 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bea24-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="bea24-112">예제의</span><span class="sxs-lookup"><span data-stu-id="bea24-112">EXAMPLES</span></span>

### <span data-ttu-id="bea24-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="bea24-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="bea24-114">변수</span><span class="sxs-lookup"><span data-stu-id="bea24-114">PARAMETERS</span></span>

### <span data-ttu-id="bea24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea24-115">-DefaultProfile</span></span>
<span data-ttu-id="bea24-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bea24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea24-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="bea24-117">-DeviceName</span></span>
<span data-ttu-id="bea24-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="bea24-118">Device Name</span></span>

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

### <span data-ttu-id="bea24-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="bea24-119">-DeviceObject</span></span>
<span data-ttu-id="bea24-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="bea24-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="bea24-121">-이름</span><span class="sxs-lookup"><span data-stu-id="bea24-121">-Name</span></span>
<span data-ttu-id="bea24-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="bea24-122">Resource Name</span></span>

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

### <span data-ttu-id="bea24-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea24-123">-ResourceGroupName</span></span>
<span data-ttu-id="bea24-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bea24-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bea24-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea24-125">-ResourceId</span></span>
<span data-ttu-id="bea24-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea24-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="bea24-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea24-127">CommonParameters</span></span>
<span data-ttu-id="bea24-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea24-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea24-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bea24-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea24-130">입력</span><span class="sxs-lookup"><span data-stu-id="bea24-130">INPUTS</span></span>

### <span data-ttu-id="bea24-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bea24-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="bea24-132">출력</span><span class="sxs-lookup"><span data-stu-id="bea24-132">OUTPUTS</span></span>

### <span data-ttu-id="bea24-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="bea24-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="bea24-134">상속자</span><span class="sxs-lookup"><span data-stu-id="bea24-134">NOTES</span></span>

## <span data-ttu-id="bea24-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bea24-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216633"
---
# <span data-ttu-id="0fe55-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="0fe55-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="0fe55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe55-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe55-103">장치에 대해 사용 가능한 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe55-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="0fe55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fe55-104">SYNTAX</span></span>

### <span data-ttu-id="0fe55-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0fe55-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe55-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe55-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe55-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe55-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe55-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe55-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0fe55-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0fe55-109">DESCRIPTION</span></span>
<span data-ttu-id="0fe55-110">**AzStackEdgeRole** Cmdlet은 스택 경계 장치에 사용할 수 있는 IoT 역할을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe55-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="0fe55-111">Name 매개 변수를 언급 하 여 특정 IoT 역할의 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fe55-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="0fe55-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0fe55-112">EXAMPLES</span></span>

### <span data-ttu-id="0fe55-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0fe55-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="0fe55-114">변수</span><span class="sxs-lookup"><span data-stu-id="0fe55-114">PARAMETERS</span></span>

### <span data-ttu-id="0fe55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe55-115">-DefaultProfile</span></span>
<span data-ttu-id="0fe55-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fe55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe55-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="0fe55-117">-DeviceName</span></span>
<span data-ttu-id="0fe55-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="0fe55-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe55-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0fe55-119">-DeviceObject</span></span>
<span data-ttu-id="0fe55-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0fe55-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe55-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0fe55-121">-Name</span></span>
<span data-ttu-id="0fe55-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="0fe55-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe55-123">-ResourceGroupName</span></span>
<span data-ttu-id="0fe55-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0fe55-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe55-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe55-125">-ResourceId</span></span>
<span data-ttu-id="0fe55-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe55-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe55-127">CommonParameters</span></span>
<span data-ttu-id="0fe55-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fe55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe55-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0fe55-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe55-130">입력</span><span class="sxs-lookup"><span data-stu-id="0fe55-130">INPUTS</span></span>

### <span data-ttu-id="0fe55-131">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="0fe55-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="0fe55-132">출력</span><span class="sxs-lookup"><span data-stu-id="0fe55-132">OUTPUTS</span></span>

### <span data-ttu-id="0fe55-133">StackEdge. PSStackEdgeRole에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="0fe55-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="0fe55-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0fe55-134">NOTES</span></span>

## <span data-ttu-id="0fe55-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fe55-135">RELATED LINKS</span></span>

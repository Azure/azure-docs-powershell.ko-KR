---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217988"
---
# <span data-ttu-id="58bc3-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="58bc3-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="58bc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="58bc3-103">장치에 예약 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58bc3-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="58bc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58bc3-104">SYNTAX</span></span>

### <span data-ttu-id="58bc3-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="58bc3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58bc3-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="58bc3-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58bc3-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58bc3-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="58bc3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="58bc3-108">DESCRIPTION</span></span>
<span data-ttu-id="58bc3-109">**AzStackEdgeJob** Cmdlet은 스택 경계 장치에서 활성 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58bc3-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="58bc3-110">Name 매개 변수를 언급 하 여 특정 작업에 대 한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58bc3-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="58bc3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="58bc3-111">EXAMPLES</span></span>

### <span data-ttu-id="58bc3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="58bc3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="58bc3-113">변수</span><span class="sxs-lookup"><span data-stu-id="58bc3-113">PARAMETERS</span></span>

### <span data-ttu-id="58bc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bc3-114">-DefaultProfile</span></span>
<span data-ttu-id="58bc3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58bc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58bc3-116">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="58bc3-116">-DeviceName</span></span>
<span data-ttu-id="58bc3-117">장치 이름</span><span class="sxs-lookup"><span data-stu-id="58bc3-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc3-118">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="58bc3-118">-DeviceObject</span></span>
<span data-ttu-id="58bc3-119">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="58bc3-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc3-120">-이름</span><span class="sxs-lookup"><span data-stu-id="58bc3-120">-Name</span></span>
<span data-ttu-id="58bc3-121">작업 이름 (일반적으로 GUID)</span><span class="sxs-lookup"><span data-stu-id="58bc3-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58bc3-122">-ResourceGroupName</span></span>
<span data-ttu-id="58bc3-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="58bc3-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58bc3-124">-ResourceId</span></span>
<span data-ttu-id="58bc3-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="58bc3-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58bc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bc3-126">CommonParameters</span></span>
<span data-ttu-id="58bc3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bc3-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58bc3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bc3-129">입력</span><span class="sxs-lookup"><span data-stu-id="58bc3-129">INPUTS</span></span>

### <span data-ttu-id="58bc3-130">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="58bc3-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="58bc3-131">출력</span><span class="sxs-lookup"><span data-stu-id="58bc3-131">OUTPUTS</span></span>

### <span data-ttu-id="58bc3-132">StackEdge. PSStackEdgeJob에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="58bc3-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="58bc3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="58bc3-133">NOTES</span></span>

## <span data-ttu-id="58bc3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58bc3-134">RELATED LINKS</span></span>

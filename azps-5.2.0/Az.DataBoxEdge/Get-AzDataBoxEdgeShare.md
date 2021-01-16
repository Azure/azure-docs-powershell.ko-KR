---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362790"
---
# <span data-ttu-id="ab6ae-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ab6ae-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="ab6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6ae-103">디바이스에 사용 가능한 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="ab6ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab6ae-104">SYNTAX</span></span>

### <span data-ttu-id="ab6ae-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab6ae-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6ae-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab6ae-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6ae-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab6ae-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab6ae-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab6ae-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ab6ae-109">설명</span><span class="sxs-lookup"><span data-stu-id="ab6ae-109">DESCRIPTION</span></span>
<span data-ttu-id="ab6ae-110">**Get-AzDataBoxEdgeShare** cmdlet은 Data Box Edge 디바이스에 사용 가능한 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="ab6ae-111">Name이 제공된 경우 이름에 따라 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="ab6ae-112">예제</span><span class="sxs-lookup"><span data-stu-id="ab6ae-112">EXAMPLES</span></span>

### <span data-ttu-id="ab6ae-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab6ae-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="ab6ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab6ae-114">PARAMETERS</span></span>

### <span data-ttu-id="ab6ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6ae-115">-DefaultProfile</span></span>
<span data-ttu-id="ab6ae-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab6ae-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ab6ae-117">-DeviceName</span></span>
<span data-ttu-id="ab6ae-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="ab6ae-118">Device Name</span></span>

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

### <span data-ttu-id="ab6ae-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ab6ae-119">-DeviceObject</span></span>
<span data-ttu-id="ab6ae-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="ab6ae-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab6ae-121">-Name</span></span>
<span data-ttu-id="ab6ae-122">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ab6ae-122">Resource Name</span></span>

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

### <span data-ttu-id="ab6ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab6ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab6ae-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ab6ae-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ab6ae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab6ae-125">-ResourceId</span></span>
<span data-ttu-id="ab6ae-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab6ae-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="ab6ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6ae-127">CommonParameters</span></span>
<span data-ttu-id="ab6ae-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6ae-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab6ae-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6ae-130">입력</span><span class="sxs-lookup"><span data-stu-id="ab6ae-130">INPUTS</span></span>

### <span data-ttu-id="ab6ae-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ab6ae-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ab6ae-132">출력</span><span class="sxs-lookup"><span data-stu-id="ab6ae-132">OUTPUTS</span></span>

### <span data-ttu-id="ab6ae-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ab6ae-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="ab6ae-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab6ae-134">NOTES</span></span>

## <span data-ttu-id="ab6ae-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab6ae-135">RELATED LINKS</span></span>

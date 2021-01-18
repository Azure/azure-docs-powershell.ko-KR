---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495698"
---
# <span data-ttu-id="7f6d9-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7f6d9-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="7f6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6d9-103">디바이스에 대해 구성된 사용자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="7f6d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f6d9-104">SYNTAX</span></span>

### <span data-ttu-id="7f6d9-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f6d9-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f6d9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f6d9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f6d9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f6d9-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f6d9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f6d9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7f6d9-109">설명</span><span class="sxs-lookup"><span data-stu-id="7f6d9-109">DESCRIPTION</span></span>
<span data-ttu-id="7f6d9-110">**Get-AzDataBoxEdgeUser** cmdlet은 Data Box Edge 디바이스에 대해 구성된 사용자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="7f6d9-111">매개 변수에서 이름을 언급하여 특정 사용자에 대한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="7f6d9-112">예제</span><span class="sxs-lookup"><span data-stu-id="7f6d9-112">EXAMPLES</span></span>

### <span data-ttu-id="7f6d9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f6d9-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="7f6d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f6d9-114">PARAMETERS</span></span>

### <span data-ttu-id="7f6d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6d9-115">-DefaultProfile</span></span>
<span data-ttu-id="7f6d9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f6d9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7f6d9-117">-DeviceName</span></span>
<span data-ttu-id="7f6d9-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="7f6d9-118">Device Name</span></span>

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

### <span data-ttu-id="7f6d9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7f6d9-119">-DeviceObject</span></span>
<span data-ttu-id="7f6d9-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7f6d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7f6d9-121">-Name</span></span>
<span data-ttu-id="7f6d9-122">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="7f6d9-122">Username</span></span>

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

### <span data-ttu-id="7f6d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f6d9-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7f6d9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7f6d9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f6d9-125">-ResourceId</span></span>
<span data-ttu-id="7f6d9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f6d9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="7f6d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6d9-127">CommonParameters</span></span>
<span data-ttu-id="7f6d9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6d9-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7f6d9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6d9-130">입력</span><span class="sxs-lookup"><span data-stu-id="7f6d9-130">INPUTS</span></span>

### <span data-ttu-id="7f6d9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7f6d9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7f6d9-132">출력</span><span class="sxs-lookup"><span data-stu-id="7f6d9-132">OUTPUTS</span></span>

### <span data-ttu-id="7f6d9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7f6d9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="7f6d9-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f6d9-134">NOTES</span></span>

## <span data-ttu-id="7f6d9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f6d9-135">RELATED LINKS</span></span>

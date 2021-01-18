---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495701"
---
# <span data-ttu-id="6f152-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f152-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6f152-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f152-102">SYNOPSIS</span></span>
<span data-ttu-id="6f152-103">디바이스에서 Edge Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f152-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="6f152-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f152-104">SYNTAX</span></span>

### <span data-ttu-id="6f152-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f152-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f152-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f152-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f152-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f152-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f152-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f152-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6f152-109">설명</span><span class="sxs-lookup"><span data-stu-id="6f152-109">DESCRIPTION</span></span>
<span data-ttu-id="6f152-110">**Get-AzDataBoxEdgeStorageAccount** cmdlet은 Data Box Edge 디바이스에서 사용할 수 있는 Edge Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f152-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="6f152-111">cmdlet에서 이름을 매개 변수로 지정하여 특정 Edge Storage 계정의 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f152-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="6f152-112">예제</span><span class="sxs-lookup"><span data-stu-id="6f152-112">EXAMPLES</span></span>

### <span data-ttu-id="6f152-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f152-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="6f152-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f152-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="6f152-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6f152-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="6f152-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="6f152-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="6f152-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f152-117">PARAMETERS</span></span>

### <span data-ttu-id="6f152-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f152-118">-DefaultProfile</span></span>
<span data-ttu-id="6f152-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f152-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f152-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6f152-120">-DeviceName</span></span>
<span data-ttu-id="6f152-121">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="6f152-121">Device Name</span></span>

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

### <span data-ttu-id="6f152-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6f152-122">-DeviceObject</span></span>
<span data-ttu-id="6f152-123">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="6f152-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6f152-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6f152-124">-Name</span></span>
<span data-ttu-id="6f152-125">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="6f152-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f152-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f152-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f152-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6f152-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6f152-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f152-128">-ResourceId</span></span>
<span data-ttu-id="6f152-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f152-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="6f152-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f152-130">CommonParameters</span></span>
<span data-ttu-id="6f152-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f152-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f152-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f152-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f152-133">입력</span><span class="sxs-lookup"><span data-stu-id="6f152-133">INPUTS</span></span>

### <span data-ttu-id="6f152-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6f152-134">System.String</span></span>

### <span data-ttu-id="6f152-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6f152-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="6f152-136">출력</span><span class="sxs-lookup"><span data-stu-id="6f152-136">OUTPUTS</span></span>

### <span data-ttu-id="6f152-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f152-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6f152-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f152-138">NOTES</span></span>

## <span data-ttu-id="6f152-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f152-139">RELATED LINKS</span></span>

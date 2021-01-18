---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493605"
---
# <span data-ttu-id="92e1b-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="92e1b-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="92e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="92e1b-103">디바이스의 저장소 계정에 해당하는 저장소 계정 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92e1b-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="92e1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="92e1b-104">SYNTAX</span></span>

### <span data-ttu-id="92e1b-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="92e1b-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e1b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e1b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92e1b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e1b-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e1b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e1b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="92e1b-109">설명</span><span class="sxs-lookup"><span data-stu-id="92e1b-109">DESCRIPTION</span></span>
<span data-ttu-id="92e1b-110">**Get-AzDataBoxEdgeStorageAccountCredential** cmdlet은 Data Box Edge 디바이스에서 해당 저장소 계정에 대한 저장소 계정 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92e1b-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="92e1b-111">이름, 리소스 그룹 이름 및 디바이스 이름 매개 변수를 지정하여 특정 저장소 계정 자격 증명에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92e1b-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="92e1b-112">예제</span><span class="sxs-lookup"><span data-stu-id="92e1b-112">EXAMPLES</span></span>

### <span data-ttu-id="92e1b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="92e1b-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="92e1b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92e1b-114">PARAMETERS</span></span>

### <span data-ttu-id="92e1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e1b-115">-DefaultProfile</span></span>
<span data-ttu-id="92e1b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92e1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e1b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="92e1b-117">-DeviceName</span></span>
<span data-ttu-id="92e1b-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="92e1b-118">Device Name</span></span>

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

### <span data-ttu-id="92e1b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="92e1b-119">-DeviceObject</span></span>
<span data-ttu-id="92e1b-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="92e1b-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="92e1b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92e1b-121">-Name</span></span>
<span data-ttu-id="92e1b-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="92e1b-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="92e1b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e1b-123">-ResourceGroupName</span></span>
<span data-ttu-id="92e1b-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="92e1b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="92e1b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92e1b-125">-ResourceId</span></span>
<span data-ttu-id="92e1b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="92e1b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="92e1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e1b-127">CommonParameters</span></span>
<span data-ttu-id="92e1b-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92e1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e1b-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92e1b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e1b-130">입력</span><span class="sxs-lookup"><span data-stu-id="92e1b-130">INPUTS</span></span>

### <span data-ttu-id="92e1b-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="92e1b-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="92e1b-132">출력</span><span class="sxs-lookup"><span data-stu-id="92e1b-132">OUTPUTS</span></span>

### <span data-ttu-id="92e1b-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="92e1b-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="92e1b-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92e1b-134">NOTES</span></span>

## <span data-ttu-id="92e1b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92e1b-135">RELATED LINKS</span></span>

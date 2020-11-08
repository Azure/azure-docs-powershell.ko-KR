---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212352"
---
# <span data-ttu-id="7d933-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7d933-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7d933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d933-102">SYNOPSIS</span></span>
<span data-ttu-id="7d933-103">장치의 저장소 계정에 해당 하는 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d933-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="7d933-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d933-104">SYNTAX</span></span>

### <span data-ttu-id="7d933-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d933-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d933-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d933-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d933-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d933-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d933-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d933-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7d933-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7d933-109">DESCRIPTION</span></span>
<span data-ttu-id="7d933-110">**AzDataBoxEdgeStorageAccountCredential** Cmdlet은 데이터 상자 가장자리 디바이스의 해당 저장소 계정에 대 한 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d933-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="7d933-111">특정 저장소 계정 자격 증명에 대 한 정보를 얻기 위해 이름, 리소스 그룹 이름 및 디바이스 이름 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d933-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="7d933-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7d933-112">EXAMPLES</span></span>

### <span data-ttu-id="7d933-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d933-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="7d933-114">변수</span><span class="sxs-lookup"><span data-stu-id="7d933-114">PARAMETERS</span></span>

### <span data-ttu-id="7d933-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d933-115">-DefaultProfile</span></span>
<span data-ttu-id="7d933-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d933-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d933-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="7d933-117">-DeviceName</span></span>
<span data-ttu-id="7d933-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="7d933-118">Device Name</span></span>

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

### <span data-ttu-id="7d933-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7d933-119">-DeviceObject</span></span>
<span data-ttu-id="7d933-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7d933-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7d933-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7d933-121">-Name</span></span>
<span data-ttu-id="7d933-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7d933-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="7d933-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d933-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d933-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7d933-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7d933-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d933-125">-ResourceId</span></span>
<span data-ttu-id="7d933-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d933-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="7d933-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d933-127">CommonParameters</span></span>
<span data-ttu-id="7d933-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d933-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d933-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d933-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d933-130">입력</span><span class="sxs-lookup"><span data-stu-id="7d933-130">INPUTS</span></span>

### <span data-ttu-id="7d933-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7d933-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7d933-132">출력</span><span class="sxs-lookup"><span data-stu-id="7d933-132">OUTPUTS</span></span>

### <span data-ttu-id="7d933-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7d933-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7d933-134">상속자</span><span class="sxs-lookup"><span data-stu-id="7d933-134">NOTES</span></span>

## <span data-ttu-id="7d933-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d933-135">RELATED LINKS</span></span>

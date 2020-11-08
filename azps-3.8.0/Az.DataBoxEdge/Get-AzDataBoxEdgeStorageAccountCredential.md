---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043413"
---
# <span data-ttu-id="437d0-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="437d0-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="437d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="437d0-102">SYNOPSIS</span></span>
<span data-ttu-id="437d0-103">장치의 저장소 계정에 해당 하는 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="437d0-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="437d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="437d0-104">SYNTAX</span></span>

### <span data-ttu-id="437d0-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="437d0-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="437d0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="437d0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="437d0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="437d0-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="437d0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="437d0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="437d0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="437d0-109">DESCRIPTION</span></span>
<span data-ttu-id="437d0-110">**AzDataBoxEdgeStorageAccountCredential** Cmdlet은 데이터 상자 가장자리 디바이스의 해당 저장소 계정에 대 한 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="437d0-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="437d0-111">특정 저장소 계정 자격 증명에 대 한 정보를 얻기 위해 이름, 리소스 그룹 이름 및 디바이스 이름 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="437d0-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="437d0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="437d0-112">EXAMPLES</span></span>

### <span data-ttu-id="437d0-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="437d0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="437d0-114">변수</span><span class="sxs-lookup"><span data-stu-id="437d0-114">PARAMETERS</span></span>

### <span data-ttu-id="437d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="437d0-115">-DefaultProfile</span></span>
<span data-ttu-id="437d0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="437d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="437d0-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="437d0-117">-DeviceName</span></span>
<span data-ttu-id="437d0-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="437d0-118">Device Name</span></span>

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

### <span data-ttu-id="437d0-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="437d0-119">-DeviceObject</span></span>
<span data-ttu-id="437d0-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="437d0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="437d0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="437d0-121">-Name</span></span>
<span data-ttu-id="437d0-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="437d0-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="437d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="437d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="437d0-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="437d0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="437d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="437d0-125">-ResourceId</span></span>
<span data-ttu-id="437d0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="437d0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="437d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437d0-127">CommonParameters</span></span>
<span data-ttu-id="437d0-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="437d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437d0-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="437d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437d0-130">입력</span><span class="sxs-lookup"><span data-stu-id="437d0-130">INPUTS</span></span>

### <span data-ttu-id="437d0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="437d0-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="437d0-132">출력</span><span class="sxs-lookup"><span data-stu-id="437d0-132">OUTPUTS</span></span>

### <span data-ttu-id="437d0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="437d0-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="437d0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="437d0-134">NOTES</span></span>

## <span data-ttu-id="437d0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="437d0-135">RELATED LINKS</span></span>

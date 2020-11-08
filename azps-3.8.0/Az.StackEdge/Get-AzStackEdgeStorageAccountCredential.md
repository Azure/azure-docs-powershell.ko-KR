---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034518"
---
# <span data-ttu-id="1927c-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1927c-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1927c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1927c-102">SYNOPSIS</span></span>
<span data-ttu-id="1927c-103">장치의 저장소 계정에 해당 하는 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1927c-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="1927c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1927c-104">SYNTAX</span></span>

### <span data-ttu-id="1927c-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1927c-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1927c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1927c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1927c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1927c-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1927c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1927c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="1927c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1927c-109">DESCRIPTION</span></span>
<span data-ttu-id="1927c-110">**AzStackEdgeStorageAccountCredential** Cmdlet은 스택 경계 디바이스의 해당 저장소 계정에 대 한 저장소 계정 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1927c-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="1927c-111">특정 저장소 계정 자격 증명에 대 한 정보를 얻기 위해 이름, 리소스 그룹 이름 및 디바이스 이름 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1927c-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="1927c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1927c-112">EXAMPLES</span></span>

### <span data-ttu-id="1927c-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1927c-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="1927c-114">변수</span><span class="sxs-lookup"><span data-stu-id="1927c-114">PARAMETERS</span></span>

### <span data-ttu-id="1927c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1927c-115">-DefaultProfile</span></span>
<span data-ttu-id="1927c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1927c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1927c-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="1927c-117">-DeviceName</span></span>
<span data-ttu-id="1927c-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="1927c-118">Device Name</span></span>

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

### <span data-ttu-id="1927c-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="1927c-119">-DeviceObject</span></span>
<span data-ttu-id="1927c-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="1927c-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="1927c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1927c-121">-Name</span></span>
<span data-ttu-id="1927c-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="1927c-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1927c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1927c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1927c-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1927c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1927c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1927c-125">-ResourceId</span></span>
<span data-ttu-id="1927c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1927c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1927c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1927c-127">CommonParameters</span></span>
<span data-ttu-id="1927c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1927c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1927c-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1927c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1927c-130">입력</span><span class="sxs-lookup"><span data-stu-id="1927c-130">INPUTS</span></span>

### <span data-ttu-id="1927c-131">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="1927c-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="1927c-132">출력</span><span class="sxs-lookup"><span data-stu-id="1927c-132">OUTPUTS</span></span>

### <span data-ttu-id="1927c-133">StackEdge. PSStackEdgeStorageAccountCredential에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="1927c-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1927c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="1927c-134">NOTES</span></span>

## <span data-ttu-id="1927c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1927c-135">RELATED LINKS</span></span>
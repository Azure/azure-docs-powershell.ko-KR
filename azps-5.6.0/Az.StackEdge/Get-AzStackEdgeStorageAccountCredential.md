---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: efb9c7828417596afecc21fc5e5c2b2b8f7c81b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007568"
---
# <span data-ttu-id="c0051-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c0051-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c0051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0051-102">SYNOPSIS</span></span>
<span data-ttu-id="c0051-103">디바이스의 저장소 계정에 해당하는 저장소 계정 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0051-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="c0051-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0051-104">SYNTAX</span></span>

### <span data-ttu-id="c0051-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0051-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0051-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0051-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0051-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0051-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0051-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0051-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c0051-109">설명</span><span class="sxs-lookup"><span data-stu-id="c0051-109">DESCRIPTION</span></span>
<span data-ttu-id="c0051-110">**Get-AzStackEdgeStorageAccountCredential** cmdlet은 Stack Edge 디바이스에서 해당 저장소 계정에 대한 저장소 계정 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c0051-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="c0051-111">이름, 리소스 그룹 이름 및 디바이스 이름 매개 변수를 지정하여 특정 저장소 계정 자격 증명에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0051-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="c0051-112">예제</span><span class="sxs-lookup"><span data-stu-id="c0051-112">EXAMPLES</span></span>

### <span data-ttu-id="c0051-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0051-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="c0051-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0051-114">PARAMETERS</span></span>

### <span data-ttu-id="c0051-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0051-115">-DefaultProfile</span></span>
<span data-ttu-id="c0051-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0051-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0051-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c0051-117">-DeviceName</span></span>
<span data-ttu-id="c0051-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="c0051-118">Device Name</span></span>

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

### <span data-ttu-id="c0051-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c0051-119">-DeviceObject</span></span>
<span data-ttu-id="c0051-120">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="c0051-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c0051-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0051-121">-Name</span></span>
<span data-ttu-id="c0051-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="c0051-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="c0051-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0051-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0051-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c0051-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c0051-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0051-125">-ResourceId</span></span>
<span data-ttu-id="c0051-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0051-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c0051-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0051-127">CommonParameters</span></span>
<span data-ttu-id="c0051-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0051-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0051-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0051-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0051-130">입력</span><span class="sxs-lookup"><span data-stu-id="c0051-130">INPUTS</span></span>

### <span data-ttu-id="c0051-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c0051-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c0051-132">출력</span><span class="sxs-lookup"><span data-stu-id="c0051-132">OUTPUTS</span></span>

### <span data-ttu-id="c0051-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c0051-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="c0051-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0051-134">NOTES</span></span>

## <span data-ttu-id="c0051-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0051-135">RELATED LINKS</span></span>

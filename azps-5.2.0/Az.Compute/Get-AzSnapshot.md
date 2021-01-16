---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 135d9fab47f06dbd2fca1273094548e27273b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332325"
---
# <span data-ttu-id="92cc1-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="92cc1-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="92cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="92cc1-103">스냅숏의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="92cc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="92cc1-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92cc1-105">설명</span><span class="sxs-lookup"><span data-stu-id="92cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="92cc1-106">**Get-AzSnapshot** cmdlet은 스냅숏의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="92cc1-107">예제</span><span class="sxs-lookup"><span data-stu-id="92cc1-107">EXAMPLES</span></span>

### <span data-ttu-id="92cc1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="92cc1-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="92cc1-109">이 명령은 구독의 모든 스냅숏의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="92cc1-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="92cc1-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="92cc1-111">이 명령은 "ResourceGroupName1"이라는 리소스 그룹에 있는 모든 스냅숏의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="92cc1-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="92cc1-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="92cc1-113">이 명령은 "ResourceGroupName1"이라는 리소스 그룹에서 "SnapshotName1"이라는 스냅숏의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="92cc1-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="92cc1-114">Example 4</span></span>
```
PS C:\> Get-AzSnapshot -SnapshotName "SnapshotName*"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="92cc1-115">이 명령은 "SnapshotName"으로 시작하는 모든 스냅숏을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-115">This command gets all snapshots that start with "SnapshotName"</span></span>

## <span data-ttu-id="92cc1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92cc1-116">PARAMETERS</span></span>

### <span data-ttu-id="92cc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cc1-117">-DefaultProfile</span></span>
<span data-ttu-id="92cc1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92cc1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92cc1-119">-ResourceGroupName</span></span>
<span data-ttu-id="92cc1-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="92cc1-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="92cc1-121">-SnapshotName</span></span>
<span data-ttu-id="92cc1-122">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="92cc1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cc1-123">CommonParameters</span></span>
<span data-ttu-id="92cc1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92cc1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cc1-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92cc1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cc1-126">입력</span><span class="sxs-lookup"><span data-stu-id="92cc1-126">INPUTS</span></span>

### <span data-ttu-id="92cc1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="92cc1-127">System.String</span></span>

## <span data-ttu-id="92cc1-128">출력</span><span class="sxs-lookup"><span data-stu-id="92cc1-128">OUTPUTS</span></span>

### <span data-ttu-id="92cc1-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="92cc1-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="92cc1-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92cc1-130">NOTES</span></span>

## <span data-ttu-id="92cc1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92cc1-131">RELATED LINKS</span></span>

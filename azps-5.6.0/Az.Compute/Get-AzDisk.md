---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 58b5e0aad0982b08256694f842e55929ca7dfcc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969371"
---
# <span data-ttu-id="1c899-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="1c899-101">Get-AzDisk</span></span>

## <span data-ttu-id="1c899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c899-102">SYNOPSIS</span></span>
<span data-ttu-id="1c899-103">관리 디스크의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="1c899-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c899-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c899-105">설명</span><span class="sxs-lookup"><span data-stu-id="1c899-105">DESCRIPTION</span></span>
<span data-ttu-id="1c899-106">**Get-AzDisk** cmdlet은 관리 디스크의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="1c899-107">예제</span><span class="sxs-lookup"><span data-stu-id="1c899-107">EXAMPLES</span></span>

### <span data-ttu-id="1c899-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c899-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/Disk01
Name               : Disk01
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="1c899-109">이 명령은 리소스 그룹 'ResourceGroup01'에서 'Disk01'이라는 디스크의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1c899-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="1c899-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="1c899-111">이 명령은 리소스 그룹 'ResourceGroup01'의 모든 디스크의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1c899-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="1c899-112">Example 3</span></span>
```
PS C:\> Get-AzDisk

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="1c899-113">이 명령은 구독 아래에서 모든 디스크의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-113">This command gets the properties of all disks under the subscription.</span></span>

### <span data-ttu-id="1c899-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="1c899-114">Example 4</span></span>
```
PS C:\> Get-AzDisk -Name win_OsDisk*

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="1c899-115">이 명령은 구독 이름으로 시작하여 모든 디스크의 속성을 win1_OsDisk.</span><span class="sxs-lookup"><span data-stu-id="1c899-115">This command gets the properties of all disks under the subscription name starting with win1_OsDisk.</span></span>

## <span data-ttu-id="1c899-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c899-116">PARAMETERS</span></span>

### <span data-ttu-id="1c899-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c899-117">-DefaultProfile</span></span>
<span data-ttu-id="1c899-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c899-119">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1c899-119">-DiskName</span></span>
<span data-ttu-id="1c899-120">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-120">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="1c899-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c899-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c899-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c899-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c899-123">CommonParameters</span></span>
<span data-ttu-id="1c899-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c899-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c899-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c899-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c899-126">입력</span><span class="sxs-lookup"><span data-stu-id="1c899-126">INPUTS</span></span>

### <span data-ttu-id="1c899-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1c899-127">System.String</span></span>

## <span data-ttu-id="1c899-128">출력</span><span class="sxs-lookup"><span data-stu-id="1c899-128">OUTPUTS</span></span>

### <span data-ttu-id="1c899-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="1c899-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1c899-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c899-130">NOTES</span></span>

## <span data-ttu-id="1c899-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c899-131">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493893"
---
# <span data-ttu-id="a563d-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a563d-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="a563d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a563d-102">SYNOPSIS</span></span>
<span data-ttu-id="a563d-103">갤러리 이미지 버전을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="a563d-104">구문</span><span class="sxs-lookup"><span data-stu-id="a563d-104">SYNTAX</span></span>

### <span data-ttu-id="a563d-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="a563d-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a563d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a563d-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a563d-107">설명</span><span class="sxs-lookup"><span data-stu-id="a563d-107">DESCRIPTION</span></span>
<span data-ttu-id="a563d-108">갤러리 이미지 버전을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="a563d-109">예제</span><span class="sxs-lookup"><span data-stu-id="a563d-109">EXAMPLES</span></span>

### <span data-ttu-id="a563d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a563d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="a563d-111">갤러리 이미지 버전을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-111">Get the gallery image version.</span></span>

### <span data-ttu-id="a563d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a563d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="a563d-113">"1"로 시작하는 갤러리 이미지 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="a563d-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="a563d-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="a563d-115">모든 갤러리 이미지 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="a563d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a563d-116">PARAMETERS</span></span>

### <span data-ttu-id="a563d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a563d-117">-DefaultProfile</span></span>
<span data-ttu-id="a563d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a563d-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="a563d-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="a563d-120">복제 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a563d-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a563d-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="a563d-122">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a563d-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="a563d-123">-GalleryName</span></span>
<span data-ttu-id="a563d-124">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a563d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a563d-125">-Name</span></span>
<span data-ttu-id="a563d-126">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a563d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a563d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a563d-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a563d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a563d-129">-ResourceId</span></span>
<span data-ttu-id="a563d-130">갤러리 이미지 버전에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a563d-130">The resource ID for the gallery image version</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a563d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a563d-131">CommonParameters</span></span>
<span data-ttu-id="a563d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a563d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a563d-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a563d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a563d-134">입력</span><span class="sxs-lookup"><span data-stu-id="a563d-134">INPUTS</span></span>

### <span data-ttu-id="a563d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a563d-135">System.String</span></span>

### <span data-ttu-id="a563d-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a563d-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a563d-137">출력</span><span class="sxs-lookup"><span data-stu-id="a563d-137">OUTPUTS</span></span>

### <span data-ttu-id="a563d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a563d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="a563d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a563d-139">NOTES</span></span>

## <span data-ttu-id="a563d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a563d-140">RELATED LINKS</span></span>

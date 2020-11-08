---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048141"
---
# <span data-ttu-id="6225d-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6225d-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="6225d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6225d-102">SYNOPSIS</span></span>
<span data-ttu-id="6225d-103">갤러리 이미지 버전을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="6225d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6225d-104">SYNTAX</span></span>

### <span data-ttu-id="6225d-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="6225d-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6225d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6225d-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6225d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6225d-107">DESCRIPTION</span></span>
<span data-ttu-id="6225d-108">갤러리 이미지 버전을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="6225d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6225d-109">EXAMPLES</span></span>

### <span data-ttu-id="6225d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6225d-110">Example 1</span></span>
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

<span data-ttu-id="6225d-111">갤러리 이미지 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-111">Get the gallery image version.</span></span>

### <span data-ttu-id="6225d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6225d-112">Example 2</span></span>
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

<span data-ttu-id="6225d-113">"1"로 시작 하는 갤러리 이미지 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="6225d-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="6225d-114">Example 3</span></span>
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

<span data-ttu-id="6225d-115">모든 갤러리 이미지 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="6225d-116">변수</span><span class="sxs-lookup"><span data-stu-id="6225d-116">PARAMETERS</span></span>

### <span data-ttu-id="6225d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6225d-117">-DefaultProfile</span></span>
<span data-ttu-id="6225d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6225d-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="6225d-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="6225d-120">복제 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-120">Show replication status.</span></span>

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

### <span data-ttu-id="6225d-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6225d-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="6225d-122">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6225d-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6225d-123">-GalleryName</span></span>
<span data-ttu-id="6225d-124">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="6225d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="6225d-125">-Name</span></span>
<span data-ttu-id="6225d-126">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-126">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="6225d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6225d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6225d-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6225d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6225d-129">-ResourceId</span></span>
<span data-ttu-id="6225d-130">갤러리 이미지 버전의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6225d-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="6225d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6225d-131">CommonParameters</span></span>
<span data-ttu-id="6225d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6225d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6225d-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6225d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6225d-134">입력</span><span class="sxs-lookup"><span data-stu-id="6225d-134">INPUTS</span></span>

### <span data-ttu-id="6225d-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6225d-135">System.String</span></span>

### <span data-ttu-id="6225d-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6225d-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6225d-137">출력</span><span class="sxs-lookup"><span data-stu-id="6225d-137">OUTPUTS</span></span>

### <span data-ttu-id="6225d-138">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="6225d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="6225d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6225d-139">NOTES</span></span>

## <span data-ttu-id="6225d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6225d-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 0599226e4b9856378804aca7bce013b03456b1ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969275"
---
# <span data-ttu-id="840e8-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="840e8-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="840e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="840e8-102">SYNOPSIS</span></span>
<span data-ttu-id="840e8-103">갤러리 이미지 정의를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="840e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="840e8-104">SYNTAX</span></span>

### <span data-ttu-id="840e8-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="840e8-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="840e8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="840e8-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="840e8-107">설명</span><span class="sxs-lookup"><span data-stu-id="840e8-107">DESCRIPTION</span></span>
<span data-ttu-id="840e8-108">갤러리 이미지 정의를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="840e8-109">예제</span><span class="sxs-lookup"><span data-stu-id="840e8-109">EXAMPLES</span></span>

### <span data-ttu-id="840e8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="840e8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="840e8-111">갤러리 이미지 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="840e8-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="840e8-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="840e8-113">"image"로 시작하는 갤러리 이미지 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="840e8-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="840e8-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="840e8-115">갤러리1에서 갤러리 이미지 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="840e8-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="840e8-116">PARAMETERS</span></span>

### <span data-ttu-id="840e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840e8-117">-DefaultProfile</span></span>
<span data-ttu-id="840e8-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="840e8-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="840e8-119">-GalleryName</span></span>
<span data-ttu-id="840e8-120">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="840e8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="840e8-121">-Name</span></span>
<span data-ttu-id="840e8-122">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="840e8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840e8-123">-ResourceGroupName</span></span>
<span data-ttu-id="840e8-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="840e8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="840e8-125">-ResourceId</span></span>
<span data-ttu-id="840e8-126">갤러리 이미지 정의에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="840e8-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="840e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840e8-127">CommonParameters</span></span>
<span data-ttu-id="840e8-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="840e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840e8-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="840e8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840e8-130">입력</span><span class="sxs-lookup"><span data-stu-id="840e8-130">INPUTS</span></span>

### <span data-ttu-id="840e8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="840e8-131">System.String</span></span>

## <span data-ttu-id="840e8-132">출력</span><span class="sxs-lookup"><span data-stu-id="840e8-132">OUTPUTS</span></span>

### <span data-ttu-id="840e8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="840e8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="840e8-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="840e8-134">NOTES</span></span>

## <span data-ttu-id="840e8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="840e8-135">RELATED LINKS</span></span>

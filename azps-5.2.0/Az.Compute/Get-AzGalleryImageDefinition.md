---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332745"
---
# <span data-ttu-id="033b2-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="033b2-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="033b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="033b2-102">SYNOPSIS</span></span>
<span data-ttu-id="033b2-103">갤러리 이미지 정의를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="033b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="033b2-104">SYNTAX</span></span>

### <span data-ttu-id="033b2-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="033b2-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="033b2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="033b2-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="033b2-107">설명</span><span class="sxs-lookup"><span data-stu-id="033b2-107">DESCRIPTION</span></span>
<span data-ttu-id="033b2-108">갤러리 이미지 정의를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="033b2-109">예제</span><span class="sxs-lookup"><span data-stu-id="033b2-109">EXAMPLES</span></span>

### <span data-ttu-id="033b2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="033b2-110">Example 1</span></span>
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

<span data-ttu-id="033b2-111">갤러리 이미지 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="033b2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="033b2-112">Example 2</span></span>
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

<span data-ttu-id="033b2-113">"image"로 시작하는 갤러리 이미지 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="033b2-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="033b2-114">Example 3</span></span>
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

<span data-ttu-id="033b2-115">gallery1에서 갤러리 이미지 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="033b2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="033b2-116">PARAMETERS</span></span>

### <span data-ttu-id="033b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033b2-117">-DefaultProfile</span></span>
<span data-ttu-id="033b2-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="033b2-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="033b2-119">-GalleryName</span></span>
<span data-ttu-id="033b2-120">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="033b2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="033b2-121">-Name</span></span>
<span data-ttu-id="033b2-122">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="033b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="033b2-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="033b2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="033b2-125">-ResourceId</span></span>
<span data-ttu-id="033b2-126">갤러리 이미지 정의에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="033b2-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="033b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033b2-127">CommonParameters</span></span>
<span data-ttu-id="033b2-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="033b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033b2-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="033b2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033b2-130">입력</span><span class="sxs-lookup"><span data-stu-id="033b2-130">INPUTS</span></span>

### <span data-ttu-id="033b2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="033b2-131">System.String</span></span>

## <span data-ttu-id="033b2-132">출력</span><span class="sxs-lookup"><span data-stu-id="033b2-132">OUTPUTS</span></span>

### <span data-ttu-id="033b2-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="033b2-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="033b2-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="033b2-134">NOTES</span></span>

## <span data-ttu-id="033b2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="033b2-135">RELATED LINKS</span></span>

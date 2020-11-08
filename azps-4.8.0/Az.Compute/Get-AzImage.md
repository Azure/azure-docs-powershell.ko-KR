---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048450"
---
# <span data-ttu-id="b78ae-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="b78ae-101">Get-AzImage</span></span>

## <span data-ttu-id="b78ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b78ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b78ae-103">이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="b78ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b78ae-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b78ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b78ae-106">**Get-AzImage** cmdlet은 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="b78ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b78ae-107">EXAMPLES</span></span>

### <span data-ttu-id="b78ae-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b78ae-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="b78ae-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Image01 ' 인 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b78ae-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="b78ae-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="b78ae-111">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b78ae-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="b78ae-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="b78ae-113">이 명령은 구독에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="b78ae-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="b78ae-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="b78ae-115">이 명령은 "Image"로 시작 하는 구독 아래에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="b78ae-116">변수</span><span class="sxs-lookup"><span data-stu-id="b78ae-116">PARAMETERS</span></span>

### <span data-ttu-id="b78ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78ae-117">-DefaultProfile</span></span>
<span data-ttu-id="b78ae-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b78ae-119">-확장</span><span class="sxs-lookup"><span data-stu-id="b78ae-119">-Expand</span></span>
<span data-ttu-id="b78ae-120">확장 식 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b78ae-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b78ae-121">-ImageName</span></span>
<span data-ttu-id="b78ae-122">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b78ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b78ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="b78ae-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b78ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78ae-125">CommonParameters</span></span>
<span data-ttu-id="b78ae-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78ae-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b78ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78ae-128">입력</span><span class="sxs-lookup"><span data-stu-id="b78ae-128">INPUTS</span></span>

### <span data-ttu-id="b78ae-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b78ae-129">System.String</span></span>

## <span data-ttu-id="b78ae-130">출력</span><span class="sxs-lookup"><span data-stu-id="b78ae-130">OUTPUTS</span></span>

### <span data-ttu-id="b78ae-131">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="b78ae-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b78ae-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b78ae-132">NOTES</span></span>

## <span data-ttu-id="b78ae-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b78ae-133">RELATED LINKS</span></span>

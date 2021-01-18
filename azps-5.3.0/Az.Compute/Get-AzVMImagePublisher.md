---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496074"
---
# <span data-ttu-id="30c44-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="30c44-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="30c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30c44-102">SYNOPSIS</span></span>
<span data-ttu-id="30c44-103">VMImage 게시자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30c44-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="30c44-104">구문</span><span class="sxs-lookup"><span data-stu-id="30c44-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c44-105">설명</span><span class="sxs-lookup"><span data-stu-id="30c44-105">DESCRIPTION</span></span>
<span data-ttu-id="30c44-106">**Get-AzVMImagePublisher** cmdlet은 VMImage 게시자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30c44-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="30c44-107">예제</span><span class="sxs-lookup"><span data-stu-id="30c44-107">EXAMPLES</span></span>

### <span data-ttu-id="30c44-108">예제 1: 지역에 대한 VMImage 게시자 얻기</span><span class="sxs-lookup"><span data-stu-id="30c44-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="30c44-109">이 명령은 Azure 프로필 내에서 미국 중부 지역에 대한 VMImage 인스턴스의 게시자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30c44-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="30c44-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30c44-110">PARAMETERS</span></span>

### <span data-ttu-id="30c44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c44-111">-DefaultProfile</span></span>
<span data-ttu-id="30c44-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30c44-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c44-113">-Location</span><span class="sxs-lookup"><span data-stu-id="30c44-113">-Location</span></span>
<span data-ttu-id="30c44-114">VMImage의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30c44-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c44-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c44-115">CommonParameters</span></span>
<span data-ttu-id="30c44-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30c44-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c44-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30c44-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c44-118">입력</span><span class="sxs-lookup"><span data-stu-id="30c44-118">INPUTS</span></span>

### <span data-ttu-id="30c44-119">System.String</span><span class="sxs-lookup"><span data-stu-id="30c44-119">System.String</span></span>

## <span data-ttu-id="30c44-120">출력</span><span class="sxs-lookup"><span data-stu-id="30c44-120">OUTPUTS</span></span>

### <span data-ttu-id="30c44-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="30c44-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="30c44-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30c44-122">NOTES</span></span>

## <span data-ttu-id="30c44-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30c44-123">RELATED LINKS</span></span>

[<span data-ttu-id="30c44-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="30c44-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="30c44-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="30c44-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="30c44-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="30c44-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="30c44-127">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="30c44-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042883"
---
# <span data-ttu-id="c3ee4-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c3ee4-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="c3ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ee4-103">VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="c3ee4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3ee4-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3ee4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c3ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ee4-106">**AzVMImagePublisher** Cmdlet은 VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="c3ee4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c3ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ee4-108">예제 1: 영역에 대해 VMImage 게시자 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3ee4-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="c3ee4-109">이 명령은 Azure 프로필 내의 중앙 US 지역에 대 한 VMImage 인스턴스의 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="c3ee4-110">변수</span><span class="sxs-lookup"><span data-stu-id="c3ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="c3ee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ee4-111">-DefaultProfile</span></span>
<span data-ttu-id="c3ee4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ee4-113">-위치</span><span class="sxs-lookup"><span data-stu-id="c3ee4-113">-Location</span></span>
<span data-ttu-id="c3ee4-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="c3ee4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ee4-115">CommonParameters</span></span>
<span data-ttu-id="c3ee4-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ee4-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ee4-118">입력</span><span class="sxs-lookup"><span data-stu-id="c3ee4-118">INPUTS</span></span>

### <span data-ttu-id="c3ee4-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3ee4-119">System.String</span></span>

## <span data-ttu-id="c3ee4-120">출력</span><span class="sxs-lookup"><span data-stu-id="c3ee4-120">OUTPUTS</span></span>

### <span data-ttu-id="c3ee4-121">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="c3ee4-122">상속자</span><span class="sxs-lookup"><span data-stu-id="c3ee4-122">NOTES</span></span>

## <span data-ttu-id="c3ee4-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3ee4-123">RELATED LINKS</span></span>

[<span data-ttu-id="c3ee4-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c3ee4-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c3ee4-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c3ee4-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="c3ee4-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c3ee4-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="c3ee4-127">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c3ee4-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



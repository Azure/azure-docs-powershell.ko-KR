---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: bd463ffad1c38265dbca894748d0c5b9a479fade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536444"
---
# <span data-ttu-id="4573f-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4573f-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="4573f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4573f-102">SYNOPSIS</span></span>
<span data-ttu-id="4573f-103">VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4573f-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4573f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4573f-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4573f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4573f-105">DESCRIPTION</span></span>
<span data-ttu-id="4573f-106">**AzureRmVMImagePublisher** Cmdlet은 VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4573f-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="4573f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4573f-107">EXAMPLES</span></span>

### <span data-ttu-id="4573f-108">예제 1: 영역에 대해 VMImage 게시자 가져오기</span><span class="sxs-lookup"><span data-stu-id="4573f-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="4573f-109">이 명령은 Azure 프로필 내의 중앙 US 지역에 대 한 VMImage 인스턴스의 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4573f-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="4573f-110">변수</span><span class="sxs-lookup"><span data-stu-id="4573f-110">PARAMETERS</span></span>

### <span data-ttu-id="4573f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4573f-111">-DefaultProfile</span></span>
<span data-ttu-id="4573f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4573f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4573f-113">-위치</span><span class="sxs-lookup"><span data-stu-id="4573f-113">-Location</span></span>
<span data-ttu-id="4573f-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4573f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4573f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4573f-115">CommonParameters</span></span>
<span data-ttu-id="4573f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4573f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4573f-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4573f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4573f-118">입력</span><span class="sxs-lookup"><span data-stu-id="4573f-118">INPUTS</span></span>

## <span data-ttu-id="4573f-119">출력</span><span class="sxs-lookup"><span data-stu-id="4573f-119">OUTPUTS</span></span>

## <span data-ttu-id="4573f-120">상속자</span><span class="sxs-lookup"><span data-stu-id="4573f-120">NOTES</span></span>

## <span data-ttu-id="4573f-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4573f-121">RELATED LINKS</span></span>

[<span data-ttu-id="4573f-122">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4573f-122">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4573f-123">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4573f-123">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4573f-124">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4573f-124">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="4573f-125">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4573f-125">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)



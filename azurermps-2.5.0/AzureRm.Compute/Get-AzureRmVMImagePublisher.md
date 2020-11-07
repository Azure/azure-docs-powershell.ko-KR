---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882393"
---
# <span data-ttu-id="f2772-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f2772-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="f2772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2772-102">SYNOPSIS</span></span>
<span data-ttu-id="f2772-103">VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2772-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2772-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2772-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2772-105">DESCRIPTION</span></span>
<span data-ttu-id="f2772-106">**AzureRmVMImagePublisher** Cmdlet은 VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="f2772-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2772-107">EXAMPLES</span></span>

### <span data-ttu-id="f2772-108">예제 1: 영역에 대해 VMImage 게시자 가져오기</span><span class="sxs-lookup"><span data-stu-id="f2772-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="f2772-109">이 명령은 Azure 프로필 내의 중앙 US 지역에 대 한 VMImage 인스턴스의 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="f2772-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2772-110">PARAMETERS</span></span>

### <span data-ttu-id="f2772-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2772-111">-DefaultProfile</span></span>
<span data-ttu-id="f2772-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2772-113">-위치</span><span class="sxs-lookup"><span data-stu-id="f2772-113">-Location</span></span>
<span data-ttu-id="f2772-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2772-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2772-115">CommonParameters</span></span>
<span data-ttu-id="f2772-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2772-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2772-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2772-118">입력</span><span class="sxs-lookup"><span data-stu-id="f2772-118">INPUTS</span></span>

### <span data-ttu-id="f2772-119">않아야</span><span class="sxs-lookup"><span data-stu-id="f2772-119">None</span></span>
<span data-ttu-id="f2772-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2772-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2772-121">출력</span><span class="sxs-lookup"><span data-stu-id="f2772-121">OUTPUTS</span></span>

### <span data-ttu-id="f2772-122">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="f2772-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="f2772-123">상속자</span><span class="sxs-lookup"><span data-stu-id="f2772-123">NOTES</span></span>

## <span data-ttu-id="f2772-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2772-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2772-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f2772-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f2772-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f2772-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f2772-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f2772-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f2772-128">저장-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f2772-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)



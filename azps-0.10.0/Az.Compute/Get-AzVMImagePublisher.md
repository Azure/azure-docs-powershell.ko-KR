---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: dcb5913176af352c39867f7029523765aca0d781
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877054"
---
# <span data-ttu-id="2e1ca-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2e1ca-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="2e1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1ca-103">VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="2e1ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e1ca-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e1ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2e1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1ca-106">**AzVMImagePublisher** Cmdlet은 VMImage 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="2e1ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2e1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="2e1ca-108">예제 1: 영역에 대해 VMImage 게시자 가져오기</span><span class="sxs-lookup"><span data-stu-id="2e1ca-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="2e1ca-109">이 명령은 Azure 프로필 내의 중앙 US 지역에 대 한 VMImage 인스턴스의 게시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="2e1ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="2e1ca-110">PARAMETERS</span></span>

### <span data-ttu-id="2e1ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1ca-111">-DefaultProfile</span></span>
<span data-ttu-id="2e1ca-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e1ca-113">-위치</span><span class="sxs-lookup"><span data-stu-id="2e1ca-113">-Location</span></span>
<span data-ttu-id="2e1ca-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="2e1ca-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1ca-115">CommonParameters</span></span>
<span data-ttu-id="2e1ca-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1ca-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e1ca-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1ca-118">입력</span><span class="sxs-lookup"><span data-stu-id="2e1ca-118">INPUTS</span></span>

### <span data-ttu-id="2e1ca-119">않아야</span><span class="sxs-lookup"><span data-stu-id="2e1ca-119">None</span></span>
<span data-ttu-id="2e1ca-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e1ca-121">출력</span><span class="sxs-lookup"><span data-stu-id="2e1ca-121">OUTPUTS</span></span>

### <span data-ttu-id="2e1ca-122">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="2e1ca-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="2e1ca-123">상속자</span><span class="sxs-lookup"><span data-stu-id="2e1ca-123">NOTES</span></span>

## <span data-ttu-id="2e1ca-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e1ca-124">RELATED LINKS</span></span>

[<span data-ttu-id="2e1ca-125">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2e1ca-125">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="2e1ca-126">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2e1ca-126">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="2e1ca-127">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2e1ca-127">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="2e1ca-128">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2e1ca-128">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



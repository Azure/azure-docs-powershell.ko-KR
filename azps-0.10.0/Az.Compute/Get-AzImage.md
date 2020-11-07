---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 13829081952be7ab79c6d7badde4dc687aa845ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877085"
---
# <span data-ttu-id="56401-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="56401-101">Get-AzImage</span></span>

## <span data-ttu-id="56401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56401-102">SYNOPSIS</span></span>
<span data-ttu-id="56401-103">이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56401-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="56401-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56401-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56401-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56401-105">DESCRIPTION</span></span>
<span data-ttu-id="56401-106">**Get-AzImage** cmdlet은 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56401-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="56401-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56401-107">EXAMPLES</span></span>

### <span data-ttu-id="56401-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="56401-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="56401-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Image01 ' 인 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56401-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="56401-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="56401-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="56401-111">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56401-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="56401-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="56401-112">Example 3</span></span>
```
PS C:\> Get-AzImage
```

<span data-ttu-id="56401-113">이 명령은 구독에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56401-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="56401-114">변수</span><span class="sxs-lookup"><span data-stu-id="56401-114">PARAMETERS</span></span>

### <span data-ttu-id="56401-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56401-115">-DefaultProfile</span></span>
<span data-ttu-id="56401-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56401-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56401-117">-확장</span><span class="sxs-lookup"><span data-stu-id="56401-117">-Expand</span></span>
<span data-ttu-id="56401-118">확장 식 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56401-118">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56401-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="56401-119">-ImageName</span></span>
<span data-ttu-id="56401-120">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56401-120">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56401-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56401-121">-ResourceGroupName</span></span>
<span data-ttu-id="56401-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56401-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56401-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56401-123">CommonParameters</span></span>
<span data-ttu-id="56401-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56401-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56401-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56401-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56401-126">입력</span><span class="sxs-lookup"><span data-stu-id="56401-126">INPUTS</span></span>

### <span data-ttu-id="56401-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56401-127">System.String</span></span>

## <span data-ttu-id="56401-128">출력</span><span class="sxs-lookup"><span data-stu-id="56401-128">OUTPUTS</span></span>

### <span data-ttu-id="56401-129">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="56401-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="56401-130">상속자</span><span class="sxs-lookup"><span data-stu-id="56401-130">NOTES</span></span>

## <span data-ttu-id="56401-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56401-131">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: c1d7a7128c0fd4774c99799695e0d041a08c8053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711292"
---
# <span data-ttu-id="550d7-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="550d7-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="550d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="550d7-102">SYNOPSIS</span></span>
<span data-ttu-id="550d7-103">이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="550d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="550d7-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="550d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="550d7-105">DESCRIPTION</span></span>
<span data-ttu-id="550d7-106">**Get-AzureRmImage** cmdlet은 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="550d7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="550d7-107">EXAMPLES</span></span>

### <span data-ttu-id="550d7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="550d7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="550d7-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Image01 ' 인 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="550d7-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="550d7-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="550d7-111">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="550d7-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="550d7-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="550d7-113">이 명령은 구독에 있는 모든 이미지의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="550d7-114">변수</span><span class="sxs-lookup"><span data-stu-id="550d7-114">PARAMETERS</span></span>

### <span data-ttu-id="550d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550d7-115">-DefaultProfile</span></span>
<span data-ttu-id="550d7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="550d7-117">-확장</span><span class="sxs-lookup"><span data-stu-id="550d7-117">-Expand</span></span>
<span data-ttu-id="550d7-118">확장 식 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550d7-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="550d7-119">-ImageName</span></span>
<span data-ttu-id="550d7-120">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="550d7-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550d7-123">CommonParameters</span></span>
<span data-ttu-id="550d7-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="550d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550d7-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="550d7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550d7-126">입력</span><span class="sxs-lookup"><span data-stu-id="550d7-126">INPUTS</span></span>

### <span data-ttu-id="550d7-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="550d7-127">System.String</span></span>

## <span data-ttu-id="550d7-128">출력</span><span class="sxs-lookup"><span data-stu-id="550d7-128">OUTPUTS</span></span>

### <span data-ttu-id="550d7-129">System. 개체</span><span class="sxs-lookup"><span data-stu-id="550d7-129">System.Object</span></span>

## <span data-ttu-id="550d7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="550d7-130">NOTES</span></span>

## <span data-ttu-id="550d7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="550d7-131">RELATED LINKS</span></span>


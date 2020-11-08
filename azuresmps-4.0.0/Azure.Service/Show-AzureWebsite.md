---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045785"
---
# <span data-ttu-id="1572c-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1572c-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="1572c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1572c-102">SYNOPSIS</span></span>
<span data-ttu-id="1572c-103">지정 된 웹 사이트에서 브라우저를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="1572c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1572c-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1572c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1572c-105">DESCRIPTION</span></span>
<span data-ttu-id="1572c-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1572c-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1572c-108">**AzureWebsite** cmdlet은 지정 된 웹 사이트에서 브라우저를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="1572c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1572c-109">EXAMPLES</span></span>

## <span data-ttu-id="1572c-110">변수</span><span class="sxs-lookup"><span data-stu-id="1572c-110">PARAMETERS</span></span>

### <span data-ttu-id="1572c-111">-이름</span><span class="sxs-lookup"><span data-stu-id="1572c-111">-Name</span></span>
<span data-ttu-id="1572c-112">브라우저에서 열려는 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-112">Specifies the name of the site to open in the browser.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1572c-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="1572c-113">-Profile</span></span>
<span data-ttu-id="1572c-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1572c-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1572c-116">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1572c-116">-Slot</span></span>
<span data-ttu-id="1572c-117">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-117">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1572c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1572c-118">CommonParameters</span></span>
<span data-ttu-id="1572c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1572c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1572c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1572c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1572c-121">입력</span><span class="sxs-lookup"><span data-stu-id="1572c-121">INPUTS</span></span>

## <span data-ttu-id="1572c-122">출력</span><span class="sxs-lookup"><span data-stu-id="1572c-122">OUTPUTS</span></span>

## <span data-ttu-id="1572c-123">상속자</span><span class="sxs-lookup"><span data-stu-id="1572c-123">NOTES</span></span>

## <span data-ttu-id="1572c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1572c-124">RELATED LINKS</span></span>

[<span data-ttu-id="1572c-125">쇼-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="1572c-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="1572c-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1572c-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1572c-127">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1572c-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1572c-128">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1572c-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1572c-129">다시 시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1572c-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="1572c-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1572c-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)



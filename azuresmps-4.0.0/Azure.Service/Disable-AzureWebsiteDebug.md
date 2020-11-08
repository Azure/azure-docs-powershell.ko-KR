---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045691"
---
# <span data-ttu-id="bee07-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="bee07-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="bee07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee07-102">SYNOPSIS</span></span>
<span data-ttu-id="bee07-103">웹 사이트의 디버깅을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="bee07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bee07-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bee07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bee07-105">DESCRIPTION</span></span>
<span data-ttu-id="bee07-106">Visual Studio에서 웹 사이트의 디버깅을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="bee07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bee07-107">EXAMPLES</span></span>

### <span data-ttu-id="bee07-108">--------------웹 사이트 디버깅을 사용 하지 않도록 설정--------------</span><span class="sxs-lookup"><span data-stu-id="bee07-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="bee07-109">웹 사이트 MyWebsite에서 웹 사이트 디버깅을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="bee07-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="bee07-110">변수</span><span class="sxs-lookup"><span data-stu-id="bee07-110">PARAMETERS</span></span>

### <span data-ttu-id="bee07-111">-이름</span><span class="sxs-lookup"><span data-stu-id="bee07-111">-Name</span></span>
<span data-ttu-id="bee07-112">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="bee07-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bee07-113">-PassThru</span></span>
<span data-ttu-id="bee07-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bee07-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee07-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="bee07-116">-Profile</span></span>
<span data-ttu-id="bee07-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bee07-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bee07-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="bee07-119">-Slot</span></span>
<span data-ttu-id="bee07-120">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="bee07-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee07-121">CommonParameters</span></span>
<span data-ttu-id="bee07-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bee07-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee07-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee07-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee07-124">입력</span><span class="sxs-lookup"><span data-stu-id="bee07-124">INPUTS</span></span>

## <span data-ttu-id="bee07-125">출력</span><span class="sxs-lookup"><span data-stu-id="bee07-125">OUTPUTS</span></span>

## <span data-ttu-id="bee07-126">상속자</span><span class="sxs-lookup"><span data-stu-id="bee07-126">NOTES</span></span>

## <span data-ttu-id="bee07-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bee07-127">RELATED LINKS</span></span>

[<span data-ttu-id="bee07-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="bee07-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="bee07-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bee07-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="bee07-130">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bee07-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="bee07-131">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bee07-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="bee07-132">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="bee07-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045470"
---
# <span data-ttu-id="0b987-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b987-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="0b987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b987-102">SYNOPSIS</span></span>
<span data-ttu-id="0b987-103">지정 된 웹 사이트를 중지 한 다음 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="0b987-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b987-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b987-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b987-105">DESCRIPTION</span></span>
<span data-ttu-id="0b987-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0b987-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0b987-108">**AzureWebsite** cmdlet이 중지 된 다음 지정 된 웹 사이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="0b987-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0b987-109">EXAMPLES</span></span>

### <span data-ttu-id="0b987-110">예제 1: 웹 사이트 다시 시작</span><span class="sxs-lookup"><span data-stu-id="0b987-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="0b987-111">이 예제에서는 MyWebsite 이라는 웹 사이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="0b987-112">변수</span><span class="sxs-lookup"><span data-stu-id="0b987-112">PARAMETERS</span></span>

### <span data-ttu-id="0b987-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0b987-113">-Name</span></span>
<span data-ttu-id="0b987-114">다시 시작할 Azure 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="0b987-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b987-115">-PassThru</span></span>
<span data-ttu-id="0b987-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b987-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b987-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="0b987-118">-Profile</span></span>
<span data-ttu-id="0b987-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b987-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b987-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="0b987-121">-Slot</span></span>
<span data-ttu-id="0b987-122">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="0b987-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b987-123">CommonParameters</span></span>
<span data-ttu-id="0b987-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b987-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b987-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b987-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b987-126">입력</span><span class="sxs-lookup"><span data-stu-id="0b987-126">INPUTS</span></span>

## <span data-ttu-id="0b987-127">출력</span><span class="sxs-lookup"><span data-stu-id="0b987-127">OUTPUTS</span></span>

## <span data-ttu-id="0b987-128">상속자</span><span class="sxs-lookup"><span data-stu-id="0b987-128">NOTES</span></span>

## <span data-ttu-id="0b987-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b987-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b987-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b987-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="0b987-131">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b987-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0b987-132">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b987-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="0b987-133">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b987-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)



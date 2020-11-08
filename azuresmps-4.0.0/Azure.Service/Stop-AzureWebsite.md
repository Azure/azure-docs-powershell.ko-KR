---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046588"
---
# <span data-ttu-id="984e8-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="984e8-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="984e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984e8-102">SYNOPSIS</span></span>
<span data-ttu-id="984e8-103">지정 된 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-103">Stops the specified website.</span></span>

## <span data-ttu-id="984e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="984e8-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="984e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="984e8-105">DESCRIPTION</span></span>
<span data-ttu-id="984e8-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="984e8-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="984e8-108">**AzureWebsite** Cmdlet은 Azure에서 호스팅되는 지정 된 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="984e8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="984e8-109">EXAMPLES</span></span>

## <span data-ttu-id="984e8-110">변수</span><span class="sxs-lookup"><span data-stu-id="984e8-110">PARAMETERS</span></span>

### <span data-ttu-id="984e8-111">-이름</span><span class="sxs-lookup"><span data-stu-id="984e8-111">-Name</span></span>
<span data-ttu-id="984e8-112">중지할 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="984e8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="984e8-113">-PassThru</span></span>
<span data-ttu-id="984e8-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="984e8-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="984e8-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="984e8-116">-Profile</span></span>
<span data-ttu-id="984e8-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="984e8-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="984e8-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="984e8-119">-Slot</span></span>
<span data-ttu-id="984e8-120">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="984e8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984e8-121">CommonParameters</span></span>
<span data-ttu-id="984e8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="984e8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984e8-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="984e8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984e8-124">입력</span><span class="sxs-lookup"><span data-stu-id="984e8-124">INPUTS</span></span>

## <span data-ttu-id="984e8-125">출력</span><span class="sxs-lookup"><span data-stu-id="984e8-125">OUTPUTS</span></span>

## <span data-ttu-id="984e8-126">상속자</span><span class="sxs-lookup"><span data-stu-id="984e8-126">NOTES</span></span>

## <span data-ttu-id="984e8-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="984e8-127">RELATED LINKS</span></span>

[<span data-ttu-id="984e8-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="984e8-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="984e8-129">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="984e8-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)



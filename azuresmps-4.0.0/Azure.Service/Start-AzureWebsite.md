---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045770"
---
# <span data-ttu-id="12367-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12367-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="12367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12367-102">SYNOPSIS</span></span>
<span data-ttu-id="12367-103">지정 된 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-103">Starts the specified website.</span></span>

## <span data-ttu-id="12367-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12367-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="12367-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12367-105">DESCRIPTION</span></span>
<span data-ttu-id="12367-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="12367-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="12367-108">**AzureWebsite** Cmdlet은 Azure에서 실행 되는 지정 된 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="12367-109">예제의</span><span class="sxs-lookup"><span data-stu-id="12367-109">EXAMPLES</span></span>

## <span data-ttu-id="12367-110">변수</span><span class="sxs-lookup"><span data-stu-id="12367-110">PARAMETERS</span></span>

### <span data-ttu-id="12367-111">-이름</span><span class="sxs-lookup"><span data-stu-id="12367-111">-Name</span></span>
<span data-ttu-id="12367-112">시작할 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="12367-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12367-113">-PassThru</span></span>
<span data-ttu-id="12367-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12367-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12367-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12367-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="12367-116">-Profile</span></span>
<span data-ttu-id="12367-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12367-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="12367-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12367-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="12367-119">-Slot</span></span>
<span data-ttu-id="12367-120">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="12367-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12367-121">CommonParameters</span></span>
<span data-ttu-id="12367-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12367-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12367-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12367-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12367-124">입력</span><span class="sxs-lookup"><span data-stu-id="12367-124">INPUTS</span></span>

## <span data-ttu-id="12367-125">출력</span><span class="sxs-lookup"><span data-stu-id="12367-125">OUTPUTS</span></span>

## <span data-ttu-id="12367-126">상속자</span><span class="sxs-lookup"><span data-stu-id="12367-126">NOTES</span></span>

## <span data-ttu-id="12367-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12367-127">RELATED LINKS</span></span>

[<span data-ttu-id="12367-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12367-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="12367-129">다시 시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12367-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="12367-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12367-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="12367-131">쇼-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12367-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="12367-132">중지-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12367-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)



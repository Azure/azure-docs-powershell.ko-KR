---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046374"
---
# <span data-ttu-id="9cc23-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="9cc23-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="9cc23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc23-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc23-103">웹 사이트의 디버그를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-103">Enables the website's debug.</span></span>

## <span data-ttu-id="9cc23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cc23-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9cc23-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9cc23-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc23-106">Visual Studio에서 웹 사이트의 디버그 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="9cc23-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9cc23-107">EXAMPLES</span></span>

### <span data-ttu-id="9cc23-108">Visual Studio 2013 디버깅 사용</span><span class="sxs-lookup"><span data-stu-id="9cc23-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="9cc23-109">VS 2013에서 디버깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="9cc23-110">변수</span><span class="sxs-lookup"><span data-stu-id="9cc23-110">PARAMETERS</span></span>

### <span data-ttu-id="9cc23-111">-이름</span><span class="sxs-lookup"><span data-stu-id="9cc23-111">-Name</span></span>
<span data-ttu-id="9cc23-112">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="9cc23-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cc23-113">-PassThru</span></span>
<span data-ttu-id="9cc23-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cc23-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cc23-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="9cc23-116">-Profile</span></span>
<span data-ttu-id="9cc23-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cc23-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9cc23-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="9cc23-119">-Slot</span></span>
<span data-ttu-id="9cc23-120">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="9cc23-121">-버전</span><span class="sxs-lookup"><span data-stu-id="9cc23-121">-Version</span></span>
<span data-ttu-id="9cc23-122">Visual Studio 버전</span><span class="sxs-lookup"><span data-stu-id="9cc23-122">The Visual Studio version.</span></span>

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

### <span data-ttu-id="9cc23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc23-123">CommonParameters</span></span>
<span data-ttu-id="9cc23-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cc23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc23-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc23-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc23-126">입력</span><span class="sxs-lookup"><span data-stu-id="9cc23-126">INPUTS</span></span>

## <span data-ttu-id="9cc23-127">출력</span><span class="sxs-lookup"><span data-stu-id="9cc23-127">OUTPUTS</span></span>

## <span data-ttu-id="9cc23-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9cc23-128">NOTES</span></span>

## <span data-ttu-id="9cc23-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cc23-129">RELATED LINKS</span></span>

[<span data-ttu-id="9cc23-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="9cc23-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="9cc23-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cc23-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="9cc23-132">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cc23-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="9cc23-133">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cc23-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="9cc23-134">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cc23-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045482"
---
# <span data-ttu-id="a4409-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a4409-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="a4409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4409-102">SYNOPSIS</span></span>
<span data-ttu-id="a4409-103">웹 사이트에 대 한 기존 웹 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="a4409-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4409-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a4409-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a4409-105">DESCRIPTION</span></span>
<span data-ttu-id="a4409-106">웹 사이트에 대 한 기존 웹 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="a4409-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a4409-107">EXAMPLES</span></span>

### <span data-ttu-id="a4409-108">예제 1: 웹 사이트에 대 한 기존 웹 작업 제거</span><span class="sxs-lookup"><span data-stu-id="a4409-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="a4409-109">MyWebSite 용 MyWebJob 이라는 웹 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="a4409-110">변수</span><span class="sxs-lookup"><span data-stu-id="a4409-110">PARAMETERS</span></span>

### <span data-ttu-id="a4409-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a4409-111">-Force</span></span>
<span data-ttu-id="a4409-112">이 cmdlet이 확인을 묻지 않고 웹 작업을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a4409-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a4409-113">-JobName</span></span>
<span data-ttu-id="a4409-114">웹 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-114">The web job name.</span></span>

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

### <span data-ttu-id="a4409-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="a4409-115">-JobType</span></span>
<span data-ttu-id="a4409-116">웹 작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-116">The web job type.</span></span>
<span data-ttu-id="a4409-117">트리거 또는 연속이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-117">Can be triggered or continuous.</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4409-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a4409-118">-Name</span></span>
<span data-ttu-id="a4409-119">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="a4409-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="a4409-120">-Profile</span></span>
<span data-ttu-id="a4409-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4409-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4409-123">-슬롯</span><span class="sxs-lookup"><span data-stu-id="a4409-123">-Slot</span></span>
<span data-ttu-id="a4409-124">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="a4409-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4409-125">CommonParameters</span></span>
<span data-ttu-id="a4409-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4409-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4409-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4409-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4409-128">입력</span><span class="sxs-lookup"><span data-stu-id="a4409-128">INPUTS</span></span>

## <span data-ttu-id="a4409-129">출력</span><span class="sxs-lookup"><span data-stu-id="a4409-129">OUTPUTS</span></span>

## <span data-ttu-id="a4409-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a4409-130">NOTES</span></span>

## <span data-ttu-id="a4409-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4409-131">RELATED LINKS</span></span>

[<span data-ttu-id="a4409-132">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a4409-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="a4409-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a4409-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="a4409-134">새로운 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a4409-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="a4409-135">시작-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a4409-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="a4409-136">중지-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="a4409-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)



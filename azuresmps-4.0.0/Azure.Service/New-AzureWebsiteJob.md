---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046183"
---
# <span data-ttu-id="1a6b3-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1a6b3-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="1a6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6b3-103">웹사이트에 대 한 웹 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="1a6b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a6b3-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a6b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="1a6b3-106">**새 AzureWebsiteJob** cmdlet은 웹 사이트에 대 한 웹 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="1a6b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a6b3-107">EXAMPLES</span></span>

### <span data-ttu-id="1a6b3-108">예제 1: 웹 사이트에 대 한 새 웹 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="1a6b3-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="1a6b3-109">웹 사이트 MyWebsite에서 job.bat를 호출 하는 연속 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="1a6b3-110">변수</span><span class="sxs-lookup"><span data-stu-id="1a6b3-110">PARAMETERS</span></span>

### <span data-ttu-id="1a6b3-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="1a6b3-111">-JobFile</span></span>
<span data-ttu-id="1a6b3-112">웹 작업 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-112">The web job file.</span></span>

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

### <span data-ttu-id="1a6b3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1a6b3-113">-JobName</span></span>
<span data-ttu-id="1a6b3-114">웹 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-114">The web job name.</span></span>

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

### <span data-ttu-id="1a6b3-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="1a6b3-115">-JobType</span></span>
<span data-ttu-id="1a6b3-116">웹 작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-116">The web job type.</span></span>
<span data-ttu-id="1a6b3-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a6b3-118">되었을</span><span class="sxs-lookup"><span data-stu-id="1a6b3-118">Triggered</span></span> 
- <span data-ttu-id="1a6b3-119">연속적</span><span class="sxs-lookup"><span data-stu-id="1a6b3-119">Continuous</span></span>

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

### <span data-ttu-id="1a6b3-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1a6b3-120">-Name</span></span>
<span data-ttu-id="1a6b3-121">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="1a6b3-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="1a6b3-122">-Profile</span></span>
<span data-ttu-id="1a6b3-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a6b3-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a6b3-125">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1a6b3-125">-Slot</span></span>
<span data-ttu-id="1a6b3-126">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="1a6b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6b3-127">CommonParameters</span></span>
<span data-ttu-id="1a6b3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6b3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a6b3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6b3-130">입력</span><span class="sxs-lookup"><span data-stu-id="1a6b3-130">INPUTS</span></span>

## <span data-ttu-id="1a6b3-131">출력</span><span class="sxs-lookup"><span data-stu-id="1a6b3-131">OUTPUTS</span></span>

## <span data-ttu-id="1a6b3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1a6b3-132">NOTES</span></span>

## <span data-ttu-id="1a6b3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a6b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a6b3-134">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a6b3-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1a6b3-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1a6b3-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="1a6b3-136">제거-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1a6b3-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="1a6b3-137">시작-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1a6b3-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="1a6b3-138">중지-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1a6b3-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)



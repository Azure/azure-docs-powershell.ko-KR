---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046273"
---
# <span data-ttu-id="22ef6-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="22ef6-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="22ef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="22ef6-103">웹 사이트와 연결 된 웹 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="22ef6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22ef6-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22ef6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="22ef6-106">웹 사이트와 연결 된 웹 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="22ef6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="22ef6-108">예제 1: 특정 웹 작업 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="22ef6-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="22ef6-109">MyWebsite 프로덕션 슬롯에서 MyWebJob 이라고 하는 웹 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="22ef6-110">예제 2: 웹 사이트에 대 한 모든 웹 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="22ef6-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="22ef6-111">MyWebsite 프로덕션 슬롯에 연결 된 모든 웹 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="22ef6-112">예제 3: 트리거된 모든 웹 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="22ef6-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="22ef6-113">MyWebsite의 스테이징 슬롯에서 트리거된 모든 웹 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="22ef6-114">변수</span><span class="sxs-lookup"><span data-stu-id="22ef6-114">PARAMETERS</span></span>

### <span data-ttu-id="22ef6-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="22ef6-115">-JobName</span></span>
<span data-ttu-id="22ef6-116">웹 작업 이름</span><span class="sxs-lookup"><span data-stu-id="22ef6-116">The web job name</span></span>

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

### <span data-ttu-id="22ef6-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="22ef6-117">-JobType</span></span>
<span data-ttu-id="22ef6-118">웹 작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-118">The web job type.</span></span>
<span data-ttu-id="22ef6-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22ef6-120">되었을</span><span class="sxs-lookup"><span data-stu-id="22ef6-120">Triggered</span></span>
- <span data-ttu-id="22ef6-121">연속적</span><span class="sxs-lookup"><span data-stu-id="22ef6-121">Continuous</span></span>

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

### <span data-ttu-id="22ef6-122">-이름</span><span class="sxs-lookup"><span data-stu-id="22ef6-122">-Name</span></span>
<span data-ttu-id="22ef6-123">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="22ef6-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="22ef6-124">-Profile</span></span>
<span data-ttu-id="22ef6-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22ef6-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22ef6-127">-슬롯</span><span class="sxs-lookup"><span data-stu-id="22ef6-127">-Slot</span></span>
<span data-ttu-id="22ef6-128">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="22ef6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ef6-129">CommonParameters</span></span>
<span data-ttu-id="22ef6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ef6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ef6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ef6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ef6-132">입력</span><span class="sxs-lookup"><span data-stu-id="22ef6-132">INPUTS</span></span>

## <span data-ttu-id="22ef6-133">출력</span><span class="sxs-lookup"><span data-stu-id="22ef6-133">OUTPUTS</span></span>

## <span data-ttu-id="22ef6-134">상속자</span><span class="sxs-lookup"><span data-stu-id="22ef6-134">NOTES</span></span>

## <span data-ttu-id="22ef6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22ef6-135">RELATED LINKS</span></span>

[<span data-ttu-id="22ef6-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="22ef6-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="22ef6-137">새로운 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="22ef6-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="22ef6-138">제거-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="22ef6-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="22ef6-139">시작-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="22ef6-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="22ef6-140">중지-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="22ef6-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045767"
---
# <span data-ttu-id="13fdd-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="13fdd-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="13fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="13fdd-103">웹사이트에 대 한 웹 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="13fdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13fdd-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13fdd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="13fdd-106">**AzureWebsiteJob** cmdlet은 웹사이트에 대 한 웹 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="13fdd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="13fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="13fdd-108">예제 1: 웹 사이트에 대 한 웹 작업 시작</span><span class="sxs-lookup"><span data-stu-id="13fdd-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="13fdd-109">MyWebSite 용 MyWebJob 이라는 웹 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="13fdd-110">변수</span><span class="sxs-lookup"><span data-stu-id="13fdd-110">PARAMETERS</span></span>

### <span data-ttu-id="13fdd-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="13fdd-111">-JobName</span></span>
<span data-ttu-id="13fdd-112">웹 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-112">The web job name.</span></span>

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

### <span data-ttu-id="13fdd-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="13fdd-113">-JobType</span></span>
<span data-ttu-id="13fdd-114">웹 작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-114">The web job type.</span></span>
<span data-ttu-id="13fdd-115">트리거 또는 연속이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="13fdd-116">-이름</span><span class="sxs-lookup"><span data-stu-id="13fdd-116">-Name</span></span>
<span data-ttu-id="13fdd-117">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="13fdd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13fdd-118">-PassThru</span></span>
<span data-ttu-id="13fdd-119">작업이 성공적으로 시작 되었음을 나타내는 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="13fdd-120">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="13fdd-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="13fdd-121">-Profile</span></span>
<span data-ttu-id="13fdd-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13fdd-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13fdd-124">-슬롯</span><span class="sxs-lookup"><span data-stu-id="13fdd-124">-Slot</span></span>
<span data-ttu-id="13fdd-125">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="13fdd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fdd-126">CommonParameters</span></span>
<span data-ttu-id="13fdd-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fdd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fdd-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fdd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fdd-129">입력</span><span class="sxs-lookup"><span data-stu-id="13fdd-129">INPUTS</span></span>

## <span data-ttu-id="13fdd-130">출력</span><span class="sxs-lookup"><span data-stu-id="13fdd-130">OUTPUTS</span></span>

## <span data-ttu-id="13fdd-131">상속자</span><span class="sxs-lookup"><span data-stu-id="13fdd-131">NOTES</span></span>

## <span data-ttu-id="13fdd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13fdd-132">RELATED LINKS</span></span>

[<span data-ttu-id="13fdd-133">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="13fdd-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="13fdd-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="13fdd-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="13fdd-135">새로운 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="13fdd-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="13fdd-136">제거-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="13fdd-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="13fdd-137">시작-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="13fdd-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)



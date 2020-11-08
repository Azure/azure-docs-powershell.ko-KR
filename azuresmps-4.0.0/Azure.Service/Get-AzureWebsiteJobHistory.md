---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046507"
---
# <span data-ttu-id="28d46-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="28d46-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="28d46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d46-102">SYNOPSIS</span></span>
<span data-ttu-id="28d46-103">웹 작업 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-103">Gets a web job history.</span></span>

## <span data-ttu-id="28d46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28d46-104">SYNTAX</span></span>

### <span data-ttu-id="28d46-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="28d46-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="28d46-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="28d46-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="28d46-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="28d46-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28d46-108">설명은</span><span class="sxs-lookup"><span data-stu-id="28d46-108">DESCRIPTION</span></span>
<span data-ttu-id="28d46-109">웹 작업 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-109">Gets a web job history.</span></span>

## <span data-ttu-id="28d46-110">예제의</span><span class="sxs-lookup"><span data-stu-id="28d46-110">EXAMPLES</span></span>

### <span data-ttu-id="28d46-111">예제 1: 웹 작업에 대 한 전체 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d46-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="28d46-112">MyWebJob에 대 한 전체 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="28d46-113">예제 2: 웹 작업에 대 한 최신 실행 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d46-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="28d46-114">MyWebJob에 대 한 최신 실행 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="28d46-115">예제 3: 웹 작업에 대 한 특정 실행 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d46-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="28d46-116">MyWebJob에 대해 id 10으로 실행에 대 한 모든 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="28d46-117">변수</span><span class="sxs-lookup"><span data-stu-id="28d46-117">PARAMETERS</span></span>

### <span data-ttu-id="28d46-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="28d46-118">-JobName</span></span>
<span data-ttu-id="28d46-119">웹 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-119">The web job name.</span></span>

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

### <span data-ttu-id="28d46-120">-최신 버전</span><span class="sxs-lookup"><span data-stu-id="28d46-120">-Latest</span></span>
<span data-ttu-id="28d46-121">지정 된 경우 최신 실행 기록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d46-122">-이름</span><span class="sxs-lookup"><span data-stu-id="28d46-122">-Name</span></span>
<span data-ttu-id="28d46-123">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="28d46-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="28d46-124">-Profile</span></span>
<span data-ttu-id="28d46-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28d46-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28d46-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="28d46-127">-RunId</span></span>
<span data-ttu-id="28d46-128">보려는 실행 기록의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28d46-129">-슬롯</span><span class="sxs-lookup"><span data-stu-id="28d46-129">-Slot</span></span>
<span data-ttu-id="28d46-130">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="28d46-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d46-131">CommonParameters</span></span>
<span data-ttu-id="28d46-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d46-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d46-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d46-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d46-134">입력</span><span class="sxs-lookup"><span data-stu-id="28d46-134">INPUTS</span></span>

## <span data-ttu-id="28d46-135">출력</span><span class="sxs-lookup"><span data-stu-id="28d46-135">OUTPUTS</span></span>

## <span data-ttu-id="28d46-136">상속자</span><span class="sxs-lookup"><span data-stu-id="28d46-136">NOTES</span></span>

## <span data-ttu-id="28d46-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28d46-137">RELATED LINKS</span></span>

[<span data-ttu-id="28d46-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="28d46-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="28d46-139">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="28d46-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="28d46-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="28d46-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="28d46-141">새로운 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="28d46-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="28d46-142">제거-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="28d46-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045612"
---
# <span data-ttu-id="a308c-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a308c-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="a308c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a308c-102">SYNOPSIS</span></span>
<span data-ttu-id="a308c-103">스케줄러 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="a308c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a308c-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a308c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a308c-105">DESCRIPTION</span></span>
<span data-ttu-id="a308c-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a308c-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a308c-108">**AzureSchedulerJobCollection** cmdlet은 하나 이상의 스케줄러 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="a308c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a308c-109">EXAMPLES</span></span>

### <span data-ttu-id="a308c-110">예제 1: 모든 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="a308c-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="a308c-111">이 명령은 현재 구독의 모든 위치에서 모든 스케줄러 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="a308c-112">예제 2: 위치에 대 한 모든 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="a308c-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="a308c-113">이 명령은 미국 중부 US 라는 위치에 있는 모든 스케줄러 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="a308c-114">예제 3: 이름을 사용 하 여 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="a308c-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="a308c-115">이 명령은 JobCollection01 이라는 스케줄러 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="a308c-116">변수</span><span class="sxs-lookup"><span data-stu-id="a308c-116">PARAMETERS</span></span>

### <span data-ttu-id="a308c-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a308c-117">-JobCollectionName</span></span>
<span data-ttu-id="a308c-118">가져올 스케줄러 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="a308c-119">-위치</span><span class="sxs-lookup"><span data-stu-id="a308c-119">-Location</span></span>
<span data-ttu-id="a308c-120">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="a308c-121">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-121">Valid values are:</span></span> 

- <span data-ttu-id="a308c-122">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="a308c-122">Anywhere Asia</span></span>
- <span data-ttu-id="a308c-123">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="a308c-123">Anywhere Europe</span></span>
- <span data-ttu-id="a308c-124">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="a308c-124">Anywhere US</span></span>
- <span data-ttu-id="a308c-125">동아시아</span><span class="sxs-lookup"><span data-stu-id="a308c-125">East Asia</span></span>
- <span data-ttu-id="a308c-126">미국 동부</span><span class="sxs-lookup"><span data-stu-id="a308c-126">East US</span></span>
- <span data-ttu-id="a308c-127">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="a308c-127">North Central US</span></span>
- <span data-ttu-id="a308c-128">동유럽</span><span class="sxs-lookup"><span data-stu-id="a308c-128">North Europe</span></span>
- <span data-ttu-id="a308c-129">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="a308c-129">South Central US</span></span>
- <span data-ttu-id="a308c-130">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="a308c-130">Southeast Asia</span></span>
- <span data-ttu-id="a308c-131">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="a308c-131">West Europe</span></span>
- <span data-ttu-id="a308c-132">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="a308c-132">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a308c-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="a308c-133">-Profile</span></span>
<span data-ttu-id="a308c-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a308c-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a308c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a308c-136">CommonParameters</span></span>
<span data-ttu-id="a308c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a308c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a308c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a308c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a308c-139">입력</span><span class="sxs-lookup"><span data-stu-id="a308c-139">INPUTS</span></span>

## <span data-ttu-id="a308c-140">출력</span><span class="sxs-lookup"><span data-stu-id="a308c-140">OUTPUTS</span></span>

## <span data-ttu-id="a308c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a308c-141">NOTES</span></span>

## <span data-ttu-id="a308c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a308c-142">RELATED LINKS</span></span>

[<span data-ttu-id="a308c-143">새로운 AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a308c-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="a308c-144">제거-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a308c-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="a308c-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a308c-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046129"
---
# <span data-ttu-id="3809b-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="3809b-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="3809b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3809b-102">SYNOPSIS</span></span>
<span data-ttu-id="3809b-103">스케줄러 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="3809b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3809b-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3809b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3809b-105">DESCRIPTION</span></span>
<span data-ttu-id="3809b-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3809b-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3809b-108">**AzureSchedulerJob** cmdlet은 스케줄러 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="3809b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3809b-109">EXAMPLES</span></span>

### <span data-ttu-id="3809b-110">예제 1: 스케줄러 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="3809b-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="3809b-111">이 명령은 Job17 이라는 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="3809b-112">해당 작업은 JobCollection01 이라는 작업 컬렉션의 일부 이며 지정 된 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="3809b-113">변수</span><span class="sxs-lookup"><span data-stu-id="3809b-113">PARAMETERS</span></span>

### <span data-ttu-id="3809b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3809b-114">-Force</span></span>
<span data-ttu-id="3809b-115">이 cmdlet이 스케줄러 작업이 확인 메시지 없이 제거 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3809b-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3809b-116">-JobCollectionName</span></span>
<span data-ttu-id="3809b-117">삭제할 스케줄러 작업을 포함 하는 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="3809b-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="3809b-118">-JobName</span></span>
<span data-ttu-id="3809b-119">삭제할 스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="3809b-120">-위치</span><span class="sxs-lookup"><span data-stu-id="3809b-120">-Location</span></span>
<span data-ttu-id="3809b-121">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="3809b-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-122">Valid values are:</span></span> 

- <span data-ttu-id="3809b-123">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="3809b-123">Anywhere Asia</span></span>
- <span data-ttu-id="3809b-124">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="3809b-124">Anywhere Europe</span></span>
- <span data-ttu-id="3809b-125">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="3809b-125">Anywhere US</span></span>
- <span data-ttu-id="3809b-126">동아시아</span><span class="sxs-lookup"><span data-stu-id="3809b-126">East Asia</span></span>
- <span data-ttu-id="3809b-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="3809b-127">East US</span></span>
- <span data-ttu-id="3809b-128">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="3809b-128">North Central US</span></span>
- <span data-ttu-id="3809b-129">동유럽</span><span class="sxs-lookup"><span data-stu-id="3809b-129">North Europe</span></span>
- <span data-ttu-id="3809b-130">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="3809b-130">South Central US</span></span>
- <span data-ttu-id="3809b-131">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="3809b-131">Southeast Asia</span></span>
- <span data-ttu-id="3809b-132">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="3809b-132">West Europe</span></span>
- <span data-ttu-id="3809b-133">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="3809b-133">West US</span></span>

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

### <span data-ttu-id="3809b-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="3809b-134">-Profile</span></span>
<span data-ttu-id="3809b-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3809b-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3809b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3809b-137">CommonParameters</span></span>
<span data-ttu-id="3809b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3809b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3809b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3809b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3809b-140">입력</span><span class="sxs-lookup"><span data-stu-id="3809b-140">INPUTS</span></span>

## <span data-ttu-id="3809b-141">출력</span><span class="sxs-lookup"><span data-stu-id="3809b-141">OUTPUTS</span></span>

## <span data-ttu-id="3809b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="3809b-142">NOTES</span></span>

## <span data-ttu-id="3809b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3809b-143">RELATED LINKS</span></span>

[<span data-ttu-id="3809b-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="3809b-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)



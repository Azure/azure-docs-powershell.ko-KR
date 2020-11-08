---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046128"
---
# <span data-ttu-id="0f34b-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f34b-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="0f34b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f34b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f34b-103">스케줄러 작업 컬렉션을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="0f34b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f34b-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f34b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f34b-105">DESCRIPTION</span></span>
<span data-ttu-id="0f34b-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0f34b-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0f34b-108">**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 컬렉션 및 해당 컬렉션 아래의 모든 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="0f34b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0f34b-109">EXAMPLES</span></span>

### <span data-ttu-id="0f34b-110">예제 1: 위치에 대 한 작업 컬렉션 삭제</span><span class="sxs-lookup"><span data-stu-id="0f34b-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="0f34b-111">이 명령은 미국 중부 US 위치에서 JobCollection01 이라는 스케줄러 작업 컬렉션을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="0f34b-112">또한이 명령은 JobCollection01에서 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="0f34b-113">예제 2: 작업 위치 삭제</span><span class="sxs-lookup"><span data-stu-id="0f34b-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="0f34b-114">이 명령은 JobCollection02 이라는 스케줄러 작업 컬렉션을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="0f34b-115">또한이 명령은 JobCollection02에서 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="0f34b-116">변수</span><span class="sxs-lookup"><span data-stu-id="0f34b-116">PARAMETERS</span></span>

### <span data-ttu-id="0f34b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f34b-117">-Force</span></span>
<span data-ttu-id="0f34b-118">이 cmdlet이 스케줄러 작업 컬렉션을 확인 메시지 없이 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0f34b-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0f34b-119">-JobCollectionName</span></span>
<span data-ttu-id="0f34b-120">삭제할 스케줄러 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="0f34b-121">-위치</span><span class="sxs-lookup"><span data-stu-id="0f34b-121">-Location</span></span>
<span data-ttu-id="0f34b-122">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="0f34b-123">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-123">Valid values are:</span></span> 

- <span data-ttu-id="0f34b-124">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="0f34b-124">Anywhere Asia</span></span>
- <span data-ttu-id="0f34b-125">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="0f34b-125">Anywhere Europe</span></span>
- <span data-ttu-id="0f34b-126">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="0f34b-126">Anywhere US</span></span>
- <span data-ttu-id="0f34b-127">동아시아</span><span class="sxs-lookup"><span data-stu-id="0f34b-127">East Asia</span></span>
- <span data-ttu-id="0f34b-128">미국 동부</span><span class="sxs-lookup"><span data-stu-id="0f34b-128">East US</span></span>
- <span data-ttu-id="0f34b-129">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="0f34b-129">North Central US</span></span>
- <span data-ttu-id="0f34b-130">동유럽</span><span class="sxs-lookup"><span data-stu-id="0f34b-130">North Europe</span></span>
- <span data-ttu-id="0f34b-131">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="0f34b-131">South Central US</span></span>
- <span data-ttu-id="0f34b-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="0f34b-132">Southeast Asia</span></span>
- <span data-ttu-id="0f34b-133">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="0f34b-133">West Europe</span></span>
- <span data-ttu-id="0f34b-134">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="0f34b-134">West US</span></span>

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

### <span data-ttu-id="0f34b-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="0f34b-135">-Profile</span></span>
<span data-ttu-id="0f34b-136">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f34b-137">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f34b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f34b-138">CommonParameters</span></span>
<span data-ttu-id="0f34b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f34b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f34b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f34b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f34b-141">입력</span><span class="sxs-lookup"><span data-stu-id="0f34b-141">INPUTS</span></span>

## <span data-ttu-id="0f34b-142">출력</span><span class="sxs-lookup"><span data-stu-id="0f34b-142">OUTPUTS</span></span>

## <span data-ttu-id="0f34b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="0f34b-143">NOTES</span></span>

## <span data-ttu-id="0f34b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f34b-144">RELATED LINKS</span></span>

[<span data-ttu-id="0f34b-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f34b-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0f34b-146">새로운 AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f34b-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0f34b-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0f34b-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)



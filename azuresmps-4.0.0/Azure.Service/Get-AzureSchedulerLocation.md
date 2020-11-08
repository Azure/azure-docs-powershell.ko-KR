---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045611"
---
# <span data-ttu-id="458d5-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="458d5-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="458d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458d5-102">SYNOPSIS</span></span>
<span data-ttu-id="458d5-103">사용할 수 있는 스케줄러 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="458d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="458d5-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="458d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="458d5-105">DESCRIPTION</span></span>
<span data-ttu-id="458d5-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="458d5-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="458d5-108">**Get-AzureSchedulerLocation** cmdlet은 사용 가능한 스케줄러 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="458d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="458d5-109">EXAMPLES</span></span>

### <span data-ttu-id="458d5-110">예제 1: 사용할 수 있는 스케줄러 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="458d5-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="458d5-111">이 명령은 사용할 수 있는 스케줄러 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="458d5-112">변수</span><span class="sxs-lookup"><span data-stu-id="458d5-112">PARAMETERS</span></span>

### <span data-ttu-id="458d5-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="458d5-113">-Profile</span></span>
<span data-ttu-id="458d5-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="458d5-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="458d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458d5-116">CommonParameters</span></span>
<span data-ttu-id="458d5-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="458d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458d5-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458d5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458d5-119">입력</span><span class="sxs-lookup"><span data-stu-id="458d5-119">INPUTS</span></span>

## <span data-ttu-id="458d5-120">출력</span><span class="sxs-lookup"><span data-stu-id="458d5-120">OUTPUTS</span></span>

## <span data-ttu-id="458d5-121">상속자</span><span class="sxs-lookup"><span data-stu-id="458d5-121">NOTES</span></span>

## <span data-ttu-id="458d5-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="458d5-122">RELATED LINKS</span></span>

[<span data-ttu-id="458d5-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="458d5-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="458d5-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="458d5-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="458d5-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="458d5-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046336"
---
# <span data-ttu-id="03f46-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="03f46-101">Get-AzureLocation</span></span>

## <span data-ttu-id="03f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f46-102">SYNOPSIS</span></span>
<span data-ttu-id="03f46-103">현재 Azure 구독에 대해 사용 가능한 데이터 센터 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="03f46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03f46-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="03f46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03f46-105">DESCRIPTION</span></span>
<span data-ttu-id="03f46-106">**Get AzureLocation** cmdlet은 사용 가능한 azure 데이터 센터 및 현재 azure 구독에 대 한 해당 속성의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="03f46-107">이 cmdlet을 실행 하기 전에 Select-AzureSubscription 및 Set-AzureSubscription cmdlet을 사용 하 여 현재 구독을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="03f46-108">예제의</span><span class="sxs-lookup"><span data-stu-id="03f46-108">EXAMPLES</span></span>

### <span data-ttu-id="03f46-109">예제 1: 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="03f46-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="03f46-110">이 명령은 현재 구독에 대해 사용 가능한 데이터 센터 목록과 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="03f46-111">변수</span><span class="sxs-lookup"><span data-stu-id="03f46-111">PARAMETERS</span></span>

### <span data-ttu-id="03f46-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="03f46-112">-InformationAction</span></span>
<span data-ttu-id="03f46-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="03f46-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03f46-115">하기로</span><span class="sxs-lookup"><span data-stu-id="03f46-115">Continue</span></span>
- <span data-ttu-id="03f46-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="03f46-116">Ignore</span></span>
- <span data-ttu-id="03f46-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="03f46-117">Inquire</span></span>
- <span data-ttu-id="03f46-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="03f46-118">SilentlyContinue</span></span>
- <span data-ttu-id="03f46-119">중지가</span><span class="sxs-lookup"><span data-stu-id="03f46-119">Stop</span></span>
- <span data-ttu-id="03f46-120">대기</span><span class="sxs-lookup"><span data-stu-id="03f46-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03f46-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="03f46-121">-InformationVariable</span></span>
<span data-ttu-id="03f46-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03f46-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="03f46-123">-Profile</span></span>
<span data-ttu-id="03f46-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03f46-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03f46-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f46-126">CommonParameters</span></span>
<span data-ttu-id="03f46-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03f46-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f46-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f46-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f46-129">입력</span><span class="sxs-lookup"><span data-stu-id="03f46-129">INPUTS</span></span>

## <span data-ttu-id="03f46-130">출력</span><span class="sxs-lookup"><span data-stu-id="03f46-130">OUTPUTS</span></span>

## <span data-ttu-id="03f46-131">상속자</span><span class="sxs-lookup"><span data-stu-id="03f46-131">NOTES</span></span>

## <span data-ttu-id="03f46-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03f46-132">RELATED LINKS</span></span>


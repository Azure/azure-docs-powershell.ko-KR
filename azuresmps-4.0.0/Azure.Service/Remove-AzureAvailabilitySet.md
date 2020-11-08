---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046168"
---
# <span data-ttu-id="c61ab-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c61ab-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="c61ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c61ab-103">Azure 가상 머신에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="c61ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c61ab-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c61ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c61ab-105">DESCRIPTION</span></span>
<span data-ttu-id="c61ab-106">**AzureAvailabilitySet** Cmdlet은 Azure 가상 컴퓨터에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="c61ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c61ab-107">EXAMPLES</span></span>

### <span data-ttu-id="c61ab-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="c61ab-108">1:</span></span>
```

```

## <span data-ttu-id="c61ab-109">변수</span><span class="sxs-lookup"><span data-stu-id="c61ab-109">PARAMETERS</span></span>

### <span data-ttu-id="c61ab-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c61ab-110">-InformationAction</span></span>
<span data-ttu-id="c61ab-111">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c61ab-112">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c61ab-113">하기로</span><span class="sxs-lookup"><span data-stu-id="c61ab-113">Continue</span></span>
- <span data-ttu-id="c61ab-114">숨기기</span><span class="sxs-lookup"><span data-stu-id="c61ab-114">Ignore</span></span>
- <span data-ttu-id="c61ab-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="c61ab-115">Inquire</span></span>
- <span data-ttu-id="c61ab-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c61ab-116">SilentlyContinue</span></span>
- <span data-ttu-id="c61ab-117">중지가</span><span class="sxs-lookup"><span data-stu-id="c61ab-117">Stop</span></span>
- <span data-ttu-id="c61ab-118">대기</span><span class="sxs-lookup"><span data-stu-id="c61ab-118">Suspend</span></span>

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

### <span data-ttu-id="c61ab-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c61ab-119">-InformationVariable</span></span>
<span data-ttu-id="c61ab-120">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c61ab-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="c61ab-121">-Profile</span></span>
<span data-ttu-id="c61ab-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c61ab-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c61ab-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c61ab-124">-VM</span></span>
<span data-ttu-id="c61ab-125">이 cmdlet에서 가용성 집합을 제거 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61ab-126">CommonParameters</span></span>
<span data-ttu-id="c61ab-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61ab-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61ab-129">입력</span><span class="sxs-lookup"><span data-stu-id="c61ab-129">INPUTS</span></span>

## <span data-ttu-id="c61ab-130">출력</span><span class="sxs-lookup"><span data-stu-id="c61ab-130">OUTPUTS</span></span>

## <span data-ttu-id="c61ab-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c61ab-131">NOTES</span></span>

## <span data-ttu-id="c61ab-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c61ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="c61ab-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c61ab-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


